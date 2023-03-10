# Hackaday 奖参赛作品:表征 LED 和激光二极管

> 原文：<https://hackaday.com/2016/09/09/hackaday-prize-entry-characterizing-led-and-laser-diodes/>

不用说，我们对发光二极管、激光二极管和其他闪光灯着迷。虽然我们可以得到任何发光的东西，但数据表并不总是准确或可用的。为了他的 Hackaday 奖参赛作品，[Ted] [正在建造一种设备来表征所有 blinkies 的效率、I/V 曲线和光学特性](https://hackaday.io/project/12874-automated-ledlaser-diode-analysis-and-modeling)。这是一个让 glowy 的东西变得更好的项目，也是 Hackaday 奖的一个很好的参赛作品。

这个项目的灵感来自[Ted]的两个项目，一个需要 led 的响应曲线，另一个需要激光二极管。这将为他提供光输出与电流的关系图、光输出角分布以及激光二极管的激射阈值。数据手册中并不总是有这些数据，所以自制工具是唯一的选择。

这个工具的高级设计基本上是一个电压表和电流表测量一个发光二极管，产生 IV 曲线和测量光输出。除了 LED 的纯光学特性之外，它可以处理所有的测量。这是通过测角仪测量的，或者基本上是将被测设备放在与步进电机相连的托架上，并移动它通过固定的光学检测器。

如果您想知道为什么需要这款器件，而简单的数据手册是不够的，[看看这个](https://hackaday.io/project/12874/log/44613-this-is-why-i-am-building-the-analyzer)。[Ted]测量了 Luxeon Z LED 的效率，发现最大效率约为 10mA。该 LED 的数据表显示标称正向电流为 500mA，最大值为 1000mA。如果你只看数据手册，你可以很容易地假设一个由硬币电池供电多年的设备是不可能的。它不是，而且[Ted]的设备给了我们这个信息。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)