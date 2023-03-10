# 如何构建袖珍 MBed 信号发生器

> 原文：<https://hackaday.com/2015/09/15/how-to-build-a-pocket-sized-mbed-signal-generator/>

上个月，[我谈到了如何使用非常便宜的开发板开始使用 mBed 和 ARM 处理器](http://hackaday.com/2015/08/11/getting-started-with-arm-using-mbed/)。不过，我想再次访问 mBed，展示一些更有实质内容的东西。特别是，我经常需要一个简单的便携式波形发生器。它不需要太花哨，也不需要符合我的一些实验室设备的规格，但它应该易于携带，关闭 USB 电源，并在需要时自行工作。

我的要求意味着我需要一个功能稍强的主板。特别是我拿起一个 K64F 板。这非常类似于 KL25Z 板，但有更多的一切-速度，内存等。不过，我真正想要的是 SD 卡插槽。然而，我在 KL25Z 上做了我的早期测试，所以如果你有一个，你仍然可以通过代码工作，尽管独立操作是不可能的。价格从 13 美元涨到 35 美元，但是你可以用这个价格获得更多的功能。

## 项目概述

K64F 板有一个带内置 DAC(数模转换器)的 CPU。输出通过 J4 的引脚 11 输出(在随板提供的引脚输出图上标记为 DAC0_OUT)。与电路板的 USB 串行连接允许您向电路板发送命令和数据。命令非常简单:

*   l–通过串行端口加载十进制文件(16K 个条目，范围从 0 到 65535)
*   x–通过串行端口加载一个十六进制文件(16K 个条目，范围从 0 到 FFFF)
*   f–通过串行端口加载浮点文件(从-1 到 1 的 16K 条目)
*   t–以微秒(浮点)为单位设置时基
*   z-用一个值或两个交替的值替换内存(适合测试)
*   d–显示 SD 卡的目录
*   r–从 SD 卡读取文件
*   w–将文件写入 SD 卡
*   g–生成输出(重置以返回提示)

如果您读取或写入扩展名为. cfg 的文件(实际上，任何以 C 开头的扩展名)，设备将以特殊的文件格式读取或写入数据和时基。任何其他扩展都应该是使用 16 位无符号整数的数据的二进制转储。

当板复位时，它将在 SD 卡的根目录中寻找 autowave.cfg。如果找到了，它会加载并立即执行，除非你在重启时按住 S2 键。如果按钮被按下或文件不在那里，纸板会提示你并等待命令。如果你有一个 autowave.cfg 文件，开发板可以在没有连接到 PC 的情况下工作(只需供电)。

你可以使用 [TTI 的 Wave Manager Plus](http://tti1.co.uk/downloads/waveman-plus.htm) 软件轻松生成有趣的波形。由于有些人不想注册下载该软件，所以也可以使用电子表格或文本编辑器，但手工制作复杂的波形会比较困难。TTI 软件适用于 Windows，但我在 Wine 下运行它没有任何问题(查看下面的视频，了解在此板上使用该软件的完整演示)。

 [![Cardiac waveform made with TTI](img/271e3a568fc46d316ef7f58cd7850828.png "cardiac0")](https://hackaday.com/2015/09/15/how-to-build-a-pocket-sized-mbed-signal-generator/cardiac0/) Cardiac waveform made with TTI [![spacer4x480](img/7c5063f8dc14e84251b9e879d26997dc.png "spacer4x480")](https://hackaday.com/2015/09/15/how-to-build-a-pocket-sized-mbed-signal-generator/spacer4x480/)  [![mBed generated waveform](img/8703bda846876ea5e131537845cc7b73.png "heartcap")](https://hackaday.com/2015/09/15/how-to-build-a-pocket-sized-mbed-signal-generator/heartcap/) mBed generated waveform

例如，左边的图像是用 TTI 软件制作的“心脏”波形。它以 NRM 格式导出，然后用 F 命令读取。右图显示了最终的输出(以及一点上一个波形和一点下一个波形)。一旦加载了波形，明智的做法是将其保存到 SD 卡中，因为这样将来加载会快得多。串行端口只有 57600 波特，有一个很好的数据位可以通过(该程序使用 16 位数据的 16K 缓冲区)。

该项目不需要任何外部硬件，除非您需要对 DAC 输出进行滤波。对于我所需要的，它是完美的方式。使用 G 命令时，电路板会向 DAC 输出一个 16 位值，等待时基中指定的时间，然后移动到下一个值。

 [https://www.youtube.com/embed/vLDp_tFlWL4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vLDp_tFlWL4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 入门指南

如果你以前没有使用过 mBed，你可能想要[重温我们之前的教程](http://hackaday.com/2015/08/11/getting-started-with-arm-using-mbed/)。否则，如果你愿意，可以跳到[在线项目](https://developer.mbed.org/users/wd5gnr/code/HAD_SigGen/)。请注意，该平台是为更大的主板设置的。如果你想使用更小的板，你可能必须减少缓冲区的大小并关闭 SD 卡(所有这些都在 main.h 中完成)。您还必须更改项目以使用您的板，并且可能必须重新校准时基(见下文)。

与我上次展示的 starter 项目不同，这个项目有很多文件。然而，它们中的大多数只包含好的旧 C 或 C++代码。只需要一些 mBed 专用的特殊项目。

## 文件方向

在我们查看 mBed 特定代码之前，让我们大致了解一下程序的布局。有五个 C 文件(及其相关的头文件)。还有两个库:mBed 库和一个用于 SD 卡访问。这个库来自于在 mBed IDE 中搜索导入按钮。

以下是组成该程序的文件:

*   main–一个非常简单的主程序驻留在这里。标头包含一些全局配置数据。
*   CIO——面向字符(串行端口)的 I/O。帮助程序可以读取整数、浮点数等。
*   命令–允许您与程序交互的命令处理器。
*   输出–驱动模拟输出并处理时序。
*   SD card–sd 卡文件系统的简单接口。

虽然文件都以。cpp，我在实际程序中没怎么用 C++(除了 C++注释，可能还有一些默认参数)。不过，我使用的是库提供的 C++对象，让生活变得更容易。

## 图书馆支持

mBed 库负责所有特定于电路板的设置(时钟、电源等)。).它还为数字输入(自动启动覆盖开关)、DAC、串行端口以及我们不使用的板上的许多其他功能提供了 C++对象。

图书馆是经过深思熟虑的。比如串口无非就是这个(在 main.cpp 中):

```
// Serial port
Serial pc(USBTX, USBRX);
```

使用它很简单:

```
 pc.baud(BAUD); // set baudrate
 pc.printf("Hello World\r\n");
```

数字输入也很容易:

```
// Switch to suppress auto loading
DigitalIn NoBoot(SW2);
```

阅读它是轻而易举的事:

```
if (NoBoot==1) auto_open();
```

不出所料，DAC 同样简单:

```
AnalogOut aout(DAC0_OUT); // Analog output
aout.write_u16(buffer[bp]);
```

图书馆唯一的问题是时间。有各种各样的计时机制可用，但没有一个在几十微秒以下具有良好的特性。所以我没有使用库计时组件。

你可能认为 SD 卡访问会很复杂。感谢漂亮的图书馆，它一点也不复杂。有一组常见的函数，如`fopen`、`fclose`、`fread`、`fwrite`等。唯一的问题是知道所有文件似乎都在一个名为/sd 的目录中(您可以更改这个目录)。

以下是 SD 卡访问的设置:

```
SDFileSystem sd(PTE3, PTE1, PTE2, PTE4, "sd"); // MOSI, MISO, SCK, CS
```

就是这样。一旦导入了这个库，屏幕左侧的项目浏览器就会有这个库的文档节点，这样您就可以阅读可用的函数并找到示例代码。虽然`SDFileSystem`对象有很好的文档，但是底层的`FATFileSystem`没有文档节点(但是你可以阅读源代码中的注释)。然而，如示例代码所示，这几乎是标准的 C 文件调用，您几乎可以在任何其他地方使用:

```
// worker for directory listing (call from file prompt too)
uint32_t do_list(const char *fsrc)
{
#if SDCARD==1
 DIR *d = opendir(fsrc);
 struct dirent *p;
 uint32_t counter = 0;

while ((p = readdir(d)) != NULL) {
 counter++;
 printf("%s\r\n", p->d_name);
 }
 closedir(d);
 return counter;
#else
 return 0;
#endif
}
```

所以访问 SD 卡是非常反气候的。你可能认为所有这些占用了大量的程序空间。当然，它确实占用了一些空间，但是根据构建工具，我使用了 1M 闪存中的 42K。所以有足够的空间做更多的事情。

## 驱动输出

我尝试了一些 DDS 风格的输出([Bil Herd]在 DDS 上做了一个很棒的帖子)，但最终决定保持简单。输出模块有两个执行内核。一旦它们中的任何一个开始运行，处理器除了产生输出波形之外什么也不做，直到你复位系统。当其他事情正在进行时，这一方需要考虑输出的时间。一个内核处理时基设置为零的情况(表示 CPU 应该尽可能快地运行)。另一个处理您希望程序从缓冲区输出一个样本，延迟一段时间，然后输出下一个样本的情况。

正如我前面提到的，有一个重要的问题。mBed 库具有非常易于使用的定期和单次定时器。低于某个时间(在 KL25Z 上，该时间约为 26 微秒)时，它们也不会做得很好。mBed 讨论板上有很多关于这个问题的讨论，但最终很难在没有大量抖动的情况下获得非常短的定时器。

由于输出例程独占 CPU，我做了一些改变可编程间隔定时器的实验，您可以在 mBed 中完成:

```
// assume by here the PITs are ours
SIM->SCGC6|=SIM_SCGC6_PIT_MASK;
 PIT->MCR=0;
 PIT->CHANNEL[0].LDVAL=0xFFFFFFFF;
 PIT->CHANNEL[0].TCTRL=PIT_TCTRL_TEN_MASK;
...
 counts=PIT->CHANNEL[0].CVAL;
...
 counts=~counts; // convert to count up
 counts+=110; // how many ticks before we proceed (40nS per + overhead)
 do {
 clock=~PIT->CHANNEL[0].CVAL;
 } while (clock-counts>=0x80000000UL);
 nop(); nop(); nop(); nop(); // fine tune delay
 }

```

最后，我真的不喜欢这种方式。它需要一些调整，也不一定能移植到其他平台。如果这是一个汇编语言程序，我可以计算周期，但我决定采取不同的策略。顺便说一下，你可以非常容易地在 mbed 中嵌入程序集。看到上面代码中的`nop`调用了吗？下面是 output.cpp 中的定义:

```
// inline assembly for nop (plus function call overhead)
void nop(void)
{
 __ASM volatile("nop\n");
}

```

如果需要数字码发生器，也可以将缓冲字发送到输出引脚。唯一的问题是，该板没有 16 针都在一个端口容易访问。mBed 库将允许您写入从不同端口聚合引脚的虚拟端口，但其性能并不好。然而，如果您需要一个模式发生器，其位数不超过属于单个端口的 edge 连接器上的剩余位数，只需简单地更改 output.cpp 即可(即写入端口而不是 DAC)。

## 正时校准

output.cpp 中的 exec 函数本质上是在一个`for`循环中执行一些`nop`调用来获得延迟。这就引出了一个问题:你需要通过多少次循环才能得到一个特定的时间？为了回答这个问题，我添加了一个临时校准模式，并将设备连接到一个示波器上。

默认情况下，每次重启时(没有自动载入的波形时)，内存中会填充两个重复的字:0xAAAA 和 0x5555(顺便说一下，您可以在 command.cpp 中更改这一点)。在校准模式下，您可以将时基设置为某个数值，并测量信号转换一次所需的时间。换句话说，你会得到一个小方波，你需要知道方波的高或低部分执行的时间。尝试几个不同的时基值，并制作一个表格。

| T | 测量时间 |
| one | 0.328 美国 |
| One hundred | 4.67 美元 |
| Two hundred | 8.8 美国 |
| One thousand | 42.4 美国 |

想法是对数据做线性曲线拟合，得出斜率和偏移量(还记得 y=mx+b 吗？)，并将其插入程序中。然后关闭校准，重新编译，就大功告成了。如果没有示波器，很难进行这种校准，尽管如果你有一个低带宽的示波器，你可以使用更大的 T 值来按比例增加时间。

[![fit](img/74e642841c929e56f90f8e5b307198ca.png)](https://hackaday.com/wp-content/uploads/2015/09/fit.png) 如果你不记得如何做线性曲线拟合，并且手边没有计算器，试试[这个很酷的网站](http://mycurvefit.com/)。你可以看到我的部分会话，并读出斜率(23.79)和偏移(-8.98)的权利。请注意，R 等于 1，这意味着曲线拟合良好。如果 R 比 1 小得多，你也许应该仔细检查你的数据以确保它是正确的。

`M`和`B`常量在 output.cpp 中，程序使用它(在非校准模式下)将您的时基(以微秒计)转换成整数计数。它并不总是完美的，但它非常好，编译器中的浮点数学支持使这变得容易。当然，浮点数学在性能方面并不总是好的，但是非整数数学不会出现在关键的计时循环中。

唯一要记住的是，如果 exec 循环发生变化，您需要重新校准。这确实带来了使用在线 IDE 的一个问题。尽管不太可能，重新编译可能会改变 exec 循环，即使您没有接触它。编译器的升级或选项的改变可能在任何时候发生，而你并没有真正意识到。如果你正在运行一个本地编译器(顺便说一下，你可以)，那么你会知道你是否改变了什么，如果这是一个重要的项目，你可以自己对编译器、库和选项进行版本控制。

请记住，时间不会与一些实验室级别的仪器相匹配。如果你想的话，当然可以用一些技巧来减少错误。另一方面，DAC 建立时间意味着无论如何都不会得到超级尖锐的方波。对于该设备的目的，这种定时方案是完全足够的。

## 提示和花絮

如果你使用 Chrome，在 mBed 编辑器中看不清文本，你可能想去 Chrome 商店看看。[MBE ++扩展](https://chrome.google.com/webstore/detail/mbededitor%20%20/liljebdcddbhpligfnecaflbflifhkma?hl=en)允许您设置文本大小。唯一让我感到不安的是，当你选择文本时，它会缩小到正常大小。尽管如此，它使环境变得更加友好。

这实际上不是 mBed 技巧，但是当我谈到 PIT 计时器时，您是否注意到了查看时间周期是否完成的测试？这里有一个用 16 位代替 32 位的释义:

```
unsigned short counts, clock;
counts=get_current_tick()+0x100;  // A
do {
     clock=get_current_tick();
     } while (clock-counts>=0x8000U);
```

如果你以前没有见过，这是一个很好的技巧，它允许你在`clock`大于或等于计数时进行检测，即使时钟已经翻转。换句话说，这处理起始时钟加上偏移(`counts`)不溢出的情况(例如，如果在点 A `current_tick`返回 0x100 并且`counts`变成 0x200)和溢出的情况(例如，如果`current_tick`返回 0xFFF0 并且`counts`变成 0x0f 0)。当然，这是假设您经常查看它，以至于它不能在两次测试之间回绕两次，在这种情况下这不是问题。

## 包裹

这比闪烁 LED 程序(或者改变 LED 颜色，如果你考虑上一篇 mBed 帖子的话)要复杂一些。我想让你体验一下用这些板做一些实际的事情。也许最令人惊奇的部分是它并不那么令人惊奇。有一种感觉是，作为一个例子，Arduino 更容易编程。它很容易编程，主要是因为有许多带有文档和示例代码的库。然而，像 mBed 这样的系统也非常接近拥有良好的库支持。拥有一个 32 位处理器、大容量内存和高时钟速度也让生活变得更加简单。

你可能还会说 Arduino 有这么多子板(说 shields 让我很痛苦)。然而，许多 mBed 板(包括我在本文中提到的所有板)都有可以处理许多屏蔽的插座(记住，这些是 3.3V 板，因此要相应地规划)。

不是要抨击 Arduino。然而，在我看来，随着更强大的处理器、良好的库支持、简单的 IDE(以及升级路径，如果我想要更复杂的东西，如 Eclipse 和调试),这些板和芯片将继续侵犯 Arduino 的地盘。

在上一个帖子和这个帖子之间，你没有太多的借口不去尝试。没有要安装的软件。如果你已经有一个 USB 转串行适配器，LPC1114 将适合一个试验板，而且非常便宜。本项目中提到的飞思卡尔主板起价不到 20 美元。没有什么能阻止你进行 32 位开发。

顺便说一下，如果你决定尝试这个项目，并且你想要一些现成的数据文件放在你的 SD 卡上，你可以从我的 [Google drive](https://drive.google.com/folderview?id=0B47hz_z-oETZM1JlNHlmZ2xYZFk&usp=sharing) 中得到它们。