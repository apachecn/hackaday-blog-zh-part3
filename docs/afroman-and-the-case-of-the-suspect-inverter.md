# 一个阿曼和可疑逆变器的案例

> 原文：<https://hackaday.com/2016/03/09/afroman-and-the-case-of-the-suspect-inverter/>

如果你在网上搜索 12 伏交流电源逆变器设计，你很可能会遇到一个已经变得相当普遍的简单电路。它具有一个 4047 CMOS 非稳态多谐振荡器芯片，以推挽式配置驱动一对 MOSFETs，反过来驱动一个中心抽头主变压器。这不是一个新的设计，它的变体和前身甚至可以在互联网出现之前的日子里找到，那时电路来自你当地图书馆书架上的书。

![afroman-inverter-featured](img/3d7c58f544b44a259ce0c165a629ce4b.png)【Afroman】，对这些网页并不陌生，发布了一个视频，其中[他调查了 4047 逆变器](https://www.youtube.com/watch?v=5QaKiXRa-n0)，并提请注意它的一些缺点。让他担心的不是电路缺乏电压的频率稳定性，而是当设备负载不足时方波切换点的高频振铃。用 120 伏的美国变压器，这可以达到近 600 伏的峰峰值，如果你住在有 230 伏电源的地方，这可以超过 1 千伏。互联网建议的改进，在输出端增加一个电容，只会让情况变得更糟。正如他所说，它可以为灯泡供电，但你不会希望它靠近你的 iPhone 充电器。

如果这个视频有所成就的话，它给门外汉上了一课，虽然简单和流行的设计有时可能是绝对的宝石，但不要以为总是如此。

 [https://www.youtube.com/embed/5QaKiXRa-n0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5QaKiXRa-n0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



令人惊讶的是，我们在 Hackaday 展出的市电逆变器很少。有这种 [Arduino 驱动的，使用 PWM 驱动](http://hackaday.com/2013/06/21/an-arduino-power-inverter/)，但仅此而已。然而给我们提供了大量的娱乐。[在这里，他正在谈论升压转换器](http://hackaday.com/2014/09/15/afroman-demonstrates-boost-converters/)的话题，例如，[最近正在制造一个 FM bug](http://hackaday.com/2016/01/09/fm-101-and-transmitter-build-with-afroman/) 。