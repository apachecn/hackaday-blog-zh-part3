# Hackaday 奖品入口:以 RFID 方式解锁您的 PC

> 原文：<https://hackaday.com/2017/10/18/hackaday-prize-entry-unlock-your-pc-the-rfid-way/>

有时，我们看到项目的名称很好地描述了正在实现的目标，却没有传达它们还提供的额外有用的方面。[Prasanth KS]的 [Windows PC 使用 RFID](https://hackaday.io/project/27731-windows-pc-lockunlock-using-rfid) 锁定/解锁也是如此。从表面上看，这是一个解锁 Windows PC 的项目，但当你坐下来通读它时，你会发现这是一本非常有用的入门书，可以帮助完全的 RFID 新手了解如何构建一个 RFID 项目。即使目标没有做到这一点，也没有理由为什么它不能用于除 Windows 之外的任何其他流行的 PC 操作系统。

该项目采用了 MRFC-522 RFID 模块，并解释了如何将其与 Arduino 接口。在这种情况下，有问题的 Arduino 是 Arduino Pro Micro，因为它能够作为 USB 主机而被选中。所提供的代码相当于一个键盘，它将击键序列发送到解锁所需的计算机。整个安装在一个似乎是 3D 打印的外壳中，为了便于使用，RFID 标签的内部被安装在一个环中。

正如我们上面所说的，这个项目的重点不仅仅是一个电脑解锁器。任何简单的 RFID 任务都可以以此为基础，如果 USB 不是必需的，那么它可以很容易地使用更普通的 Arduino。如果你是 RFID 新手，不妨读一读。

很多 RFID 项目以前在这里做过，[比如这个门锁](https://hackaday.com/2016/09/25/simple-rfid-door-lock-system/)。我们还有[戒指中的另一个标签](https://hackaday.com/2014/03/16/stuffing-an-rfid-card-into-a-finger-ring/)。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)