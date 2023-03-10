# 学习 20 世纪 40 年代的 FPGA 编程

> 原文：<https://hackaday.com/2017/10/05/learn-fpga-programming-from-the-1940s/>

我们经常认为没有足够多的人在用 FPGAs 做东西。我们也喜欢旧电脑硬件上的复古帖子。所以很难拒绝[karlwood ward]关于[芯片黑客 EDSAC 挑战赛](https://www.rs-online.com/designspark/a-gentle-introduction-to-fpga-programming)的帖子——这是 2017 年呼啸字节节的一部分。

如果你将计算机定义为我们今天所认为的计算机，你可能会认为 EDSAC 是第一台可以运行的计算机。[莫里斯·威尔克斯]和他的团队发明了很多我们今天认为理所当然的东西，包括子程序(惠勒跳跃以一个研究生的名字命名)。

EDSAC 挑战赛的目的是让人们用 FPGAs 进行设计，特别是使用 Verilog 硬件描述语言(HDL)。如果你想跟进或运行你自己的芯片黑客，在网上可以找到[资料](http://chiphack.org/)。在下面的视频中，您可以看到 FPGA 驱动磁带打孔机来制作纪念磁带。

有些练习非常简单，如果你刚开始做，那就再好不过了。这个挑战使用了一个配有 Lattice ice40 FPGA 的开发板和我们之前介绍过的 Lattice 的[开源工具链。事实上，我们甚至在同一个基本设备(但不是同一块板)上完成了](https://hackaday.com/2015/03/29/reverse-engineering-lattices-ice40-fpga-bitstream/)[我们自己的教程](https://hackaday.com/2015/08/19/learning-verilog-on-a-25-fpga-part-i/)。我们的[最终项目生成了 PWM](https://hackaday.com/2015/12/16/taking-the-pulse-width-modulation-of-an-fpga/) ，而不是纸带。

说真的，EDSAC 棒极了。执行单元是串行的，通过水银延迟线一次处理一个比特。这里有相当多的文档，甚至还有一些模拟器，所以如果你想接触一台旧电脑，这是一个不错的尝试。

 [https://www.youtube.com/embed/QEKnrO0ne7M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QEKnrO0ne7M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

