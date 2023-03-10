# Hackaday 奖参赛作品:MakerNet

> 原文：<https://hackaday.com/2017/05/27/hackaday-prize-entry-makernet/>

无论“制造商”属于哪个市场，最大的趋势之一就是电子产品的乐高化。如果你没有注意到的话，制造电子产品是很难的。任何将传输线、电流环路和射频魔法转化为五岁儿童可以使用的东西，显然都可以应用于教育。对于他的 Hackaday 奖参赛作品，[杰里米·吉尔伯特]正在建立一种快速，直观，模块化的方法来探索电子学。它比 100 合 1 Radio Shack spring clip 套件更容易使用，实际上您可以使用该系统制作有用的项目。

MakerNet 是 Jeremy 对复杂电子设备问题的解决方案，Arduinos 通过 DuPont 电缆连接到试验电路板，显然还连接到实际的电子乐高玩具。该系统的核心是围绕 Atmel SAM D21 微控制器构建的，这是一款 ARM Cortex-M0+芯片，其处理能力足以满足任何值得“制造商”标签的要求。这个主板通过基本上是 I2C 总线的东西连接到设备。系统中的每个模块都有一个输入和输出接头。每个模块上的小型 SAM D11(售价 1 美元)处理所有通信。

现在，[Jeremy]正在试验十几个模块，包括 captouch 板、LED 矩阵、有机发光二极管显示器、旋转编码器和许多闪亮的 LED。这只是一个原型，但这正是我们在 Hackaday 奖的这个阶段所寻求的。看了[杰里米]制作的视频(如下)，这里有很多承诺。

 [https://www.youtube.com/embed/rZLKJq-t7fU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rZLKJq-t7fU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)