# 阅读不可读的 SROM:psoc 4 内部

> 原文：<https://hackaday.com/2017/03/04/reading-the-unreadable-srom-inside-the-psoc4/>

哇哦。[德米特里·格林伯格]刚刚用赛普拉斯的 PSoC 4 芯片闯入了 SROM。监控只读存储器(SROM)是芯片启动时以特权模式运行的专有代码区域。这正是那种有点令人毛骨悚然的黑匣子，如果黑匣子可以被破解，它对黑客来说是一个非常有用的目标。里面是什么？手册上写着“用户无权阅读或修改 SROM 代码”赛普拉斯以外的人都不知道。直到现在。

这很重要，因为 PSoC 4000 芯片是最便宜的 ARM Cortex-M0 器件之一。因此，它们存在于无数的消费设备中。在[Dmitry]的其他技巧中，他已经找到了如何写入 SROM 的方法，这为在芯片上创建一个无法检测的 rootkit 打开了大门，该 rootkit 会在每次重置时运行。这就是可怕的地方。

酷的部分分散在[Dmitry]冗长而详细的文章中。他还发现，有 8 K 闪存的芯片实际上有 16 K，通过设置单个位可以访问其余的内存。这是因为 flash 是使用 SROM 的例程编写的，而不是我们熟悉的其他微处理器通常的硬件级写入寄存器并等待的过程。当然，因为这都是在软件中完成的，你也可以通过编写错误的校验和来阻塞闪存。[德米特里]做了两次。好在芯片不贵。

[Dmitry]不得不采用的 ROP(面向返回的编程)技巧的本质，以及对系统本身设计的深入研究，都在[Dmitry]的博客上。当他继续摆弄这些筹码时，我们迫不及待地想看看他还会找到什么宝藏。如果你想知道需要什么样的疯狂天才才能实现这一点，那就想想[Dmitry] [在 AVR 上运行 Linux](http://hackaday.com/2012/03/28/building-the-worst-linux-pc-ever/)，[欺骗 nRF24 芯片发送蓝牙 LE 信标](http://hackaday.com/2013/09/21/sending-data-over-bluetooth-low-energy-with-a-cheap-nrf24l01-module/)，[重写了他自己飞机的 GPS](http://hackaday.com/2016/11/23/custom-data-writer-board-for-1996-planes-gps/) 。

[主图像是 PSoC4200 开发套件，而[Dmitry]只使用 4000 和 4100 系列。只是想让你知道。]