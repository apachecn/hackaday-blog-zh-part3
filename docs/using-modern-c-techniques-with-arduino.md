# 使用 Arduino 的现代 C++技术

> 原文：<https://hackaday.com/2017/05/05/using-modern-c-techniques-with-arduino/>

在过去的几年里，C++一直在快速地自我更新。从 C++11 的引入开始，这种语言已经向前迈进了一大步，事情已经发生了变化。对于普通 Arduino 用户来说，其中一些是不相关的，也许是大部分，但是这种语言仍然给了我们一些很好的特性，我们可以在编写微控制器时加以利用。

现代 C++允许我们编写更干净、更简洁的代码，并使我们编写的代码更具可重用性。以下是一些使用 C++新特性的技术，它们不会增加内存开销、降低速度或增加大小，因为它们都是由编译器处理的。使用语言的这些特性，您不再需要担心指定 16 位变量、用 NULL 调用错误的函数，或者用初始化来烦扰您的构造函数。旧的方法仍然可用，你仍然可以使用它们，但至少，读完这篇文章后，你会更加意识到新的功能，因为我们开始看到它们在 Arduino 代码中推出。

## 你的整数有多大？

C++11 引入了一系列固定宽度的整数类型别名，它们将给出你想要的位数(8 的倍数)。有签名和未签名的版本。如果你对一个变量使用 int16_t，你知道它是 16 位的，不管哪个 Arduino 是目标。

```

int8_t/uint8_t - a signed/unsigned type that is exactly 8 bits in size.
int16_t/uint16_t - a signed/unsigned type that is exactly 16 bits in size.
int32_t/uint32_t - a signed/unsigned type that is exactly 32 bits in size.
int64_t/uint64_t - a signed/unsigned type that is exactly 64 bits in size.

```

这些是底层类型的别名，所以在 Arduino Uno 上，int8_t 是与 char 相同的类型，uint16 是与 unsigned int 相同的大小。如果你正在编辑一个。cpp '文件，你就得`#include <stdint.h>`，而是在一个。在文件里，你不知道。

## 匿名命名空间

匿名命名空间的概念在 C++中已经存在了一段时间，但它是随着 C++11 的引入而变得突出的。在 C++11 中，匿名命名空间现在是指定只在当前文件中可访问的变量、函数或类的首选方式。它们具有内部联系，而不是外部联系)。这也是合并只需要在当前文件中访问的内容的好方法。匿名命名空间也称为“未命名的命名空间”，因为顾名思义，它们是在没有名称的情况下定义的:

```

namespace {
  ... 
}

```

匿名命名空间取代了静态声明。您可能已经声明为`static`或`const`或编写为`#define`的任何内容现在都可以放入匿名名称空间并具有相同的效果——在内部定义的任何内容都不能在外部访问。命名空间所在的“cpp”文件。但是，在 Arduino IDE 中，如果你添加了一个标签，并给新标签起了一个不以'结尾的名字。cpp '或'。然后文件的扩展名为“. ino”。当您单击“验证”按钮时，所有的。ino '文件被连接成一个单一的。“cpp”文件。这意味着您声明为 static、const 或匿名命名空间中的任何内容都将在每个。ino '文件，因为当它们连接在一起时，它们都以相同的。“cpp”文件。对于小的 Arduino 程序来说，这通常不是问题，但是意识到这一点是有好处的。

好了，现在我们知道了内部和外部链接，以及文件在编译前是如何连接的。这对我们的代码有什么帮助？好了，我们现在知道如何定义变量，这样它们就不会泄漏到它们不应该在的地方。

而不是写:

```

// This should be used sparingly anyway
#define SOME_VAR 1000    
// Static variables declared in a file are local to the file
static int16_t count = 0;    
// const variables declared in a file are local to the file as well
const int16_t numLeds = 4;  

```

你现在可以写:

```
namespace {
  const int16_t SOME_VAR = 1000;  // Now it's type-safe
  int16_t count = 0;  // No need to use static
  const int16_t numLeds = 0;  // Still declared const.

  class thisClassHasACommonName {
    ...
  };
}

```

所有内容都包含在文件开头的匿名命名空间中。如果在不同的文件中定义了另一个 SOME_VAR、count 或 numLeds，编译器不会感到困惑。与静态不同，匿名命名空间中声明的类也是文件的本地类。

## 自动为人民服务

C++11 中添加的 auto 关键字允许您在不知道变量类型的情况下定义变量。但是，一旦定义，就像其他变量一样，它的类型不能改变，就像普通的 C++变量一样。C++编译器使用演绎法计算出变量的类型。

```

auto i = 5;          // i is of type int
auto j = 7.5f;       // j is of type float
auto k = GetResult();  // k is of whatever type GetResult() returns 

```

为了让您指定您想要一个引用，您可以这样做:

```

auto&amp; temp1 = myValue; 
const auto&amp; temp2 = myValue;

```

指针的正确类型也可以推导出来:

```

int myValue = 5; 
auto myValuePtr = &amp;myValue; // myValuePtr is a pointer to an int.

```

Auto 是那些特别长、特别复杂的类型的一个很好的简写。它非常适合定义迭代器实例！

## 使用使用

在 C++中有几种创建别名的方法:低级的(危险的)`#define`和不太危险的`typedef`。使用 typedef 比使用#define 更好，但是他们确实有一些问题。首先是可读性。考虑以下 typedef:

```

typedef void(*fp)(int, const char*);

```

乍一看，特别是如果你不经常使用 C++的话，可能很难确定这是在创建一个别名`fp`，它是一个返回 void 并接受 int 和 string 参数的函数的指针。现在，让我们看看 C++11 的方式:

```

using fp = void(*)(int, const char*);

```

我们现在可以看到 fp 是某个东西的别名，确定它是某个函数指针的别名要容易一点。

