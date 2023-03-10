# 芯片上的反计算机磁盘

> 原文：<https://hackaday.com/2018/03/30/a-retrocomputer-disk-on-a-chip/>

在计算机相对较短的生命周期中，有许多不同的大容量存储方法。磁带、磁鼓、各种各样的磁盘和闪存都有过自己的时代。每一项新的创新都需要一段时间才能变得易于使用。简化闪存使用的早期尝试之一是 M-Systems DiskOnChip 设备。看起来像一个标准的 8K JEDEC 兼容存储设备，它实际上提供了从 16MB 到 1GB 的闪存盘驱动器。[Smbakeryt]购买了一些这样的设备，并建造了一个 ISA 板，为旧的 8 位总线提供磁盘和时钟。您可以在下面看到关于该设备的视频讨论。

SanDisk 收购了 M-Systems，并在 2007 年停产了这些设备。当然，您仍然可以将闪存设计到您的系统中，但 DiskOnChip 的简单高效的界面已经不复存在。这证明了接口的简单性，包括 DS12885 实时时钟在内的小电路板原理图可以放在一页纸上。

DiskOnChip 足够复杂，能够提供正确的 BIOS 签名，因此它自己的 BIOS 被加载到 PC 的加电序列中。当您考虑所涉及的电路有多少时——特别是如果您忽略不属于磁盘子系统的时钟的话——它真的非常优雅。

我们喜欢这些旧的版本，我们怀念你可以不费吹灰之力就把一块板连到你的电脑上的日子。如今，如果你想做一些花哨的 PCI 或 PCI Express 接口，你最好从一个 [FPGA 板](https://hackaday.com/2018/02/17/catching-the-pcie-bus/)开始。或者，你可以[黑掉一个现有的主板](https://hackaday.com/2013/03/02/24-port-gpio-on-a-pci-card/)。

 [https://www.youtube.com/embed/agRE5t24MS4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/agRE5t24MS4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

