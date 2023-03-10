# 5 美元 VGA 用于树莓 Pi

> 原文：<https://hackaday.com/2016/02/21/5-vga-for-raspberry-pi/>

Hackaday.io 用户[mincepi]希望他的 Raspberry Pi Zero 有 VGA 输出。他的追求让他设计了一个 PCB，可以与 VGA 显示器和 Pi 板配合使用，根据他的估计，每个成本约为 3.62 美元(尽管要达到这个价格，你必须建造三个)。

VGA hack 使用 Pi 的内置端口来驱动 VGA(VGA 666 by[Gert])，我们在之前已经介绍过[。不过，本着零度的精神，[明斯皮]将外部组件剥离到了最低限度。他使用较少的位元，所以色彩解析度较低。他使用更便宜的 5%电阻，并将它们直接焊接在 Pi 和 VGA 板之间，以节省一个连接器(见下文)。他使用了一个中间引脚被移除的公连接器，因此它跨在 PCB 上并直接插入显示器。](https://hackaday.com/2015/03/05/using-cheap-displays-with-the-raspberry-pi/)

[![pivgaint](img/05be69e35601269f5baec177ba3a545f.png)](https://hackaday.com/wp-content/uploads/2016/02/pivgaint.png)

你可以从 OSHPark 订购电路板，也可以自己制作电路板。如果你不想买新的，甚至还有回收旧 VGA 电缆的说明。不用担心 [VGA 已死](https://hackaday.com/2016/01/29/vga-in-memoriam/)的传言。黑胶唱片和电子管放大器也已经死了很长时间，但它们仍然年复一年地存在着。

顺便说一下，这个项目是树莓派零竞赛的参赛作品。

* * *

![Raspberry_Pi_LogoSmall](img/87d7e34f7ac8cc3ae6c8619ad96c149e.png)

树莓派零竞赛由 Hackaday 和 Adafruit 主办。奖品包括 Adafruit 的树莓派零和 Hackaday 商店的礼品卡！
[查看所有参赛作品](https://hackaday.io/submissions/adafruitpizerocontest/list) || [现在就进入你的项目吧！](https://hackaday.io/contest/9326-adafruit-pi-zero-contest)