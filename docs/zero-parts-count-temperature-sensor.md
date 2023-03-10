# 零零件计数温度传感器

> 原文：<https://hackaday.com/2016/06/10/zero-parts-count-temperature-sensor/>

快问:导通二极管的正向压降是多少？如果你回答了 0.6 到 0.7 V，你就及格了，但是你还得继续读下去。如果你回答了![V_F = \frac{T-T_0}{k} ](img/b334b4860d6f02c57bb26ba5d73e5cdb.png)，其中`T[0]`和`k`是由实验确定的设备特定常数，你会得到一个金色的开心果扳手。

[![vsd%2C+n-01](img/83cb3cda38d3152288242f9abb014641.png)](https://hackaday.com/wp-content/uploads/2016/06/vsd2cn-01.png) 【雅各布】挣了他的扳手，然后一些。因为他不仅用上面的方程式[制作了一个温度传感器](http://kaktuscircuits.blogspot.de/2016/06/push-it-to-limit-measure-true-junction.html)，他还用了一个你可能已经忘了的二极管——MOSFET 硅片内部的二极管——本征[体二极管](https://en.wikipedia.org/wiki/Power_MOSFET#body_diode)。

[Jakub]的主要项目是一个 Arduino 控制的电子负载，他称之为[兆瓦](http://kaktuscircuits.blogspot.de/2015/03/mightywatt-resource-page.html)，一个结实的功率 MOSFET 被用作可变电阻元件。拉二三十 A 的时候就热了。没有温度传感器，很难测量到底有多热，最好的温度传感器是内置在 MOSFET 芯片中的传感器。

在他的文章中有很多细节，关于他如何切换负载来测量向前的下降，以及他如何校准整个事情。这是技术性的，但给它一个阅读，这是好东西。这是你锦囊妙计。

如果你想玩更多愚蠢的二极管把戏，我们建议[将它们用作太阳能电池](http://hackaday.com/2012/04/13/using-diodes-and-transistors-as-solar-cells/)或者将它们串在一起[制成热感相机](http://hackaday.com/2012/02/01/reading-diodes-to-create-a-thermal-imaging-system/)。