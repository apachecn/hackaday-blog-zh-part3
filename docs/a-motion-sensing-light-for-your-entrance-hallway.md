# 门厅的运动感应灯

> 原文：<https://hackaday.com/2017/11/11/a-motion-sensing-light-for-your-entrance-hallway/>

抱着一堆东西回到一个黑暗的房子里，通常是在混乱中摸索，直到有人设法打开灯。[Pavel Gesyuk]通过建造和安装一个[运动检测入口灯](http://pagealh.com/2015/05/09/arduino-self-switching-corridor-lamp/)完全避开了这个问题！

[Gesyuk]正在使用一个名为 Funduino Mini Pro 的 Arduino 克隆，一个双通道、双向继电器——他只需要一个，但你可以使用手头上的东西——一个将 220V AC 转换为 5V DC 的循环电源和一个红外传感器。

该项目的目标是了解 Arduino 和运动传感器的来龙去脉，而不仅仅是入口走廊的照明解决方案。在熟悉 Arduino 的一些最初障碍之后，[Gesyuk]将所有东西都连接在一个原型板上，并将其放入一个塑料盒中——在交通繁忙的地区松散的电线不是一个安全的家。

虽然灯被设置为超时并在一段时间后关闭，但[Gesyuk]家的配置意味着他[![](img/62b8d1f7d453f742c45961f73eea0c83.png)](https://hackaday.com/wp-content/uploads/2017/10/motion-sensing-hallway-light-mounted.jpg)必须故意放置红外传感器，以便只有入口处的移动才会触发它——尽管这将是扰乱房客的绝佳素材！不过，不用担心一回家就开灯还是挺好的。

我们之前报道过[Gesyuk]的[Raspberry Pi 供电的气象站](https://hackaday.com/2016/01/16/raspberry-pi-wind-measurement/)，迫不及待地想看看他是如何将自己的家变成创客的仙境的。