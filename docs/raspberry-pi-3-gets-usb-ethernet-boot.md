# 树莓 Pi 3 获得 USB，以太网启动

> 原文：<https://hackaday.com/2016/08/04/raspberry-pi-3-gets-usb-ethernet-boot/>

树莓派是一个伟大的电脑，即使它没有 SATA。对于那些因为没有正确关闭 Pi 而不可避免地损坏了一些 SD 卡的人来说，这里有一些东西给你: [USB 大容量存储引导树莓 Pi 3](https://www.raspberrypi.org/blog/pi-3-booting-part-i-usb-mass-storage-boot/) 。

对于 Raspberry Pi 1、2、计算模块和 Zero，有两种引导模式–SD 引导和 USB 设备引导，USB 设备引导仅在计算模块上找到。Raspberry Pi foundation 的[Gordon]花了很多时间研究 Raspberry Pi 3 中使用的 Broadcom 2837，并在 32 kB 中找到了足够的空间来包括 SD 引导、eMMC 引导、SPI 引导、NAND 闪存、FAT 文件系统、GUID 和 MBR 分区、USB 设备、USB 主机、以太网设备和大容量存储设备支持。你现在可以从任何地方启动 Raspberry Pi 3。

[这些新引导模式的文档](https://www.raspberrypi.org/documentation/hardware/raspberrypi/bootmodes/)讲述了如何将映像放入 USB 拇指驱动器的过程。这与将图像放在 SD 卡上的过程没有太大的不同，在下一个版本的`rpi-update`中，这个过程会有所简化。一些 USB 拇指驱动器不工作，但只要你坚持与闪迪或三星，你应该没问题。

比 USB 引导更有趣的是 Pi 3 通过网络引导的能力。通过网络启动并不新鲜 Apple II 可以在雪地里双向爬坡(T1 ),但 Pi 最常见的用途是连接到网络存储上所有电影的哑媒体播放器。有了网络引导，你可以轻松地在第二台电视上播放所有媒体。[点击这里查看网络引导教程](https://www.raspberrypi.org/documentation/hardware/raspberrypi/bootmodes/net_tutorial.md)。