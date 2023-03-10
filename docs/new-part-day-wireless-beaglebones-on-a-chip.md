# 新零件日:芯片上的无线小猎犬骨

> 原文：<https://hackaday.com/2016/09/27/new-part-day-wireless-beaglebones-on-a-chip/>

BeagleBone 是一款非常受欢迎的单板计算机，最适合需要快速闪烁 led 的实时应用。多年来，BeagleBone 一直用于独立的 CNC 控制器，这是非常大的 LED 装置背后的大脑，在极少数情况下用于驱动 CRT。如果你只是想要一个小的 Linux 主板，那就买一个 Pi 吧。如果你想用硬件做一些有趣的事情，买一个猎兔犬骨。

BeagleBone 生态系统在去年增长了很多，从配备无线和 Grove 连接器的 [BeagleBone Green](http://hackaday.com/2016/05/21/beaglebone-green-now-wireless/) ，专注于机器人技术的 [BeagleBone Blue](http://hackaday.com/2016/01/11/introducing-the-beaglebone-blue/) ，受《超级名模》启发的 [Blue Steel](http://hackaday.com/2014/06/19/beaglebone-blacks-still-not-available-heres-blue-steel/) 。现在有一个新的 BeagleBone，围绕今年早些时候推出的一个非常有趣的模块系统构建。

这款新主板名为 [BeagleBone Black Wireless](https://beagleboard.org/blog/2016-09-26-meet-beaglebone-black-wireless/) ，它将你对 BeagleBone 的所有了解和喜爱带到了桌面上。有一个 1GHz ARM355x，带有两个 32 位 200MHz PRUs，用于实时引脚切换。RAM 设置为 512MB，预装了 4GB 的 eMMC 闪存和 Debian，以及一个 microSD 卡，用于更大的存储选项。新功能是无线连接:支持 802.11s 的 TI WiFi 和蓝牙模块取代了旧的以太网连接器。

从表面上看，新的 BeagleBone Black Wireless 值得一提——这是一款带无线功能的 beagle bone——但不是特别值得一提。但是当你看到一块巨大的树脂砖正好落在棋盘中间时，BeagleBone 家族的最新设备就变得非常非常有趣了。这个版本的 BeagleBone 的模块上系统是几个月前发布的片上系统。Octavo Systems OSD335x 是一款名副其实的片上猎兔犬骨。这是一个带大球的 BGA，可以用手工焊膏和烤箱回流转换来焊接。事实上，BeagleBone Wireless 是由 Eagle 的[Jason Kridner]设计的 6 层板。这仍然有点超出 OSHPark 的标准功能，但设计仍然可以削减，并显示了这种片上 BeagleBone 如何应用于其他开放硬件项目。