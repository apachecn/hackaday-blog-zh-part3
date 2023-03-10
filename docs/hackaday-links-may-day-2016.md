# 黑客日链接:2016 年五一

> 原文：<https://hackaday.com/2016/05/01/hackaday-links-may-day-2016/>

Humble Bundle 是填充您的 Steam 库的一个很好的方式——只需支付您想要的，并获得一些独立视频游戏。这个不起眼的包比电子游戏多得多，因为没有淀粉出版社[只是贴了一捆关于黑客的书](https://www.humblebundle.com/books/no-starch-hacking-books)。不，没有关于戴巴拉克拉法帽和单手使用笔记本电脑的书。我还没写那本书。这个包里有一些精选的书籍，包括[邦尼]的*黑掉 Xbox* 、*用 Python 自动化枯燥的东西、*和*实用的恶意软件分析。*

Raspberry Pi 摄像头——25 美元的附加网络摄像头，直接插入 Pi——[正在升级](https://www.raspberrypi.org/blog/new-8-megapixel-camera-board-sale-25/)。最初的相机是一个 500 万像素的传感器，于 2014 年底停产。Raspberry Pi 基金会买了很多股票，但最终会有替代品。新传感器是索尼 IMX219 万像素的交易，价格相同。我们假设没有红外过滤器的黑色版本将很快发布。

这里有一个小小的硬件回顾，不太值得一个完整的帖子。Raspberry Pi Zero 很棒，一旦产量再次上升，库存进入仓库，它会变得更好。Zero 的一个问题是缺乏 USB 端口，导致[至少有两篇黑客帖子](http://hackaday.com/2015/12/19/yet-another-pi-zero-usb-hub/)标题完全相同，[又一个 Pi Zero USB 集线器](http://hackaday.com/2015/12/30/yet-another-pi-zero-usb-hub-2/)。显然，易于使用的零 USB 集线器是有市场的，而[这家公司正在加紧](http://makerspot.com/stackable-usb-hub-for-raspberry-pi-zero/)来满足这一需求。这里的杀手锏是使用弹簧针接入 Pi Zero 底部的 USB 差分线路、电源和接地焊盘。USB 集线器基于流行的 FE 1.1 4 端口 USB 集线器控制器，为 Pi Zero 提供了四个 USB 2.0 端口。有用吗？是的，而且只要 10 美元。一个非常漂亮的小装置，当圆周率为零时，它将非常有用。

 [![DSC_0194](img/ef661cfdcc5b45458e9da65fb0f757fb.png "DSC_0194")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/04/dsc_0194.jpg?ssl=1)  [![DSC_0192](img/c230ddf0cb66be589281251d0850106d.png "DSC_0192")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/04/dsc_0192.jpg?ssl=1) 

它于 2014 年宣布，2015 年发布，但 STM32F7 并没有看到围绕这些部件的很多行动。遗憾的是，这是对著名的强大的 STM32F4 微控制器的升级，它已经能够通过 VGA 驱动高分辨率显示器[，作为 96 福特 Aspire](https://hackaday.com/2015/06/07/better-vga-on-the-stm32f4/) 的发动机控制单元[，以及作为非常复杂的无刷电机驱动器](https://hackaday.com/2014/01/01/building-an-engine-control-unit-with-the-stm32f4/)[。STM32F7 可以做所有这些甚至更多，现在 ST 正在 F7 的探索板上降价。如果你正在寻找一个大功率的 ARM 微处理器，并且不需要运行 Linux，你不会在其他地方做得更好。](https://hackaday.com/2016/02/04/adding-position-control-to-an-open-source-brushless-motor-driver/)

需要回流电路板，但没有烤面包机烤箱？使用喷灯！通过将 MAPP 喷灯举到离电路板一英尺远的地方，[whitequark]能够成功地回流一个大型降压转换器。有很多水蒸气会凝结在板上，所以之后好好清洗一下是个好主意。

几周前，[雷米尔先生] [造了一个 360 度全金属铰链](http://hackaday.com/2016/04/17/designing-a-360-degree-all-metal-hinge/)。从那以后，他一直在做一些更危险的事情:[制造成堆的迷你台锯](http://www.mrlemieux.com/the-ringinator-table-saw/)。小型台锯对模型、模型等很有用。[雷米尔先生]的台锯是一块数控铝，有一个轴承和锯轴连接到电钻。你说危险？不能和竞争对手相比。[看我花过的最差的四十块钱](http://www.harborfreight.com/4-in-mighty-mite-table-saw-with-blade-61608.html)。这个恐怖货运迷你台锯是迄今为止我用过的最糟糕的工具。床被涂上了五颜六色的油漆，不平整，刀片*没有*调整到 90 度，整件事的动力不足令人毛骨悚然。相信我说的数控电钻版更安全。