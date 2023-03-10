# 保持脂肪烟雾在它该在的地方

> 原文：<https://hackaday.com/2015/11/28/keeping-the-lipo-smoke-where-it-belongs/>

没有什么比把一个便宜的小发明变得有用更能让黑客开心的了。在 Hackaday.io [AndyHull] [打开一些廉价的 LiPo 电池电源包](https://hackaday.io/post/28071)看看他是否能给佳能 Powershot 相机供电。整个 shebang 将被留在荒野中进行摄影，因此保持其廉价是一个大目标，因为它可能会被破坏或丢失。

![](img/3d0f37da77c2043735063841809f7abd.png)

[Andy]看到的电源组有一个 TP4221，可以控制多达 4 个并联的 18650 LiPo 电池的充电周期。如果 LiPo 电池电压降至 3.2 伏以下，控制器还会将一个或两个 USB 端口的电压提升至 5 伏，同时提供自动关闭功能。低于该电压时，电池可能会受损，并可能导致火灾。

[安迪]使用的电池组也有一个*手电筒*输出，几乎直接从电池驱动 LED。该输出在 100 mA 时标称为 3.8 V，这正是他为佳能 Powershot 供电所需的电压。它可以用来驱动小型微型或其他低功率设备。

LED 被移除，并被替换为与包装外部的连接。*火炬*输出由快速按下开关触发，该开关也被一个连接器取代，以允许远程控制。

如果你正在寻找强大的电池选项，给 LiPo 一个尝试，看看[Andy]的 [LiPo 电池安全问题帖子，](https://hackaday.io/project/3223-sticks-o-dynamite-battery-pack)也在 Hackaday.io 上。要了解更广泛的 LiPo 概述，请参见这个[各种电池的强迫性消耗。](http://hackaday.com/2014/09/05/an-obsessively-thorough-battery-and-more-showdown/)