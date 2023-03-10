# 与 PocketBeagle 一起动手

> 原文：<https://hackaday.com/2017/12/07/hands-on-with-pocketbeagle/>

[Ken Shirriff]对 Hackaday 的页面并不陌生。他的博客帖子总是很有趣，最近一篇谈论[袖珍猎犬](http://www.righto.com/2017/12/hands-on-with-pocketbeagle-tiny-25.html)的帖子也不例外。如果你年纪够大了，还记得 Unix 工作站花了你几万美元的日子，你会情不自禁地惊叹于一台 Linux 计算机，它有 45 个 I/O 引脚、8 个模拟输入、512M 内存和 1 GHz 时钟，放在你的口袋里，售价 25 美元。此外，该板的 CPU 有两个 200 MHz 的板载辅助 CPU 来处理 I/O，而不必担心 Linux 开销。

这些最后的部分是重要的，尽管比格犬已经有这个功能很多年了([Ken] [之前谈到过](http://www.righto.com/2016/09/how-to-run-c-programs-on-beaglebones.html))，但是使用这些从处理器的访问和通信方法已经变得更容易了。[Ken]展示了一小段 C 代码，不管 Linux 操作系统在做什么，它都会输出一个 40 MHz 的方波。这样，您可以将 Linux 用于应用程序中不太重要的部分，并使用从处理器来处理实时处理。

从机的代码也很容易理解，因为你是用 c 语言编写的。下面是方波代码:

```
void main(void)
{
 while (1) {
 __R30 = __R30 | (1<<1); // Turn on output 1
 __delay_cycles(1);
 __R30 = __R30 & ~(1<<1); // Turn off output 1
 __delay_cycles(1);
 }
}
```

与它的大兄弟不同，PocketBeagle 没有网络端口和视频输出。但是，当插入 USB 时，它会显示一个 IP 地址，通过该地址您可以访问 shell。您还可以使用板载串行端口，甚至插入有线或无线的 USB 网卡。

很容易想象，我们将会看到大量的小型串行协议分析器和示波器，它们将与这些设备一起安装在一个钥匙链上。我们[最近亲自](https://hackaday.com/2017/09/23/the-tiny-25-pocketbone/)看了一下设备。如果小而便宜不是你的东西，不要绝望。总是有 [X15](https://hackaday.com/2015/10/07/new-part-day-the-beagleboard-gets-bigger/) 。