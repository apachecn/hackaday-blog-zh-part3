# TMS9900 复古版

> 原文：<https://hackaday.com/2017/06/30/tms9900-retro-build/>

[Robert Baruch]在一家旧货商店发现了一个 1983 年的 TMS9900 CPU。如果这个名字听起来不耳熟，TMS9900 是德州仪器早期的 16 位 CPU。他发现，与现代 CPU 不同，该芯片采用几种电压和一个四相 12 伏时钟。他决定启动它——当然——一件事接着一件事，他在试验板上完成了一个系统。你可以在下面看到他制作的一个关于这台机器的视频。

这种 CPU 有一些奇怪的功能，最明显的是它将寄存器存储在片外存储器中，并可以通过改变寄存器的位置来切换上下文。当内存和 CPU 的速度相似时，这是一个新颖的想法。在现代计算机中，内存比 CPU 慢得多，这将是程序执行的主要瓶颈。唯一的板载寄存器是程序计数器、状态寄存器和指向内存中通用寄存器的指针。

[Robert]还没有一个完整的系统，但我们打赌他会成功的。他构建了一个四位数显示器，并对处理器进行了一些简单的控制线解码。他可以监视地址总线，也可以单步执行。TMS9900 使用动态逻辑，所以你不能停止时钟。然而，有一种方法可以用一些触发器和一个 ATmega 处理器构建的状态机[Robert]来实现。

为了克服快速存储器的问题，TI 公司的 TI-99/4 家用计算机只有 128 字可直接寻址的存储器。主程序存储器是更便宜、更慢的动态 RAM (16 K 字节)，只能通过显示控制器访问。这意味着性能受到影响。如果你有可选的软驱控制器，你会得到额外的内存，但那在当时是很贵的。

我们最近看到一辆 TI 99/4A 作为气象站提供[服务。如果[罗伯特]复制 TI-99/4 显示系统，也许他可以运行](https://hackaday.com/2017/04/30/ti-994a-weather-station/)[这个演示](https://hackaday.com/2017/01/30/dont-mess-with-texas-the-ti-994a-megademo/)。我们正等着看[罗伯特]从这里把他的剩余库存带往何处。

 [https://www.youtube.com/embed/DKWfEI18j_k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DKWfEI18j_k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

