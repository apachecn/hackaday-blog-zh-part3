# 黑客日奖参赛作品:亚千兆赫射频

> 原文：<https://hackaday.com/2017/06/05/hackaday-prize-entry-sub-gigahertz-rf/>

尽管烤面包机拥有媒体 WiFi 和蓝牙连接的物联网，但在 1 千兆赫兹以下仍有很多乐趣。为了他的 Hackaday 奖参赛作品，[Adam]正在开发一款开源、可扩展的 915 和 433 MHz 无线电，专为机器人、无人机、气象气球和所有其他超千兆赫无线电支持的有趣项目而设计。

这款无线电模块的设计基于 [ADF7023 RF 收发器](http://www.analog.com/en/products/rf-microwave/integrated-transceivers-transmitters-receivers/low-power-rf-transceivers/adf7023.html)，这是一款功能强大且非常便宜的芯片，可在常见的 ISM 频段进行传输。电路的其余部分是一个 STM32 ARM Cortex M0+，具有 USB、UART 和 SPI 连接，支持用于这些移动项目的电池。

当然，你可以出去*买*一台 ISM 收音机，但这并不是这个项目的重点。[Adam]在这里设计了一款出色的电路板，全部由 KiCad 设计，同时还展示了他的射频能力。这里也有 RF 屏蔽，所以这不仅仅是一个设计挑战，也是一个组装和采购问题。这是一个伟大的项目，也是我们在 Hackaday 奖中寻找的一个很好的例子。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)