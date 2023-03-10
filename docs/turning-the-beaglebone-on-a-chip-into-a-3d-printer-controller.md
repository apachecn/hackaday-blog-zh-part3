# 将芯片上的喙骨变成 3D 打印机控制器

> 原文：<https://hackaday.com/2018/03/25/turning-the-beaglebone-on-a-chip-into-a-3d-printer-controller/>

众所周知，3D 打印机和 CNC 机器需要控制电机，但有一些其他的细节总是好的。如果控制器板运行 Linux，支持漂亮的显示器，并有某种网络，那就太好了。实现这一目标的通常方式要么是从桌面上驱动数控机床，要么是在 3D 打印机上添加一个 Raspberry Pi。

这个问题的最佳解决方案是从一个小猎犬骨驱动一切。这将会给你 Linux，通过几个马达驱动器，你可以访问 BeagleBone 中的花式 PRUs，给你快速精确的控制。在过去的几年里，[replica PE](https://www.thing-printer.com/product/replicape/)已经成为你需要将一个小猎犬骨插入几个马达的电路板。现在，有一个更好、更便宜的解决方案。在本周末的中西部 RepRap Festival 上，[Elias Bakken]推出了 Revolve，这是一款将 Octavo Systems 的 OSD 3358“beagle bone On A Chip”与 Trinamic 的静音 TMC2130 电机驱动器相结合的单板。这是一个运行 Linux 的一体化 3D 打印机控制器板。

 [![Trinamic drivers](img/df3c2e071eba9d507efa5d453c3eb824.png "trina")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/trina.jpg?ssl=1) Trinamic drivers [![2](img/b1e1a72ef35c48cebb5688705f77b600.png "2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/2.jpg?ssl=1)  [![1](img/a2572b381694d54b566449bd0f4c66b8.png "1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/1.jpg?ssl=1)  [![Thmb](img/a672ede5f9065bbbcc5f8d682cb990c7.png "Thmb")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/thmb.jpg?ssl=1)  [![ha](img/fb085aa2ccbc7b7a9e45a1e6728277c5.png "ha")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/03/ha.jpg?ssl=1) 

Revolve 的规格或多或少与你对带有 3D 打印机控制器的比格犬骨的预期相符。主芯片是 Octavo Systems OSB3358，有六个来自 Trinamic 的 TMC2130 步进驱动器直接连接到 PRUs，4gb eMMC，4 个 USB 主机端口，10/100 以太网，1080p HDMI 输出，以及足够用于所有怪异和精彩的 3D 打印机的接头。该软件基于[redempt](https://github.com/intelligent-agent/redeem)，这是一个简单地将 g 代码转换为旋转电机和开关 MOSFETs 的守护程序。

价格尚未确定，但[埃利亚斯]预计它会在 100 美元以上，略低于 150 美元。对于一个能有效完成从在线打印机监控到实时运动控制等一切工作的主板来说，这已经不错了。该板的发布日期尚未确定，但正如大多数涉及 3D 打印机的事情一样，检查更新的最佳地点是 Google+ 。