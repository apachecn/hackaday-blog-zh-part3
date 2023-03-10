# 手表很小

> 原文：<https://hackaday.com/2016/02/18/attiny-watch-is-tiny/>

[陳亮](陈亮)正在制作终极戒指手表。这个东西比我在 20 世纪 90 年代早期拥有的廉价弹性手机酷多了——它是数码的，透明的，而且可能不会转动陳]的手指绿色。

![watch-guts](img/97a5298b6dce41d186a0fc084a04ad2a.png)当前的迭代已经完成，并建立在[他之前的 Arduino 驱动手表制造经验](http://www.instructables.com/id/ATtiny-Watch-Core/)的基础上。它运行在 ATtiny85 上，并在有机发光二极管上显示时间、温度和电池状态。虽然这在纸面上是一个相当简单的构建，但它的小人国实现使它变得不可思议。

[陳]当然必须考虑沿着连续曲线建造，这意味着手表的模块必须在单独的电路板上。它们位于马蹄形 [3D 打印](http://www.thingiverse.com/thing:1333116)表体的螺钉凸台之间，用电磁线连接在一起。[陳]甚至通过从一段裸露的杜邦连接器上切下薄金属总线并对折，自己制作了硬币电池端子。

如果你喜欢开源手表，但更喜欢戴在手腕上，可以看看这款 [PIC32 智能手表](http://hackaday.com/2016/01/10/pic32-smart-watch-2/)或[基于 Microduino 的 OSWatch](http://hackaday.com/2015/12/13/oswatch-an-open-source-watch/) 。