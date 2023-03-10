# 直接执行内存块:C 中的函数指针

> 原文：<https://hackaday.com/2018/05/02/directly-executing-chunks-of-memory-function-pointers-in-c/>

在本系列的第一部分中，我们介绍了 C 语言中指针的基础知识，然后在第二部分中介绍了更复杂的 T2 和指针算法。这两次，我们都只关注表示内存中数据的指针。

但是数据并不是唯一存在于内存中的东西。所有的程序代码都可以通过 ram 或其他可执行类型的内存访问，给每个函数一个内存中的特定地址作为入口点。同样，指针只是简单的内存地址，为了充分利用这种相似性，C 提供了函数指针的概念。函数指针为我们提供了使条件代码执行更快的方法，实现回调以使代码更加模块化，甚至为逆向工程或利用提供了进入正在运行的机器代码本身的立足点。所以继续读下去吧！

## 函数指针

一般来说，函数指针并不比数据指针更神秘:主要区别是一个引用变量，另一个引用函数。如果你还记得上次数组*是如何衰减为指向第一个元素的指针的，那么一个函数同样会衰减为指向其入口点地址的指针，而`()`操作符会执行该地址上的任何内容。因此，我们可以声明一个函数指针变量`fptr`，并为其分配一个函数`func()`:`fptr = func;`。调用`fptr();`将解析到函数`func()`的入口点并执行它。*

诚然，将一个函数变成一个变量的想法一开始可能看起来很奇怪，可能需要一些时间来适应，但随着时间的推移，它会变得越来越容易，并且它可能是一个非常有用的习语。函数指针语法也是如此，开始时可能会令人生畏和困惑。但是让我们自己来看看。

### 函数指针语法

如果我们分解一个标准的函数声明，我们有一个*返回类型*，一个*名称*，以及一个可选的*参数列表* : `returntype name(parameters)`。定义一个函数指针是类似的。函数指针的返回类型和参数必须与它所引用的函数相匹配。就像数据指针一样，我们使用星号`*`来声明指针。

有一个条件。如果我们有一个函数`int func(void)`，写`int *fptr(void)`不会给我们一个函数指针，而是另一个函数返回一个整数指针`int *`，因为默认情况下`*`粘在`int`上。圆括号通过将星号与指针名而不是返回类型:`int (*fptr)(void)`分组，将语句变成函数指针声明。

所以大致的模式是:`returntype (*name)(parameters)`。让我们看看几个不同的函数指针声明。

```

// function without parameters returning int, the one we just had
int (*fptr1)(void); // --> int function1(void) { ... }

// function with one int parameter returning int
int (*fptr2)(int);  // --> int function2(int param) { ... }

// function with void * parameters returning char *
char *(*fptr3)(void *); // --> char *function3(void *param) { ... }

// function with fptr1 type function pointer as parameter returning void
void (*fptr4)(int (*)(void)); // --> void function4(int (*param)(void)) { ... }

// function with int parameter returning pointer to a fptr1 type function
int (*(*fptr5)(int))(void); // --> int (*function5(int))(void);

```

