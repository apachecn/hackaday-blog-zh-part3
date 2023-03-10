# Hackaday 奖参赛作品:玩 USB 供电

> 原文：<https://hackaday.com/2017/10/17/hackaday-prize-entry-playing-with-usb-power-delivery/>

USB 电力传输是一种能够通过 USB 电缆传输 100 瓦的技术。它已经出现了五年，但只是在最近几年，支持 USB PD 的设备和电源才出现在市场上。这是一项非常有趣的技术，我们迫不及待地想看到人们在一元店买到的五安培电流流过电缆的结果，但使用 USB PD 的 DIY 解决方案在哪里？

对于他的 Hackaday 奖参赛作品，[克莱顿]就是这样做的。他为 USB PD 制作了一个小小的电源插孔，一端有一个 USB type-C 插头，另一端有一对螺丝端子。[这是 USB PD Buddy Sink](https://hackaday.io/project/20424-pd-buddy-sink) ，一旦我们找到一些便宜的 100 瓦 USB 电源适配器，这将是一个无价的工具。

从一个 USB 充电器获得 100 瓦的功率比仅仅将几根电线焊接在一起要复杂一些。电力输送必须经过协商，为此[Clayton]使用了简单、廉价的 STM32F0 ARM 微控制器。插入 USB 总线有点复杂，但幸运的是，在 Semi 上有一个整洁的小可编程 [USB Type-C 控制器 PHY](http://www.onsemi.com/PowerSolutions/product.do?id=FUSB302BMPX) 完成所有工作。加上几个 MOSFETS 和其他辅助部件，你就有了一个简单的 100 瓦小电源，可以直接插入你新的花哨的笔记本电脑充电器。

USB PD Buddy Sink 的设计已经完成，[Clayton]手头有一堆这样的东西。他在 Tindie 上出售它们，但这也是获得 Hackaday 奖的一个很好的机会。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)