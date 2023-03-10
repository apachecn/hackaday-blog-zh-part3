# 来原型吧！这个灯丝末端需要 80 分贝

> 原文：<https://hackaday.com/2017/01/27/lets-prototype-this-filament-end-needs-80-decibels/>

当 3D 打印不可避免时，到达一卷细丝的末端。结果从轻微的烦恼到毁坏的印刷品不等。最近，我需要打印一些大型作业，每个作业都使用了半个多塑料卷轴。我不愿意每次打印都用一个新的卷轴(然后搁置一个 60%用过的)，所以有一个问题需要解决。我的 3D 打印机需要的是灯丝显示器，或者至少我是这么认为的。

在回顾了一些项目和售后选项后，我最终做出了自己的选择。像大多数原型一样，它没有立即获得成功，但没关系。原型设计的目标之一不仅是验证你正在解决的问题与你认为存在的问题是一样的，而且是迫使你可能没有考虑到的其他问题浮出水面。如果什么都没学到，失败只是一种浪费，而且学得越快越便宜越好。

明智的设计步骤也有助于最大限度地减少浪费，所以我从查看已经存在的解决方案开始。

### 我假设的需求:灯丝监控器

我发现的灯丝显示器是售后或 DIY 设备。不算不完整的 Kickstarter 项目，我发现了由[Aaron Tunell]设计的售后 [Tunell Monitor](http://tunell.us/) 以及一些 DIY 项目。大多数通过以某种方式转动编码器轮来监控灯丝的运动(例如，[弗洛里安]的[灯丝馈送编码器](http://hackaday.com/2015/06/16/prevent-failed-prints-with-a-filament-speed-sensor/)，以及[罗德]的[灯丝监控器](http://www.thingiverse.com/thing:57447))，还有一个使用旧 PS/2 鼠标的[内脏](http://hackaday.com/2016/12/08/this-old-mouse-keeps-track-of-filament-usage/)作为传感器。

这些项目很聪明，但是我的需求比他们提供的解决方案要窄得多。我的问题不是缺少细丝编码。我的问题是，在组成一个印刷品的许多小时里，我不能在那里呆上正确的四分钟。

### 实际需要:正确的四分钟

在我的打印机上，如果一个卷轴用完了，只要我有时间装载一个新的卷轴，并在旧细丝进入挤压机时，将新细丝紧靠旧细丝的末端，我就可以挽救打印。我测量了最少四分钟的时间来做这件事。四分钟是足够的时间，只要我准备好了，并且能够在交换发生时进行。

丢失的部分并不是我的机器不知道什么时候灯丝轴是空的。问题是，当*变空的时候，我——操作者——有四分钟的时间采取行动，但是我没有一个好的方法知道那是什么时候。*

通过这种方式缩小问题的范围，我可以保持解决方案简单。如果我假设至少在假脱机将要用完的一两个小时内，我会在打印机的听力范围内，我应该能够用一个简单的声音警报来解决我的问题。当最后一根细丝从线轴上脱落时，发出警报，我至少有四分钟的时间来喂一根新的。

我决定做一个简单的灯丝报警器的原型，除此之外别无它用。我称它为尖叫先生。

### 设计概述

尖叫先生的工作可以总结为:

1.  当灯丝存在时，什么都不会发生。
2.  当灯丝用完，尖叫你的傻瓜头了。

关键要素是:

*   3D 打印外壳
*   独立的(无外部电源或信号)
*   小到足以直接夹在灯丝本身上；不需要固定在打印机的框架上。
*   电气简单:硬币电池，一个感应灯丝的滚轮开关和一个蜂鸣器。
*   响应警报时易于关闭。

### 原型

一个外壳被设计成一种蛤壳状来容纳元件。磁铁将外壳固定在一起，也充当电源连接器，因此将两半合在一起(或拉开)就充当了主电源开关。两个 CR2032 硬币电池为一个小型 80+分贝蜂鸣器供电，由滚轮开关控制。当设备不尖叫时，它不耗电。

灯丝穿过一个孔，这个孔可以让一个常闭的滚轮开关感知灯丝是否存在。当滚轮按下时，电路断开。灯丝没了，滚轴就起来了，电路就闭合了；该单元开始发出大约 80 分贝的啸声，直到两半被拉开(或者灯丝被重新插入)。

[![](img/df28b80a539b5030e046027dbc8ee3cf.png)](https://hackaday.com/wp-content/uploads/2016/12/screenshot-2016-12-11-21-50-09.png)

Upper hole is a coin cell holder. Wires from the rectangular holes at the bottom will serve as contacts. The lower hole is where filament goes in.

[![](img/7b8e65695ce5fd810f9f73ebfd80b8c7.png)](https://hackaday.com/wp-content/uploads/2016/12/screenshot-2016-12-11-21-50-03.png)

The large hole is for the buzzer.

[![](img/75fdcd6e27e12fbdec0d831bd24f33d1.png)](https://hackaday.com/wp-content/uploads/2016/12/screenshot-2016-12-11-21-48-36.png)

The two halves – inside view. The round holes are for the magnets.

### 装配

这两半是用 PLA 打印的，组件是用胶水粘上去的。除了在安装前将导线焊接到磁铁上之外，连接都是在部件固定后点对点焊接的。

[![](img/6f6a9a2bf7f4da5c7391cfeb0cdbbc30.png)](https://hackaday.com/wp-content/uploads/2016/12/mister-screamer-outside-e1484936086467.jpg)

Coin cells are a friction fit.

[![](img/1c19219c6f47a0ac2dd563bc21011908.png)](https://hackaday.com/wp-content/uploads/2016/12/mister-screamer-insides.jpg)

All working parts (foreground) and power supply (background).

[![](img/3d62316b0c16b728a7bc00ee01e7ebca.png)](https://hackaday.com/wp-content/uploads/2016/12/mister-screamer-internal.jpg)

Power can be cut (and the unit silenced) by pulling the shells apart.

### **警告:大约在 1:30** 发出响亮的嘟嘟声

[https://videopress.com/embed/USFve0zv?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0](https://videopress.com/embed/USFve0zv?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0)