# 苹果 Pippin 的软驱

> 原文：<https://hackaday.com/2017/09/04/a-floppy-drive-for-apples-pippin/>

Pippin 是苹果第一次也是最后一次涉足游戏主机。本质上，Pippin 是一个奇怪的“多媒体设备”,配有一张 CD-ROM，可以上网，几个简洁的控制器，以及一个非常简单的 PowerPC Macintosh 的内部结构。想象一下 3DO 和网络电视的结合，你就会明白苹果试图在这里建立什么。

Pippin 是稀有的，这意味着从磁光驱动器到软盘驱动器的相关配件难以获得。现在，这些外围设备中的一个不再罕见；[ [Pierre]已经克隆了(无源)PCB](http://www.journaldulapin.com/2017/09/03/a-floppy-drive-for-the-bandai-pippin/) ，它允许 Macintosh 软盘驱动器直接插入 Pippin。

Pippin 的扩展功能被锁定在位于机顶盒底部的 PCI 连接器中。官方软驱配件注塑外壳，标准 Mac 软驱，PCB。在找到这些罕见的软盘驱动器配件之一后，[Pierre]简单地用一个仪表测量了所有引脚，描绘出电路，并制作了一端带有 PCI 连接器、另一端带有 20 引脚连接器的 PCB。PCB [在 OSH Park](https://oshpark.com/shared_projects/gnwbibrT) 上共享，如果你想看看这个。

尽管重建这个硬件相对容易，但测试却不容易。第一次测试使用的是软驱 Emu T1，这是一种简洁的设备，可以让旧 MAC 从 SD 卡上读取磁盘映像。这工作得很好，但是用一个真正的软盘驱动器来测试就不行了。有些磁盘根本就不能用，尽管[Pierre]认为这是 USB 软驱和运行 Sierra 的 Mac 电脑的问题。