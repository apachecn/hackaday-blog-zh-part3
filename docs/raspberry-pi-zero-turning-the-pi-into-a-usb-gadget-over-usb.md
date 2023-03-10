# raspberry Pi Zero–通过 USB 将 Pi 变成 USB 小工具

> 原文：<https://hackaday.com/2016/01/07/raspberry-pi-zero-turning-the-pi-into-a-usb-gadget-over-usb/>

[gbaman]想出了一种更简单的方法来通过 USB 编程新的 [Raspberry Pi Zero，而无需修改电路板。](http://pi.gbaman.info/?p=699)这个为什么有用？一个吸引我们的例子是将 Zero 的 USB 端口设置为大容量存储设备。想象一下，插上 Pi 驱动的机器人，将 Python 脚本拖放到出现的大容量存储设备中，然后按下机器人上的按钮运行新脚本。五块钱太贵了。

您可以让 PI 模拟从 USB MIDI 控制器到简单的 USB 串行接口的所有设备。我们很高兴看到人们想出了什么样的用途。不幸的是，在我们等待下一次生产结束时，Pi Zero 仍然在大多数地方缺货。尽管如果你已经有了一个，为什么不看看我们关于这个设备的一些[想法](http://hackaday.com/2015/12/01/raspberry-pi-zero-or-minus-one/)和[体验](http://hackaday.com/2015/12/23/firing-up-a-pi-zero/)！

[gbaman]的工作基于[Dave-0]和其他人在 Raspberry Pi 论坛上所做的工作。【LadyAda】也有这种黑客的一个版本，我们在中提到过的[，它涉及到将一个头部焊接到 pi 并使用一个 UART 适配器。](https://hackaday.com/2015/12/27/turning-the-pi-zero-into-a-usb-gadget/)

【via [黑客新闻](https://news.ycombinator.com/item?id=10842216)