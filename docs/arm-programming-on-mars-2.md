# 火星上的 ARM 编程

> 原文：<https://hackaday.com/2015/09/10/arm-programming-on-mars-2/>

在您对标题反应过度之前，请记住 Eclipse 的最新版本代号为“Mars”建立一个通用的 ARM 工具链总是有点困难。如果你不介意坚持使用一个供应商，花很多钱，或者使用基于网络的工具，那么你可能不会有这个问题。但是把所有的工具放在一起可能会很烦人。

[Erich Styger]与学生一起工作，他知道他们经常在这一步遇到困难，所以他为安装 Eclipse、ARM gcc 编译器和全套工具提供了清晰的文档。他重点介绍了 Windows 和 Kinetis 平台，但不管怎样，步骤实际上是相同的。只需为您的操作系统选择合适的工具，如果您不需要，可以跳过 Kinetis 特有的部分。

我们确实注意到，ARM gcc 包的 PPA(gcc-ARM-none-eabi)没有 Ubuntu Vivid 的包，但由于标准库有最新版本，这不是问题。如果你使用的是 Ubuntu 或者它的衍生软件，你可以像安装其他软件一样安装它。

这是普通的黑客读者无法理解的吗？没有。把所有的链接和说明都放在一个地方会节省很多时间吗？你打赌。

尽管 Eclipse 最初是一个 Java 开发工具，但它足够灵活，可以做任何事情。[甚至调试微控制器](http://hackaday.com/2011/02/24/debugging-msp430-using-eclipse/)。如果你过去在安装 Eclipse 时遇到了麻烦，Mars 版本提供了一个新的、更友好的安装程序(见下面的视频)。

 [https://www.youtube.com/embed/GRKhxroJsS8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GRKhxroJsS8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

