# 不碍事的终点挡板

> 原文：<https://hackaday.com/2017/03/30/endstops-that-stay-out-of-the-way/>

在建造一台新的 delta 打印机的过程中，[thehans]决定他[需要自己的终端设计](https://www.thingiverse.com/thing:2204123)，使用最少的硬件。终点挡板只是当打印机移动到轴的极限时被击中的开关，但[thehans]想要对他的 [BigDelta 3D 打印机](https://github.com/justinledwards/BigDelta)的构建进行一点改进。

其结果是一个小单位，摇篮微动开关，只需要一个单一的拉链领带安装齐平，导致一个超级整洁的外观件。此外，它安装在 delta 的 v 型槽轨道上，这样安装不会占用机器的任何运动范围，因为托架可以通过它。它是在 OpenSCAD 中进行的参数化设计，因此可以随意修改它以适应其他类型的开关。

[![](img/184d23686c9cd7385ec1b9b80ba33b5c.png)](https://hackaday.com/2017/03/30/endstops-that-stay-out-of-the-way/8aa08068a4f9336e5c17ff62688a8c96_preview_featured/)

Wheel triggers the endstop directly, and the carriage can ride past the endstop mount.

[![](img/09779e872df813c84b8c7fdd838ca7a6.png)](https://hackaday.com/2017/03/30/endstops-that-stay-out-of-the-way/4b078936bded8bce0049a31065e84227_preview_featured/)

Zip strap mounts flush. Nubs inside the unit mate with the microswitch’s bolt holes.

Delta 打印机非常漂亮，是创新的沃土。以这个[碰撞传感器](http://hackaday.com/2016/07/30/a-crash-sensor-for-delta-3d-printers/)为例。或者这个[非常不寻常的无轨设计](http://hackaday.com/2013/09/18/reprap-simpson-puts-a-new-spin-on-delta-repraps/)。至于*大*三角洲，一个[大到足以打印一栋房子](http://hackaday.com/2015/09/27/enormous-delta-bot-3d-designed-to-print-an-entire-house/)提醒我们，“大”是一个相对的术语。