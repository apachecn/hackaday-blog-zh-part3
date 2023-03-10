# 导航的事情:四天，三个问题，和假压电

> 原文：<https://hackaday.com/2016/10/20/navigation-thing-four-days-three-problems-and-fake-piezos/>

*[导航物](http://blog.honzamrazek.cz/2016/09/navigation-thing/)*由【Jan Mrázek】设计建造，作为为期一周的研讨会期间高中生夜间游戏活动的一部分。一条穿过森林的夜间道路上有执行简单任务的站点，而*导航设备*使用 GPS、数字罗盘、寻呼机和一圈 RGB LEDs 来提供一点“惊喜因素”，同时引导一群学生从一个站点到下一个站点。这些设备有明确的设计方向:

> “我想制造一个参与者可以找到的设备，插入电池，并根据蜂鸣声找到下一站。想象一下这种强烈的感觉:在午夜迷失在一个远离文明的未知地带，只相信你发现的一个嘟嘟响的东西。这就是我想要实现的感觉。”

*导航设备*(总共有六个)通过 GPS、数字指南针和一圈 WS2812 LEDs 指引用户到固定的路点——但向用户反馈的主要方式是随着你接近目的地而变快的蜂鸣声。[Jan]只有四天时间来完成所有六个单元，这是可行的。但正如我们大多数人所知，在紧迫的期限内完成工作，往往不是做你知道的工作，而是有效地处理过程中不可避免地出现的意外障碍。

第一个真正要解决的问题是哔哔声本身。“越接近目的地，哔哔声越快”似乎是一个简单的任务，但由于人类感知事物的方式，它比听起来更复杂。我们感觉到大的变化比小的增量变化更容易，所以基于距离的蜂鸣频率的线性变化不是很好。无论你是在控制音量、亮度，还是人类感知的任何东西，都存在类似的问题(及其解决方案)。与其将距离编码为蜂鸣频率，不如简单地使用蜂鸣来表示整体变化更有效:当你离开时，蜂鸣明显变慢，但当你靠近时，蜂鸣快得多。

[![A "piezo" buzzer that was assumed to have no significant magnetic field, but actually contains a magnet.](img/70b95fd91ad7c04b6b36d8bd4c4969e9.png)](https://hackaday.com/wp-content/uploads/2016/10/piezo-not-piezo-elektro-028_v1.jpg)

A “piezo” buzzer that was assumed to have no significant magnetic field, but in fact contained a magnet.

其他有趣的问题就不那么简单了，它们与数字罗盘或磁力计有关。第一个问题是[来源于【Jan】的压电蜂鸣器不包含实际的压电元件](http://blog.honzamrazek.cz/2016/09/face-the-fail-piezo-or-not-to-piezo/)。它们含有磁铁——这会干扰数字罗盘的运行。解决这个问题后，更多的指南针问题出现了。在现场测试最终设备时，罗盘读数不符合预期，[Jan]不知道为什么。

经过仔细排查，找到了罪魁祸首:电路板另一侧的 AA 电池。每个 AA 电池都有一个微弱的(略有不同的)磁场，电池相对于磁力计的接近和放置导致了偏差。令人高兴的是，一旦理解了问题所在，解决方法就简单了:每次插入新电池时都要校准指南针。

如果你对*导航的东西*感兴趣，去看看 [github 库](https://github.com/yaqwsx/NavigationThing)。说到实际的压电器件，压电器件有多种巧妙的实现方式。甚至还有[压电变压器](http://hackaday.com/2015/12/12/piezoelectric-transformers-are-a-thing-have-you-used-one/)和[压电真空泵](http://hackaday.com/2014/10/30/piezo-vacuum-pump-for-lightweight-pick-and-place/)。