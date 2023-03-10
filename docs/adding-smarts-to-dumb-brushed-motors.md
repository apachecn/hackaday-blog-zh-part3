# 为无刷电机增加智能

> 原文：<https://hackaday.com/2018/06/25/adding-smarts-to-dumb-brushed-motors/>

今年 Hackaday 奖的一大部分是机器人模块，我们已经看到了许多为电机增加智能的项目。无论是电流检测、RPM 反馈、PID 控制，还是添加编码器，电机都变得越来越智能。不过，通常我们谈论的是花哨的无刷电机或步进电机。不起眼的 DC 有刷电机再次受到冷落。

这个项目旨在解决这个问题。这是一个智能电机驱动器的哑 DC 刷电机。你知道，你可以用几便士买到的马达。马达是给任何项目增加运动的最便宜的方式。那些马达。

机器人智能电机驱动器允许主机微控制器通过 I2C 控制 DC 有刷电机，并发回电机的速度和方向。实现了 PID，电机可以保持自己的速度，独立于主机系统上的许多困难控制。

这个电机控制器的内部由 PIC 12F 微控制器、H 桥电机驱动器、霍尔效应传感器和一个简洁的磁性编码盘组成。最终，这个项目将简单地安装在一个廉价的有刷电机的背面，并赋予它与花哨的伺服或步进电机相同的功能。它永远不会有与结实的 NEMA 17 踏步机相同的扭矩或功率处理，但有时你不需要它，一个简单的有刷电机就可以了。一个伟大的项目，也是 Hackaday 奖的优秀参赛作品。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)