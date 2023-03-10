# 开始使用旧熨斗上闪烁的灯

> 原文：<https://hackaday.com/2017/08/10/getting-started-with-blinking-lights-on-old-iron/>

如果你曾经去过计算机历史博物馆，你会被大多数现代计算机看起来是多么乏味而震惊。1980 年以前，计算机有灯和开关，有时还有刻度盘和仪表。有些有类似配电盘的接线板，有些甚至有类似示波器的显示器。一台有着所有开关、灯和显示器的机器让你的黑客们兴奋不已。你想过开始逆向计算吗？很难吗？你需要很多钱吗？那取决于你的目标是什么。

至少有三种方法可以参与逆向计算:你可以出钱购买真正的古董计算机，你可以建造或购买旧计算机，用从零到百分之百真实的部件重建，或者你可以用运行在现代计算机上的模拟器进行实验。作为第二和第三种选择的混合，FPGAs 中也有仿真。

你可以看到，第一种选择可能非常昂贵，你可能需要发展很多修理和修复技能。观看[Mattis Lind] [在上面的剪辑中旋转实际 PDP-8](https://www.youtube.com/watch?v=wM0fbXvmnds) 上的比特是很棒的，但你需要努力做到这一点。假设你已经有了一台个人电脑，这两种不需要原始硬件的技术不会让你倾家荡产，甚至不需要任何成本。

尽管有些人对仿真嗤之以鼻，但对某些机器来说，这几乎是唯一的出路。例如，你买不到原版的 EDSAC。这也是一个很好的开始方式，没有太多的花费和风险。但是不管你怎么做，有一个共同点:你必须知道如何操作这个东西。

## Simh 和 BlinkenBone

模拟旧计算机的一种常见方法是使用 SimH 套件。它可以模拟大量的旧电脑。通常情况下，仿真有一个控制台，您似乎正在向某种终端输入数据。从技术上来说，这很好，但是它没有给你处理旧硬件感觉。

然而，SimH 确实支持一个接口，可以驱动一些机器的真实或模拟的前面板。例如，之前我们介绍过 PiDP-8 套件，它在 Raspberry Pi 上使用 SimH 来驱动看起来相当真实的 PDP-8 前面板。不过，有了 BlinkenBone，你可以为许多经典机器运行 Java 前面板，而且多亏了 SimH，它们不仅仅是模型。他们工作。

[![](img/9e6c2b62ab6248ba9221b25c84756008.png)](https://hackaday.com/wp-content/uploads/2017/07/panel_pdp8i_large.jpg)

因此，让我们看看如何通过前面板操作 PDP-8。来自 DEC 或数字设备公司的 PDP-8 于 1965 年开始使用。一个基本型号要花费 18500 美元——在那个年代是一大笔钱。“直 8”充满了分立元件，大小相当于一台冰箱。我们来看看 PDP-8/I，这是一台在 1968 年左右用集成电路制造的机器。虽然以今天的标准来看它很大，但还没有冰箱大。

为什么是 PDP-8？嗯，有几个原因。首先，PDP-8 非常简单，但却是早期计算机的代表。第二，多亏了 BlinkenBone，你可以在没有任何硬件的情况下玩游戏。如果你有 PiDP-8，那也可以。如果你足够幸运，能够接触到一个真正的 PDP-8，那么你就万事俱备了。

如果你不想看详细的报道，你可能更喜欢看下面的视频。

## PDP-8/I 前面板概览

PDP-8/I 有 26 个开关。还有两个明显的按键开关:一个用于开/关，另一个用于锁定面板(PiDP-8 上没有这两个开关)。从左边开始，你会看到以下开关: [![](img/096024ece13db12b3ff2fd5223f0b614.png)](https://hackaday.com/wp-content/uploads/2017/07/switch1.png)

*   数据字段(3)–设置数据字段(具有用于数据的内存 4K 页面)
*   说明字段(3)–设置说明字段
*   地址/数据开关(12)–设置 12 位地址或 12 位数据字。向上位置为零，最左边的开关为位 0。颜色组对应于[八进制](https://en.wikipedia.org/wiki/Octal)位数。
*   开始–按下运行程序
*   load Add–按下以将交换机上的地址加载为当前地址
*   dep–按 up 将数据开关转移到当前存储位置，并增加当前位置
*   检查–按下以加载当前位置存储内容的灯，并增加当前位置
*   cont–停止后继续(与重新开始的 Start 相反)
*   停止–停止执行
*   sing Step-一个拨动开关，让您一次步进一个机器周期；SimH 不支持这个，PiDP-8 使用这个开关来做一些事情，比如重启底层的 Raspberry Pi
*   sing Inst–另一个拨动开关，通过执行一个指令和暂停来使机器处理启动和继续

你的电脑可能有 10 亿字节的内存被组织成 8 位字节。PDP-8 能够寻址组织为 12 位字的 4K 或 RAM。即使在那个时候，4096 个字的内存也不算多，所以如果你能负担得起额外的内存，数据和指令字段可以让你有多个 4K 字段。

[![](img/9197bdd2637444b5c6662b6a22ebf46b.png)](https://hackaday.com/wp-content/uploads/2017/07/lights.png) 在真正的 PDP-8 上，Dep 是反过来的——你向上推而不是向下推。这是为了防止您在混淆开关的情况下不小心覆盖了内存。默认情况下，PiDP-8 不会反转开关，尽管您可以通过简单的修改来实现。

正如我前面提到的，这些灯——记住，在实际系统中这些不是 led——显示地址和数据。它还显示寄存器。面板右侧框中的灯显示当前指令(第一栏)、当前机器周期(中间栏)和机器状态(右栏)。

## 简单的说明

如果你想知道 PDP-8 如何使用 8 盏灯来显示正在执行的指令，这很简单。只有 8 条指令。如果你习惯了现代电脑，这听起来可能不可思议，但这是真的。一台可以编译 Fortran 程序、运行 Basic 语言并执行许多其他任务的机器只有 8 条指令。多年后精简指令集计算机(RISC)的发明也不过如此。

老实说，8 条指令有点半真半假。有 8 个操作码。其中一个操作码有几个子码(但只有几个)。后来的增强使用 I/O 指令来做事情，进一步增加了指令集。

每个 12 位指令都以一个 3 位操作码开始。你可以做一个逻辑 and，一个有符号的加法，一个增量和跳过零操作。您可以存储累加器(并在进程中清除它)，或者跳转到某个位置或子例程。这些指令中的每一条都允许 7 位地址。您可以设置另一个位来指示内存地址是间接的，并设置另一个位来指示 7 位地址是相对于内存的当前页面或页面 0 的。显然，只有 7 位，指令不能在任何内存位置上操作，所以 0 页是一种在程序的不同区域之间进行通信的方式。

一个操作码包含两组“微码”指令。这些可以做的事情，如清除累加器，反转累加器或增加累加器。指令(OPR 指令)不仅可以做这些事情，它还可以在一条指令中完成其中的任何一项或全部。还有一个定义好的操作顺序，所以你可以做一些事情，比如清除累加器，递增它，把 1 放入寄存器。

没有减法(求反和加法都可以)。没有逻辑或指令(提示:记住德摩根定律)。但是有足够的东西可以让你进行有意义的编程。只是需要大量的说明。

字幕就更多了。自我修改代码很常见，当您将一些内存地址用作间接地址时，它们会神奇地增加。关于 PDP-8 编程的教程本身可以是一整篇文章，但是我想让你感受一下在这样的机器上编程是什么样子的。不同的机器有不同的间接寻址和内存寻址方案，但这些通用原则在这个时代非常普遍。如果你真的想深入研究，你可能比阅读[道格拉斯·w·琼斯的] [参考手册](http://homepage.cs.uiowa.edu/~jones/pdp8/man/index.html)更糟糕。

## 测试程序

用八进制来考虑这个程序:

```
7301     ; load accumulator with 1 and clear link (carry)

7001     ; increment accumulator

7430     ; skip if link=0

7402    ; halt

5001    ; jump to location 1
```

在操作中，这将使累加器和链接位(进位)归零，然后重复地给累加器加 1，直到进位位置位。那么程序将会停止。如果你重新启动它，它将在每次循环时停止，因为当你继续时进位不会被清除。您也可以使用最右边的开关单步执行它。

你怎么能用前面板进入这样的程序？

## 使用前面板

如果你使用的是 Blinkenbone，[转到这个页面](https://github.com/j-hoppe/BlinkenBone/releases)，下载你的操作系统的软件包。您还可以找到关于如何启动模拟器的说明(批处理或脚本文件)。

默认情况下，脚本文件将加载操作系统并运行，但这比我们想要的要高级得多。我们想扳动开关。所以在前面板出现后按停止键(记住，按下)。现在你可以开始拨动开关了。

 [https://www.youtube.com/embed/yUZrn7qTGcs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yUZrn7qTGcs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



1.  向上按下所有 12 个数据/地址开关。按加载地址。注意程序计数器灯全部熄灭。
2.  将数据/地址开关设置为 7301 (DDD UDD UUU UUD，其中 U 向上，D 向下)。
3.  按 Dep(记住，向上按这个开关)。请注意，程序计数器现在是 1，内存地址显示现在是 0，内存缓冲区显示您输入的代码。
4.  对其他指令(7001、7430、7402 和 5001)重复步骤 2 和 3。
5.  将数据/地址开关归零(全部打开)。按加载地址。然后按开始。

[![](img/e76db0983594354bfae1cf0dd396fc0f.png)](https://hackaday.com/wp-content/uploads/2017/07/link.png)

就是这样。您将看到蓄电池闪烁，链接灯将打开。那么处理器将停止。如果你想检查你的程序，重复第 1 步，但重复按下考试，并观察内存缓冲灯。您可能还想重复第 1 步，按下 Sing Inst 按钮，然后重复按 Cont，观看程序一次执行一条指令。

## 正在加载

[![](img/265ae6948cc8a2d9a723e9c311c1bff7.png)](https://hackaday.com/wp-content/uploads/2017/07/rim.png) 在实践中，大多数人从来没有做过你刚才所做的事情。您是否注意到面板左侧标有“Rim Loader”的方框，其中有一些数字？那是第一阶段的装载机。您将切换这些代码(从地址 7756 开始)并运行它。然后，一个更高级的加载器将从其他设备(可能是纸带，但也可能是更有磁性的东西)读取数据。然后，这个加载程序可以读取你想要运行的内容(比如编译器，或者——如果你有一个包含磁盘或磁带的大系统——一个操作系统)。

实际上，如果你真的想这么做，你可以重启 SimH，让它完成所有的工作。PDP-8 的默认播放冒险，如果你启动它，你会看到前面板上的数据显示在你播放时非常好(我假设这是故意的)。

## 后续步骤

了解旧计算机并找到绕过这些旧机器的限制的方法可能会很有趣。别的不说，为 PDP-8 编码会让 PIC 或 AVR 汇编语言看起来很奢侈。SimH 可以模拟许多机器，有些机器有前面板。还有许多闪烁光机器的复制品套件，从假的 Altair 8800s 到 COSMAC Elf 替代品等等。当然，每个前面板都是不同的，但他们确实倾向于分享共同的想法。

你可以争辩说这些旧机器已经没有实用价值了。那可能是真的。但是话说回来，这和有人想要修复一辆旧摩托车，或者建造一艘模型船，人们一直在做的事情没有太大区别。