# 代码工艺——嵌入 C++:定时虚函数

> 原文：<https://hackaday.com/2015/11/13/code-craft-embedding-c-timing-virtual-functions/>

出于对性能的考虑，嵌入式 C 开发人员回避 C++。*类*构造是他们主要关心的问题之一。我的上一篇文章 [*代码工艺——嵌入 C++:类*](http://hackaday.com/2015/11/06/code-craft-embedding-c-classes/) 探讨了类是否会导致代码膨胀。很少或没有膨胀，这确保了初始化的发生。

总的来说，使用类和 C++是有利的，因为它部分地通过将数据和对数据的操作组织到一个编程结构中，产生了看起来更整洁的代码。对类的这种简单使用并不是它们存在的理由，而是为了提供*继承*，或者更具体地说是*多态*(来自希腊语 polys，“many，much”和 morph“form，shape”)。

怀疑论者认为，遗传必然会导致时间上令人讨厌的增加。在这里，我再次勇敢地断言，没有这样的增长发生，并将提供并排比较作为证据。

# 遗产

C++使用的继承多态形式是子类型。正如上次提到的，我们正在创建*用户定义类型* (UDT ),编译器会像对待标准语言类型一样对待它们。子类型继承其父类型的特征，可以使用或不使用父类型的成员函数。你会看到这种关系有多种说法:父/子、超类/子类等等。

让我们看看用于测试遍历继承和虚函数的时间的 C++代码。父类是类 *PinOutputAbstract* 。它代表 Arduino 上的一个输出引脚:

```

class PinOutputAbstract {
public:
	PinOutputAbstract(const unsigned int pin) :
			mPinNum { pin } {
		pinMode(mPinNum, OUTPUT);
	}
	virtual ~PinOutputAbstract() { 	}
	virtual void output() const = 0;

	static void outputPins();
protected:
	const unsigned int mPinNum;

	static PinOutputAbstract* mOutpuDevices[];
	static const size_t mOutDevicesCnt;
};
using PinPtr = PinOutputAbstract*;

```

该类需要一个数据，即被访问的 pin 号: *mPinNum。*它遵循*受保护的*关键字，该关键字决定谁可以访问该数据。受保护的类成员可以由子类型访问，但不能由该类的用户访问。实际上，子类型的*是公共的*，而用户的*是私有的*。 *mPinNum* 的值在使用该类的过程中不会改变，因此它被设置为 *const* ，这意味着它必须由构造函数 *PinOutputAbstract，*初始化，该构造函数接收该值作为参数。初始化由构造函数名称和参数列表后面的表达式处理:'`: mPinNum(pin)'.`,然后构造函数的主体将 pin 初始化为输出。

构造函数之后是析构函数，它被声明为虚拟的。这个类不需要析构函数，因为没有任何资源或动态内存需要释放。但是忘记析构函数是一个常见的错误，尤其是在使用虚函数的时候，所以编译器会让你包含它。

我们感兴趣的虚函数是 *output()* 。跟在它后面的*常量*表示它没有改变类中的任何成员。这允许编译器执行优化，并在将来对函数的修改试图更改成员时生成错误。

另外，*输出()*被*常量后的`'=0'`声明为*纯虚拟*。这样的函数不需要有体，尽管它可以有。它使 *PinOutputAbstract* 成为一个抽象类，因此得名，它不能被实例化。这接近于其他语言中使用的*接口和*，除了 C++中的抽象类可以有代码体成员。*

我们稍后将讨论的*静态*成员，因为它们不直接涉及继承。

我们现在来看两种亚型:*数字输出*和*模拟输出*。最初的 Arduino 没有真正的数模输出(DAC)，但这是使用数字输出引脚上的*脉冲宽度* *调制* (PWM)伪造的。PWM 改变引脚的开和关时间，从而在引脚上产生可变电压。我们的类代表 Arduino 的纯二进制输出和 PWM 输出能力。DigitalOut 类在每次调用时打开和关闭它的管脚，只是为了让事情变得有趣。

下面是二进制数字输出类:

```

class DigitalOut: public PinOutputAbstract {

public:
	DigitalOut(const unsigned char pin) :
			PinOutputAbstract(pin) {
	}
	virtual ~DigitalOut() { }
	virtual void output() const;
};

```

继承关系在第一行用`': public PinOutputAbstract'`声明。这表明 *DigitalOut* 公开继承了 *PinOutputAbstract* 。还有*私有*和*保护*继承，但那些是你自己研究的细节。继承允许子进程访问父进程的公共成员。

构造函数遵循*公共*声明，并用作为参数传递的 pin 号初始化其父类。还有一个虚析构函数，它的主体是空的，这让编译器很高兴。最后， *output()* 方法声明。该声明必须与父级中的声明完全相同。

除了类名之外， *AnalogOut* 类声明是相同的:

```

class AnalogOut: public PinOutputAbstract {
public:
	AnalogOut(const int pin) : PinOutputAbstract(pin) { }
	virtual ~AnalogOut() { }

	virtual void output() const;
};

```

这两个成员的实现非常简单:

```

void DigitalOut::output() const {
    digitalWrite(mPinNum, !digitalRead(mPinNum));
}

void AnalogOut::output() const {
	analogWrite(mPinNum, 100);
}

```

### 使用

虚拟成员函数可以像非虚拟函数一样被调用:

```

AnalogOut ao(11);
AnalogOut* ao_ptr;

ao.output();
ao_ptr-&gt;output();

```

有趣的是实际代码中的这种用法:

```

DigitalOut pin13(13);
AnalogOut pin11(11);

PinPtr PinOutputAbstract::mOutpuDevices[] { &amp;pin13, &amp;pin11, &amp;pin13, &amp;pin11, &amp;pin13, &amp;pin11, &amp;pin13, &amp;pin11, &amp;pin13, &amp;pin11, };
PinPtr pin13_ptr = &amp;pin13;

void PinOutputAbstract::outputPins() {
	for (auto p : mOutpuDevices) {   // C++11
		p-&gt;output();
	}
}

```

数组 *mOutpuDevices* 被声明为包含指向父类 *PinOutputAbstract* 的指针。但是数组元素是指向子类实例的指针。这是继承的一个特点，很厉害。这意味着您可以在不知道实例的类的情况下使用它们的集合。您可以在这些实例上调用任何虚函数。

我使用 C++11 初始化，使用{}s，基于循环的*范围遍历数组，以及 *auto* 允许编译器确定迭代器的类型。基于的 C++范围使得处理数组更加简洁。*

如果你回头看看 *PinOutputAbstract* 的声明，有三行带有关键字 *static* 。C++使用这个关键字来表示这些是类的成员，而不是实例的成员。不需要用点或箭头符号来调用它们。相反，它们是用类名和作用域运算符来调用的。成员函数 *outputPins()* 在计时测试中使用。它遍历数组 *mOutputDevices* ，正如我们刚刚看到的。

### 虚拟表格

使用虚函数的代价是什么？为什么有些人认为这是在嵌入式系统中不使用 C++的好理由？让我们看一个典型的编译器实现。

每个具有虚函数的类都有一个附加的数据结构，指向一个*虚拟表*或*虚拟表*。vtable 是类中虚函数的地址数组。对于我们的例子，将有一个条目。图解你有:

`DigitalOut* -> vtable_ptr -> vtable[0] -> output()`

哦！所有那些指针的恐怖！开销！开销！

简单来说就是继承和虚函数。这不是一个教程，只是对 C++的这个特性的一瞥。关于如何有效地使用继承，有大量的附加信息，包括何时不使用继承来代替其他技术。

让我们开始测试，看看 C++是否真的更慢。当然不是。

# 测试场景

一个非平凡嵌入式系统中的基本处理循环是:*采集* *数据* *，* *执行* *进程* *ing* *，* *发射* *输出。*您需要环境的一致快照，这意味着一次读取所有输入。所有的输出都需要一次完成，所以改变是同时进行的。

一种方法是创建一个输入设备列表，并一次性读取它们的所有数据。类似地，创建输出设备的列表，并在输出时遍历列表。

这就是我们在这个场景中要做的，使用上面定义的类，以及它们的 C 代码等价物，如下所示。这对 Arduion Uno 来说有点大材小用，因为它只有 14 个数字引脚。但是考虑处理 Due 或附加子板的 54 个引脚，这将极大地扩展 IO 能力。

我使用 LED 引脚 13 作为数字输出，引脚 11 作为模拟输出。引脚 13 在每次通过时切换。模拟输出被设置为一个固定值，尽管它对于 C 和 C++是不同的，所以我可以使用我的新玩具 Rigol o-scope 来检查输出，从而判断一切都正常。

这些例程很简单，只需要很少的时间，因为我们的兴趣是调用的时间，而不是处理。我们已经看到了 C++代码的相关部分，所以让我们看看 C 版本。

### 实施情况

C 实现使用数据结构，需要一些函数。代码是:

```

enum PinType {
	eToggle, eAnalog
};

struct PinOut {
	enum PinType pin_type;
	const unsigned int pin;
};
typedef const struct PinOut* const PinOutPtr;
void toggle_out(const PinOutPtr p);
void analog_out(const PinOutPtr p);

void output_all();
void output_by_func();
void output_pin(const unsigned int i);

```

*引脚排列*结构包含一个标识符， **引脚类型** *，*用于识别输出类型，数字或模拟。它还包含要使用的 pin。调用函数**【toggle _ out()**和 **analog_out()** 来控制 **管脚引出线** 结构指定的管脚，该管脚通过指针传递。其他函数用于列表处理，将在下面讨论。

### 时机

计时过程很简单。 *micros()* 函数用于捕捉每个方法调用前后的时间。这两个时间的区别在于执行操作需要多长时间。每个操作执行 10000 次。仅仅为一个操作计时是不准确的，因为它们太快了。

有两个常规测试。第一个是计时单个输出例程的调用。这提供了每次调用成本的感觉，虽然有趣，但结果有点误导。第二个测试使用上面讨论的数组过程。这是比较现实的结果。

## 计时简单呼叫

调用单个输出函数会执行三个测试。一个测试是调用 C *toggle_out* *()* 。另外两个调用 C++ *数字输出()*使用点符号直接调用和一个通过基类指针变量的虚拟调用。

每个计时循环中的实际调用是:

```

	toggle_out (pin_out_ptr);
	pin13.output();
	pin13_ptr-&gt;output();

```

变量 *pin_out_ptr* 是指向引脚 13 的 C 数据结构的指针。

变量 *pin13* 是 pin13 的 *DigitalOut* 类的一个实例。变量*引脚 13_ptr* 是一个*引脚抽象*指针，包含一个指向*引脚 13* 的指针。

# 行走列表

这个更复杂的测试是多次调用两个输出函数，遍历两个实现的“引脚”数组。C 列表是一个由 **引脚排列** 指针组成的数组。C++版本是指向 **DigtalOut** 和 **AnalogOut** 实例的**PinOutputAbstract**指针数组。每个数组包含十个元素。

### C++实现

C++实现简单，这就是使用继承的好处。C++将细节放在类开发者身上，使类用户的工作更容易。c 在两个角色之间更平均地分配。在小项目中，这没有太大的区别。考虑到今天的开发团队，类开发人员可能和用户在不同的大陆。让它对用户来说更容易有很大的好处。

实现数组传递所要做的只是一个循环，对每个条目虚拟调用 **【输出()** 。我们在上面看到它使用新的 C++11 *范围为*循环。

### 实施情况

C 实现测试了遍历输出设备阵列的两种方式。第一种使用*开关盒*结构来决定输出是模拟还是数字。第二种是给那些有足够经验使用函数指针的人。这避免了以更复杂的实现为代价的决策过程。

C++不需要做出决定，因为它是设备所使用的类所固有的。类似地，对虚函数的调用由编译器处理，因此代码比通过 C 函数指针调用简单。

### 切换案例决策

下面是 **output_all** 的代码，用于遍历数组并调用 **output_pin()** 函数 *:*

```

void output_all() {
	size_t i;
	for (i = 0; i &lt; io_Pins_size; i++) {
		output_pin(i);
	}
}

```

这里是 *output_pin()* ，它包含了*开关盒*语句:

```

void output_pin(const unsigned int i) {

	PinOutPtr p = io_pins[i];

	switch (p-&gt;pin_type) {
	case eToggle:
		toggle_out(p);
		break;

	case eAnalog:
		analog_out(p);
		break;

	default:
		break;
	}
}

```

这很简单。输出的类型从数组条目中获得，并由*开关*用来确定要使用的*情况*。

### 函数指针实现

对于那些有足够经验使用指向函数的指针来解决这个问题的人来说，下面是使用的代码:

```

void output_by_func() {
	size_t i;
	for (i = 0; i &lt; io_Pins_size; i++) { 
                PinOutPtr p = io_pins[i]; 
                func_ptrs[p-&gt;pin_type](p);
		}
}

```

这个版本的优点是只需要一个函数， *func_ptrs()。*这样做的总体缺点是创建指针函数的挑战。

# 结果讨论

下面是计时结果:![comparison table](img/9bab15a6cdb38edd9541f21a5aed907c.png)我使用了与上一篇文章相同的开发环境，如[Code Craft:Using Eclipse For Arduino Development](http://hackaday.com/2015/10/30/code-craft-using-eclipse-for-arduino-development/)所述。表中的时序来自 Arduino Uno R3 和 Due。测试在两个优化级别上进行，以查看它们如何影响结果。该操作系统是 Arduino 的默认操作系统，并针对空间进行了优化。优化 O2 是为了速度，不要进入任何不寻常的技巧。这是 [GCC 文档推荐](https://gcc.gnu.org/onlinedocs/gcc/Optimize-Options.html)用于一般速度优化的级别。想实验的话还有两个更高的层次。我还会提到，当速度优化增加时，内存使用也会增加。这是一个典型的权衡。

对函数的单次调用的结果与预期的一样。Uno 上的虚拟调用整整慢了 0.7 微秒。Due 拥有更快的处理器，因此差异较小。C 函数调用和 C++直接成员调用之间几乎没有区别。从 Os 到 O2 优化的改变确实提高了 Uno 和 Due 的速度，但只是略微提高。

数组处理测试以有趣的方式改变了计时。在 Uno 上，C++虚拟方法调用比*切换用例*和函数指针版本都要快。额外的函数调用和 *switch-case* case 处理让 Uno 付出了代价。Due 的结果在各种情况下差别不大，尤其是速度优化测试。

# 包裹

计时结果没有明显的赢家，因为它们都非常接近。务实一点，用 C 还是 C++都无所谓。这就是这两篇文章的要点:平息 C++比 C++大或慢的争论。c++类不会导致代码膨胀，使用继承和虚函数本身就不会很慢。

要考虑的一个关键点是，你不能总是孤立地看待一个语言特性，就像反对者看待函数调用时所做的那样。需要从更大的角度考虑如何以及为什么使用一种语言特性；你需要看看这种语言所代表的生态系统。你必须解决一个特定的问题，并考虑每种语言的解决方案。即便如此，没有一个比较是完美的。

C++的一个设计目标是根据问题来表达解决方案，而不是用深奥的语言来表达。我们看到的一个例子是，C++将实现细节放入类和继承中，因此它们的使用表达更加清晰。例如，虚函数处理的循环比 C 函数指针的循环更容易阅读。类似地，在 classes 的文章中，使用引用参数调用成员比 C 函数更简洁，在 C 函数中用户必须添加地址操作符。

# 嵌入 C++项目

在 Hackaday.io，我创建了一个嵌入 C++ [项目](https://hackaday.io/project/8238-embedding-c)的 *[。项目将在项目描述中以目录的形式保留这些文章的列表。每篇文章都将有一个项目日志条目用于额外的讨论。感兴趣的人可以更深入地研究主题，提出问题，并分享更多的发现。](https://hackaday.io/project/8238-embedding-c)*

该项目也将作为我或合作者补充材料的地方。例如，有人可能想要获取代码并报告其他 Arduino 板甚至其他嵌入式系统的结果。停下来看看发生了什么事。