显然，语法会变得相当混乱，你可能会浪费时间去理解它。如果你曾经在野外遇到一个指针构造，并且很难弄清楚什么去哪里，那么 *cdecl* 命令行工具会有很大的帮助，[，它也有在线版本](https://cdecl.org/)。

```

cdecl> explain int (*fptr1)(void)
declare fptr1 as pointer to function (void) returning int
cdecl> explain int (*(*fptr5)(int))(void)
declare fptr5 as pointer to function (int) returning pointer to function (void) returning int
cdecl>

```

另一方面，如果你发现自己需要编写一个指针结构，可能需要多次尝试才能正确，那么使用 C 语言的`typedef`操作符可能是一个好主意。

```

// define new type "mytype" as int
typedef mytype int;
mytype x = 123;

// define new type "fptr_t" as pointer to a function without parameters returning int
typedef int (*fptr_t)(void);
fptr_t fptr = function1;
fptr();

// use fptr_t as parameter and return type
void function4(fptr_t param) { ... }
fptr_t function5(void);

```

您可能已经注意到，所有示例在引用函数时都没有使用&符号`&`，在解引用指针以执行其底层函数时也没有使用星号`*`。因为函数隐式地衰减为指针，所以没有必要使用它们，但是我们仍然可以使用它们。注意，函数调用的优先级高于解引用，所以我们需要相应地使用括号。

```

// explicitly referencing with ampersand
fptr_t fptr = &function1;
// explicitly deferencing with asterisk
(*fptr)();
// not *fptr();

```

到底是使用“与”号还是星号是个人喜好的问题。如果你可以自由选择，选择你觉得更自然、更容易阅读和理解的。对于这里的例子，我们将在代码中省略它们，但是我们将添加替代符号作为注释。

## 分配和使用函数指针

现在我们已经看到了如何声明函数指针，是时候实际使用它们了。在指针的真正精神中，我们的第一个用例例子是对[的引用，这是一篇处理带有函数指针](https://hackaday.com/2015/09/04/embed-with-elliot-practical-state-machines/)的状态机实现的文章。它本身就值得一读，尤其是如果你想更多地了解[状态机](https://en.wikipedia.org/wiki/Finite-state_machine)，所以我们不想在这里透露太多。但是概括来说，不是使用一个`switch`语句来确定和处理当前状态，而是状态处理函数自己将下一个状态的处理程序分配给一个函数指针变量。然后程序本身周期性地执行存储在变量中的函数。

```

void (*handler)(void);

void handle_some_state(void) {
    if (condition) {
        handler = handle_some_other_state;
     // handler = &handle_some_other_state;
    }
}

int main(void) {
    while (1) {
        handler();
    // (*handler)();
        ...
    }
    return 0;
}

```

### 函数指针数组

当我们没有一些预定义的或线性的状态转换时，我们可以应用类似的方法，但是例如想要处理随机的用户输入，每个输入调用它自己的处理函数。

```

void handle_input(int input) {
    switch (input) {
        case 0:
            do_something();
            break;
        case 1:
            do_something_else();
            break;
        ...
    }
}

// function that is periodically called from main()
void handler_loop(void) {
    status = read_status_from_somewhere();
    handle_input(status);
}

```

由于函数指针只是变量，我们可以把它们打包成一个数组。就像其他数组一样，括号`[]`直接附加在名称上。

```

// declare array of function pointer of type void func(void)
void(*function_array[])(void) = {
    do_something,      // &do_something,
    do_something_else, // &do_something_else,
    ...
};

```

我们现在可以通过使用`input`作为数组索引来替换前面的`switch`语句:

```

void handle_input(int input) {
    // execute whichever function is at array index "input"
    function_array[input]();
 // (*function_array[input])();
}

```

理论上，这将复杂性从 *O* (n)变为 *O* (1)，并使执行时间更可预测，但在实践中，有太多其他因素，如架构、分支预测和编译器优化权衡在内。在简单的微控制器上，函数指针通常比`if/then`或`case`语句更快。尽管如此，函数指针并不是免费的。每个指针都需要在内存中有一个位置，取消对指针的引用需要复制地址，这增加了一些额外的 CPU 周期。

用函数指针代替`switch`语句的一个更有说服力的理由是增加了灵活性。我们现在可以在运行时设置和替换处理函数，这在我们编写一个库或一些插件框架时特别有用，我们在其中提供主要逻辑，并让用户决定在每个状态/输入/事件等上实际做什么。(在此插入关于净化用户输入的注释。)自然，如果我们处理的状态或输入值是连续顺序的整数，那么使用数组最有意义。在其他情况下，我们可能需要不同的解决方案。

### 作为函数参数的函数指针

假设我们创建了一个向 web 服务器发送 HTTP 请求的库，用户定义的处理程序根据 [HTTP 状态码](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)处理它的响应。以状态码作为数组索引会给我们一个巨大的，大部分是空的数组，浪费了很多内存。在这里，旧的说法会是更好的选择。好吧，与其调整`handle_input()`函数的主体，不如我们把整个东西变成一个函数指针？你刚刚发明了`callback`。

```

// function pointer to the handle function
void (*handle_input_callback)(int);

// function to set our own handler
void set_input_handler(void (*callback)(int)) {
    handle_input_callback = callback;
}

// same handler, just using the function pointer now
void handler_loop(void) {
    status = read_status_from_somewhere();
    if (handle_input_callback != NULL) {
        // execute only if a handler was set
        handle_input_callback(status);
     // (*handle_input_callback)(status);
    }
}

```

在用户定义的代码端，我们将声明自己的处理函数并传递它。

```

void my_input_handler(int status) {
    switch (status) {
        case 200: // OK
            ...
            break;
        case 404: // Not Found
            ...
    }
}

int main(void) {
    set_input_handler(my_input_handler);
 // set_input_handler(&my_input_handler);
    while (1) {
        handler_loop();
        ...
    }
}

```

ESP8266 的非 OS C SDK 是一个为用户定义的行为大量使用回调的真实系统。在 C 标准库的[快速排序](https://en.wikipedia.org/wiki/Qsort)函数`qsort()`中可以找到一个使用函数指针参数来定义函数自身行为的例子，它将比较函数作为参数来确定任何给定数据类型的顺序。

### 作为`struct`成员的函数指针

到目前为止，我们已经了解了指针，函数指针可以是`struct`成员也就不足为奇了，我们可以像其他成员一样声明和使用它们。

```

struct something {
    int regular_member;
    void (*some_handler)(void);
    int (*another_handler)(char *, int);
} foo;

...
    foo.some_handler = some_function;
 // foo.some_handler = &some_function;
    foo.another_handler(buf, size);
 // (*foo.another_handler)(buf, size);
...

```

在插件系统中，或者在硬件相关代码与通用的、硬件无关的逻辑分离的情况下，通常会发现以各种函数指针作为成员的。一个经典的例子是 Linux 设备驱动程序，但是对于初学者来说并不需要那么极端。还记得第一部分中我们将 GPIO 端口定义为指针的过于复杂的 LED 切换示例吗？如果我们对按钮输入使用相同的概念，并添加一些处理函数，我们最终会得到一个完全通用的、独立于硬件的按钮处理框架。

注意，我们也可以将一个`NULL`指针分配给函数指针，执行这样一个函数的结果就像在分段错误中取消对任何其他`NULL`指针的引用一样。但是，如果我们期望它是可能的值，并在执行之前检查它，我们可以使用它来禁用执行，并使处理本身是可选的。

## 转换函数指针

如果函数指针的行为与其他任何指针没有什么不同，我们应该能够随心所欲地将它们转换为其他指针。是的，这在技术上是可能的，编译器不会阻止我们，但是从语言标准的角度来看，执行这样的强制转换函数指针可能会导致未定义的行为。举以下例子:

```

int function(int a, int b) { ... }

void foo(void) {
    // cast function to type "int func(int)"
    int (*fptr)(int) = (int (*)(int)) function;
    fptr(10); // -> function(10, ???);
}

```

虽然从技术上讲这是一种有效的强制转换，但我们最终调用了没有参数值的`function()`。如何处理取决于底层系统及其[调用约定](https://en.wikipedia.org/wiki/Calling_convention)。除非你有充分的理由，否则你可能不想将一个函数强制转换为不匹配的函数指针。不过，好奇心总是一个很好的理由。

### 函数指针和数据指针之间的转换

能不能把函数变成数据或者数据变成函数？当然可以！这样做是黑客的基石之一。正如我们所回忆的，我们需要一个可访问的地址和在该地址上足够的分配内存来成功地处理数据指针。对于一个函数，我们两者都有:函数代码作为分配的内存，函数本身作为地址。如果我们将一个函数指针强制转换为一个`unsigned char`指针，那么取消对指针的引用将为我们提供该函数的编译后的机器码，为逆向工程做好准备。

反过来说，如果指向有效的机器码，我们转换为函数指针的任何数据指针都可以运行。你自己汇编机器码，把它存放在一个变量中，重铸一个指向那个变量的指针，最后运行它，这对于日常使用来说肯定是一件很麻烦的事情。但是，这是通过[注入外壳代码](https://en.wikipedia.org/wiki/Shellcode)来利用安全漏洞的基本方法，并且通常是一种有趣的试验机器代码的方式——也许将来某个时候值得写一篇文章。

## 结束了

虽然指针会带来头痛和挫折，但它们也给我们提供了自由和可能的工作方式，这是其他语言结构很难比拟的。虽然由于现代语言设计“解决”了指针在不小心处理时可能出现的问题，世界可能会变得更加安全，但指针在制作和破坏软件方面总是有其一席之地。