# tiny driver–在不带 Arduino 的 tiny84 平台上

> 原文：<https://hackaday.com/2016/04/22/tinydriver-attiny84-platform-without-arduino/>

你不需要一个 Arduino 来做所有的事情！还是你？这是一个经常发生的争论。无论结果如何，大多数人都同意，一旦你把脚伸进了游泳池的浅水区，真正的乐趣就在你潜入深水区的时候。

[Mahesh Venkitachalam]为 Atmel ATtiny84 芯片设计了一个实验性的开源分线板 [tinyDriver](https://hackaday.io/project/10077-tinydriver) 。他的想法是创建一个方便的平台，让用户深入了解微控制器，并利用芯片的各种功能，如定时器、PWM、中断、ADC 和数字 I/O。对于初学者来说，ATtiny84 足够便宜和简单。加一个低成本的 AVR 编程器，安装免费的、跨平台的 avr-gcc 和 avrdude 工具链，读完数据表，学点 C 编程，开始实验。冲洗并重复，你很快就会成为专家。他在自己的网站上记录了几个[起步项目](http://electronut.in/tinyDriver/)来帮助你。

硬件是开源的， [Git 库](https://github.com/electronut/tinyDriverP)包含硬件源代码和示例代码。如果你是一个硬件新手，他会考虑周到地在板上添加一个 PTC 可复位保险丝和反极性保护，以确保你不会过早地释放神奇的蓝色烟雾。所有 I/O 都在一个接头上分开，不需要时可以禁用电机驱动器和 RGB LED。该板不支持手工组装，但他计划短期内进行众筹。如果您想超越 Arduino 平台，tinyDriver 这样的项目是不错的选择。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/b318d0dafdb9c4774e30c2c93cd4fae4.png)](http://hackaday.io/atmel) [![Microchip](img/35a8c11c83c9d58713ff84cc1841a3cf.png)](http://hackaday.io/microchip)  [![Digi-Key](img/a5cd2ae2d2d27913ef85cc9b413afa07.png)](http://www.digikey.com/)  [![Supplyframe](img/7b65eab28dbaebaf5bf15a1a9517b6dd.png)](http://supplyframe.com/)