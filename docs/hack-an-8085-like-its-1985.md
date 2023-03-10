# 像 1985 年一样黑 8085

> 原文：<https://hackaday.com/2016/10/01/hack-an-8085-like-its-1985/>

如果你已经做了几十年的电子硬件，你还有遥远过去的项目吗？它们有用吗？也许是音频放大器，或者是台式电源。

[Just4Fun]在 20 世纪 80 年代让[成为了一台相当特别的电脑](https://hackaday.io/project/14881-back-from-the-80s-homemade-8085-cpu-board)，现在它肯定还在工作。然而，把它描述为“一台带有 EPROM 仿真器的 8085 单板计算机”并不能表达它有多么特别。这不是现代意义上的带有 SoC 和一些支持组件的单板计算机。相反，它是一个完整的系统，其中处理器、内存和外围设备都是由 74 系列粘合逻辑包围的独立组件。整个系统用电线包裹在一块 perfboard 上，非常整齐地安装在机架中。EPROM 仿真器是控制台中的一个独立单元，带有十六进制键盘和 7 段显示器。

正如 LED 闪烁演示的视频所示，EPROM 仿真器允许 8085 机器代码逐字节输入，而不是必须刻录到真正的 EPROM 中。

[Just4Fun]让我们有计划用一种现代的替代品来取代那个时期的 EPROM 仿真器，这是一种 PCB 上的 EEPROM，旨在适合最初的 EPROM 插座库。在这一点上，他建议他可以安装一个引导程序和一个基本的解释器，这在传统的 EPROMs 中是完全可能的，但是可能没有这么便宜。

 [https://www.youtube.com/embed/B5aSE_ckf1M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B5aSE_ckf1M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果 8085 激起了你的兴趣，你可能想了解一下它的算术逻辑单元的结构，以及 T2 的寄存器。如果你想尝试自己制作一台 8 位计算机，我们最近评论了[RC 2014，一台 Z80 机器](http://hackaday.com/2016/09/08/review-the-rc2014-z80-computer/)。