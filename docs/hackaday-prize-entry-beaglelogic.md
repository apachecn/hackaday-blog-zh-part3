# Hackaday 奖参赛作品:BeagleLogic

> 原文：<https://hackaday.com/2017/07/19/hackaday-prize-entry-beaglelogic/>

几年前，[Kumar]为 BeagleBone 设计了 14 通道 100 MSPS 逻辑分析仪 BeagleLogic，作为 Hackaday 奖的参赛作品。这是一个很棒的工具，它利用了 BeagleBone 中的 PRUs，给任何一个拥有 BeagleBone 的人一个非常强大的逻辑分析器，而不需要太多的钱。

今年，[库马尔]又回来了。他正在用芯片上的猎兔犬骨改进猎兔犬逻辑。这是 BeagleLogic Standalone，16 通道逻辑分析仪，100 MSPS，使用单芯片。

就像几年前的 BeagleLogic 一样，[Kumar]依赖于 BeagleBone 中那些花哨的 pru，使读取 GPIOs 和闪烁的 led 变得如此简单和快速。与[beagle logic shield/cape/whatever](http://hackaday.com/2015/05/19/hackaday-prize-entry-a-beaglebone-logic-analyzer/)不同，BeagleLogic Standalone 使用 Octavo Systems 的 OSD 3358——片上 BeagleBone 作为硬件。这将 BeagleBone 中的所有东西都集成到一个包中，使其成为一个紧凑的单元，但仍然具有更大的 BeagleLogic 的所有功能。

这款袖珍逻辑分析仪内置 OSD3358 本身、逻辑分析仪前端、千兆以太网端口、USB、SPI 闪存、SD 卡插槽和 eMMC 以及 RTC。一个扩展标头包含一个 UART、I2C、SPI、两个 PWM 输出、6 个 GPIOs 和一个 PRU 时钟，用于实验性同步捕获。

这个逻辑分析仪有一个基于网络的前端，这看起来对任何硬件黑客来说都是一个极好的工具，而且价格应该相当便宜。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)