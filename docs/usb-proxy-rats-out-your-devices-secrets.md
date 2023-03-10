# USB 代理泄露你设备的秘密

> 原文：<https://hackaday.com/2015/12/23/usb-proxy-rats-out-your-devices-secrets/>

如果您需要对运行 Linux 的计算机上的 USB 协议进行逆向工程，您的工作很容易，因为您可以控制目标系统上的一切——您只需查看原始的 USB 数据。另一方面，如果你想对一个插入游戏机的 USB 设备进行逆向工程，你的工作要困难得多。直到现在。

serialusb 是 Mathieu Laurendeau(别名 Matlo)的副产品。他的主要项目， [GIMX](http://blog.gimx.fr/) 针对游戏，让你修改你的游戏控制器的性能，首先通过你的 PC，并在转发到目标主机之前调整 USB 数据。想要速射？你猜对了。改变方向盘灵敏度曲线？当然可以。

GIMX 本质上是你的控制器和你的控制台之间的一个 USB 中间人，并增加了修改数据的能力。不过，对于 GIMX 尚不支持的硬件，要么[Matlo]需要借用你的控制器，要么教你在你自己的 USB 流量中进行中间人操作。这就是 serialusb 的作用。

所需的硬件非常简单:一个 USB 转串行适配器和一个基于 ATmega32u4 的 Arduino 克隆。你们中的许多人可以用手头的零件将它组装起来，无论如何，运行 GIMX 也需要同样的硬件。数据通过你的电脑，被 USB moned T1 和 T2 wireshark T3 处理，然后通过串行传输到 ATmega，ATmega 再将数据转换回 USB，插入控制台。一个非常整洁的小装置。

如果这看起来很熟悉的话，[我们已经介绍过一个类似的由【Matlo】设计的技巧，它使用一个猎兔犬板](http://hackaday.com/2013/07/02/usb-sniffing-with-the-beagleboard-xm/)作为中间的计算机。这肯定是一个很好的设置，但是如果你没有备用的单板计算机，现在你只需要花大约 5 美元就可以完成。USB 倒车快乐！