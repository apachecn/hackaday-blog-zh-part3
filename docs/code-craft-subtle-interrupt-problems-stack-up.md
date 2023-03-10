# 代码工艺:微妙的中断问题叠加在一起

> 原文：<https://hackaday.com/2015/10/09/code-craft-subtle-interrupt-problems-stack-up/>

【埃利奥特·威廉姆斯’】专栏， *Embed with Elliot，*刚刚做了一个很棒的关于中断的系列。它分为三部分，阐述了在嵌入式系统中使用中断的[好](http://hackaday.com/2015/09/18/embed-with-elliot-interrupts-the-good/)、[坏](http://hackaday.com/2015/09/25/embed-with-elliot-interrupts-the-bad/)和[丑](http://hackaday.com/2015/10/02/embed-with-elliot-interrupts-the-ugly/)。读着读着就有不少回忆飘过。有些相当痛苦，因为调试中断问题可能是一场噩梦。

这些年来，我学会了警惕基于堆栈的语言的微妙之处，比如 C/C++，这可能会让粗心的人上当。这个问题与中断处理期间堆栈上值数组的损坏有关。此问题的修复指出了另一个经常被黑帽用来获取系统访问权的问题。

如今几乎所有受黑客欢迎的处理器都使用一个*栈*。想象一堆盘子。你可以把最上面的盘子拿走。你可以把一些盘子放回栈顶。你不能从中间或底部添加或移除盘子。处理器中的堆栈也以同样的方式工作。你可以*将*数据推送到堆栈上，而你*弹出*数据来取走它。但是就像盘子一样，你不能从中间拿走东西。

## 堆栈的基础

由于一些奇怪的历史原因，在图表中，堆栈总是向下生长，所以顶部是底部。我想是某个硬件人员干的。实际上，这是因为堆栈从较高的内存地址开始，并向较低的内存地址增长。
[![abcd stack diagram](img/15d288608b55609a886a395a3cf48847.png)](https://hackaday.com/wp-content/uploads/2015/09/abcd-stack-diagram3.jpg) 这个图应该有助于解释堆栈是如何工作的。堆栈上的操作显示在顶行，每一列都是变化的堆栈。例如，第一个动作是将 D 和 E 压入堆栈，第二个动作是从堆栈中弹出一个项目。

一个 CPU 有多个寄存器。这里引入的两个是*堆栈指针(SP)* 和*程序计数器(PC)* 。SP 总是指向堆栈的顶部。如果有东西被压入堆栈，SP 就会降低。(请记住，它是朝着内存地址越低的方向增长的)。如果弹出一个项目，SP 会增加。SP 的更改量取决于推入堆栈的数据大小。

PC 指向正在执行的代码。当指令被执行时，PC 从一个步进到另一个。当一个函数被调用时，指令将 PC 的内容推送到堆栈上。然后，该指令将被调用函数的第一条指令的地址加载到 PC 中。执行的第一个代码序列执行一些内务处理，并调整 SP 以为被调用函数的局部变量留出空间。

在返回指令中，内务处理被撤消，SP 被移动到存储返回地址的位置。地址被弹出到 PC，调用函数继续执行。

考虑两个函数，一个将数据添加到缓冲区数组，另一个调用第一个函数，但它本身会被中断(在本例中显示为注释)。

```

char* putInBuffer(...params...) {
   char local_buf[25];
   ... code to put something in local_buf ...
   return local_buf;
}

void callingFunc(...params...) {
   ...some code...
   char* buffer = putInBuffer(....params...);
   // note: an interrupt is going to occur right here
   ... code that does something with buffer ...
}

```

以下是详细情况:

1.  当 *callingFunc* 调用 *putInBuffer* 时，该调用的位置被从 PC 中取出并推送到堆栈中。SP 已调整。
2.  在堆栈上分配 *local_buf* 的空间，即分配 25 个字节。SP 会进行调整以留出该空间。
3.  *putInBuffer* 代码将某个东西放入 *local_buf* 中。![stack pointer diagram](img/c880ad309f3265e10980ea72ede9fff5.png)
4.  在返回时，指向 *local_buf* 的指针被传回给 *callingFunc。*在这里，细节并不重要。
5.  SP 被调整为指向返回地址。
6.  返回地址从堆栈中弹出到 PC 中。
7.  在 *callingFunc 中继续执行。*
8.  稍后*调用函数*使用由*缓冲区*指向的数据。

考虑 SP 指向哪里。它指向存放电脑的地址上方。这意味着*缓冲区*中的指针指向堆栈顶部以外的地址。

当中断发生时:

1.  PC 计数器被推送到堆栈上。
2.  CPU 中的许多其他寄存器被压入堆栈。
3.  PC 变为指向中断代码。
4.  中断代码执行并返回。
5.  CPU 寄存器被恢复。
6.  电脑计数器已恢复。
7.  SP 回到它开始的地方，并在*调用 Func* *中继续处理。*

假设中断发生在我在 *callingFunc 中标记它的地方。*

*在* local_buf *里的数据怎么了？*

### 一次中断吃掉了我的数据

*local_buf* 中的数据被中断堆栈操作破坏。这发生在*呼叫 Func* 使用它之前。我说过了，很微妙。我已经多次看到没有经验和有经验的开发人员陷入这个陷阱。

发现这个错误尤其棘手，因为在返回非指针值时，您可以侥幸逃脱。如果您返回一个整数或浮点值，它实际上被放入在 *callingFunc* 中分配的存储中。在这种情况下，堆栈中的![interrupt stack pointer diagram](img/5d4e66f8e4b492153c16ebd16c9fbe15.png)会发生什么并不重要。真正令人讨厌的是，代码在大多数情况下都能正常工作。像这样的间歇性错误需要进行艰苦的分析才能发现。我见过一个有这个问题的函数被一个开发者重写了五次来修复 bug。他从来没有发现这个问题，直到我，在看了很多次后，我不愿意承认，能够指出来。

或许可以通过将 *local_buf* 设为静态变量来保存函数 *putInBuffer* 。静态局部变量不是保存在堆栈中，而是保存在全局内存空间中(如果你想了解更多，这里有[关于*静态*关键字](http://hackaday.com/2015/08/04/embed-with-elliot-the-static-keyword-you-dont-fully-understand/)的帖子)。这也意味着前一次调用的数据仍然在变量中。有时这是一种可以接受的方法。看起来是这样的:

```

char* putInBuffer(...params...) {
   static char local_buf[25];
   ... code to put something in local_buf ...
   return local_buf;
}

void callingFunc(...params...) {
   ...some code...
   char* buffer = putInBuffer(....params...);
   // note: an interrupt is going to occur right here
   ... code that does something with buffer ...
}

```

### 可重入函数

我说*可能*使用*静态*来修复函数，因为这样做*输入缓冲*不再是*重入*。可重入函数是可以同时或递归调用的函数。同时调用需要使用多线程的多任务操作系统。在这种情况下，线程 R 可以调用该函数，被换出，然后线程 S 也调用该函数。这两个线程中的一个会得到错误的数据，因为它存储在全局内存空间中。

递归呢？这是什么？老的编程笑话是*递归:参见递归。*递归是指一个例程调用自己。有几类问题的递归解法更容易。在这种情况下，如果一个名为*的递归函数放入 Buffer* ，然后在使用数据之前调用它自己，那么数据将会被弄乱。

真正的解决方案是改变 *putInBuffer* ，以便调用程序提供缓冲区*和缓冲区的大小*。缓冲区大小对于避免另一个问题至关重要:缓冲区溢出漏洞。这是一个用来危害系统的黑帽黑客。传递给函数的缓冲区必须是固定长度的。该函数必须确保任何输入数据都不会超出缓冲区的末尾。在最好的情况下，这只会导致您的系统崩溃。最坏的情况是，它为黑帽提供了引入恶意代码的途径。下面是编写这个例程的最好方法。

```

char* putInBuffer(char* buffer, const int buf_size, ...params...) {
   if (buf_size &lt; ...whatever the output size is going to be...) {
      return null;   // or another value callers will understand
   }
   // doesn't matter if interrupt is called here
   ... code to put something in buffer ...
   return buffer;
}

void callingFunc(...params...) {
   ...some code...
   char buffer[20];
   putInBuffer(buffer, sizeof(buffer), ....params...);
   // note: an interrupt is going to occur right here
   ... code that does something with buffer ...
}

```

将指针返回到缓冲区对调用例程来说很方便。这允许被调用的例程在其他函数调用中用作参数。一种典型的情况是将数值转换成文本。

与堆栈相关的问题存在于 C/C++和任何基于堆栈的语言的一个肮脏的小角落，这可能会导致几个小时的烦恼。你可以明白我为什么秃头了。