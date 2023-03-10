# Hackaday 奖参赛作品:模块化步进控制

> 原文：<https://hackaday.com/2017/05/12/hackaday-prize-entry-modular-stepper-control/>

步进电机是精确运动控制的绝佳解决方案。你会在许多 3D 打印机设计中看到它们，因为它们可以精确地移动每个轴。步进器在许多机器人项目中得到应用，因为它们在低速时提供高扭矩。

由于步进器通常用于多轴控制系统，所以能够将多个电机连接到一个控制器是很好的。我们过去已经见过一些[步进器控制模块](http://hackaday.com/2016/06/01/mechaduino-closed-loop-stepper-servos-for-everyone/)，它们负责控制细节并通过 SPI、I2C 和 UART 接受命令。 [AnanasStepper 2.0](https://hackaday.io/project/20980-ananasstepper-20) 是一款使用 CAN 总线进行通信的新型步进控制器，也是 2017 年 Hackaday 奖的参赛作品。

CAN 总线在这种应用中有一些好处。多个电机可以通过单条总线连接到一个控制器。在低比特率下，它可以在公里长的总线上工作。布线简单而便宜:两根电线缠绕在一起，没有屏蔽要求。它还设计为在汽车和卡车等高噪声环境中也很可靠。

该项目旨在实现一个 API，允许从多种类型的控制器进行控制，包括 Arduino、Linux CNC、几种 3D 打印机控制器和桌面操作系统。有了这些控制器中的一个，你就可以在多个轴上移动东西了。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)