第二个区别有点深奥，至少在 Arduino 编程中是这样。Usings 可以被模板化，而 typedefs 不能。

## Nullptr

在 C 和 C++98 中，NULL 实际上被定义为 0。为了向后兼容，C++编译器将允许您使用 0 或 NULL 来初始化指针变量。

但是，当您开始使用 auto 时，您会看到如下代码:

```

auto result = GetResult(...);

if (result == 0) { ... }

```

仅仅从这个看，你无法判断`GetResult`返回的是指针还是整数。然而，即使在那些仍然使用 C 的人中，也没有多少人会检查是否`result == 0`，他们会检查是否`result == NULL`。

```

auto result = GetResult(...);

if (result == NULL) { ... }

```

如果稍后你改变`GetResult`返回一个 int，没有编译器错误——这个语句仍然有效，尽管它看起来仍然应该是一个指针。

C++11 通过引入`nullptr`改变了这一点，它是一个实际的指针类型。现在，你输入:

```

auto result = GetResult(...);

if (result == nullptr) { ... }

```

现在你知道了`GetResult`只能返回一个指针。如果有人在你身上改变了它，那么如果他们没有在你身上改变 if 语句，他们就会得到一个编译错误。`nullptr`的引入也意味着在整型和指针类型上重载方法更安全。例如:

```

void SetValue(int i);     // (1)
void SetValue(Widget* w); // (2)
... 
SetValue(5);    // Calls 1 
SetValue(NULL); // Also calls 1 

```

因为 NULL 不是指针，所以对`SetValue`的第二次调用调用采用整数参数的版本。我们现在可以通过使用`nullptr`正确地调用第二个`SetValue`:

```

SetValue(nullptr);  // Calls 2

```

这就是为什么基于整型参数和指针(指向任何东西)重载函数或方法通常被认为是危险的。现在安全了，但还是不被看好。

## 默认初始化

考虑以下类别:

```

class Foo {
  Foo() : fooString(nullptr) { ... }
  Foo(const char* str) : fooString(nullptr) { ... }
  Foo(const Foo&amp; other) : fooString(nullptr) { ... }
  ...
  private:
    char* fooString;
};

```

我们已经用`nullptr`初始化了所有变量，这很好。如果在这个类中添加了另一个成员变量，我们现在必须在构造函数中再添加三个初始化变量。如果你的类有几个变量，你必须在所有的构造函数中为它们添加初始化器。C++11 给了你用声明内联初始化变量的选项。

```

... 
private:
  char* fooString = nullptr;

```

使用 C++11，我们可以指定一个默认的初始值——如果需要，我们仍然可以在每个构造函数中覆盖它，但是，如果我们不这样做，不管我们添加多少个构造函数，我们只需要在一个地方设置值。如果我们把班级分成。h '文件和 a '。cpp '文件，那么一个额外的好处是，我们只需打开。添加和初始化变量。

## 界定你的枚举

C++试图做的事情之一是允许程序员封装东西，例如，当你命名一个变量时，你不会意外地将你的变量命名为与其他同名的变量相同。C++为您提供了允许您这样做的工具，比如名称空间和类。然而，低级枚举将其条目泄漏到周围的范围中:

```

enum Colour {
  white,
  blue,
  yellow
};
// Doesn't compile.  There's already something in this scope with the name 'white'
auto white = 5;  

```

无法定义变量“white ”,因为“white”是枚举的一部分，而该枚举将其条目泄漏到周围的范围中。C++11 引入了作用域枚举，它允许一些 C++98 不允许的事情。首先，顾名思义，枚举是完全限定范围的。创建限定范围的枚举的方法是使用“class”关键字:

```

enum class Colour {
  white,
  blue,
  yellow
};

auto white = 5; // This now works.

Colour c = white; // Error, nothing in this scope has been defined called white.
Colour c = Colour::white; // Correct.

```

默认情况下，作用域枚举有一个底层类型:int，所以无论平台上的 int 是什么大小，sizeof 都会为枚举返回这个大小。在 C++11 之前，未划分的枚举也有一个底层类型，但编译器试图聪明地处理它，所以它会确定底层类型是什么，而不会告诉我们——它可以优化它的大小，并创建一个最小的底层类型，以适应条目的数量。或者它可以针对速度进行优化，并创建一个对该平台来说最快的类型。这意味着编译器知道枚举是什么类型，但我们不知道，所以我们不能在不同的文件中向前声明枚举。举个例子，

```

file1.h:

enum Colour {
  white,
  blue,
  yellow
};

file2.h:

enum Colour; // Error, in this file, the compiler doesn't know what the type of Colour is.

void SomeFunction(Colour c);

```

唯一的方法是在 header2.h 中使用`#include` header1.h。对于小型项目来说，这很好，但是在较大的项目中，向`Colour`枚举添加一个条目将意味着重新编译任何包含 header1.h 或 header2.h 的内容。限定范围的枚举有一个默认大小:`int`，因此编译器总是知道它们的大小。此外，如果您愿意，还可以更改大小:

```

file1.h:

enum class Colour: std::int8_t {
  white,
  blue,
  yellow
};

file2.h:

enum class Colour: std::int8_t;

void SomeFunction(Colour c);

```

现在，任何包含 file2.h 的文件都不必重新编译(file2.cpp 必须重新编译，因为您必须在其中#include file1.h 才能正确编译它。)

## 最后

在对微控制器进行编程时，您确实可以选择。如果你不想用，就没有理由用这些。然而，我发现它们有助于清理我的代码，并帮助我在编译时而不是运行时捕捉错误。许多只是语法糖，你可能不喜欢这种变化。有些只是细微之处，让在复杂的语言中工作变得更好。是什么阻碍了你尝试它们？