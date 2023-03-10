# 微量天平测定酒精含量

> 原文：<https://hackaday.com/2017/12/21/microbalance-determines-alcohol-content/>

随着假日季节的临近，能够确定办公室聚会 punch 收到了多少(或多少)尖峰信号是很有用的。[Russell Smith] [展示了他如何尝试使用由老式面板仪表制成的微量天平来确定酒精的标准度数](http://blog.qqrs.us/blog/2015/08/21/proofing-spirits-with-homemade-electrobalance/)。

这可能看起来很奇怪，但是因为酒精的蒸发速度比水快，如果你有一个足够好的标尺，你可以画出蒸发速度的变化。这就是微量天平发挥作用的地方。这个想法是将一个旧仪表的指针压下，测量达到某一偏差所需的电流量。他的结果不完全令人满意，但他的方法很有趣。

[Russell]首先用一个电源和一个伏特计测试电表，看看它是如何工作的。它做得很好，但你必须确保每次都将样品放在相同的位置，并测量相同的偏差。他使用 Arduino 和红外传感器自动完成了这一过程。虽然他的数据显示了酒精含量的一些相关性，但他无法使用浸湿的棉签获得可重复的读数。

如果你想要一个更精致的微量天平，那里有一个 [open。如果酒精部分更有趣，你可以去看看](https://hackaday.com/2015/03/31/measure-as-little-as-you-want-with-openqcm/)[的 Zymeter](https://hackaday.com/2015/03/29/measuring-alcohol-content-with-time-of-flight-sensors/) 。