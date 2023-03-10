# 最简单的 DIY 超声波悬浮器

> 原文：<https://hackaday.com/2018/04/23/the-simplest-possible-diy-ultrasonic-levitator/>

我们认为通过声音的力量让东西悬浮在半空中更像是魔术，或者至少需要奇特的设备。事实证明，你可以很容易地用任何像样的黑客的衣柜里都应该有大量的部件自己做到这一点:一个电机驱动 IC，两个超声波距离探测器和一个微控制器。[本文向你展示如何](https://www.heise.de/make/artikel/Einfacher-Ultraschall-Levitationsapparat-4022505.html) ( [此处翻译](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=https://www.heise.de/make/artikel/Einfacher-Ultraschall-Levitationsapparat-4022505.html&edit-text=&act=url)，向下滚动)。

但是除了一些聪明的小把戏，没什么可展示的。两个 HC-SR04 超声波距离传感器是标准配置，只是被用作 40 kHz 传感器的廉价来源。该电路使用微控制器，但任何 40 kHz 方波源都应足够。你们中的那些能用 555(或树莓派)做到这一点的人，这是给你们的！步进电机驱动器会提高施加在传感器上的电压，但你也可以使用普通的晶体管。

然而，所有的小细节都很重要。您需要相当精确地定位两个超声波驱动器，以创建驻波，虽然您可以从 8.25 mm 开始并反复试验，但本文演示了使用示波器来对齐振膜，方法是驱动一个振膜，读取另一个振膜的信号，并调整它们，直到它们同相。聪明！

作者还从一个未使用的接收器上取下超声波透明格栅，用它作为勺子来帮助定位声波中的泡沫聚苯乙烯。我们一直想知道你是怎么做到的！

事实证明，做一个 DIY 的超声波悬浮书桌玩具很容易，而且没有一个零件是昂贵的或关键的。缺少的只是尝试的勇气，现在我们也有了。

尽管 HC-SR04 模块很酷，但它并不适合所有的距离感测应用。这里是你需要知道的关于他们的一切，包括让他们近距离工作的技巧。由于 HC-SR04 传感器是十个装中最便宜的，你会想知道你将如何处理其他八个。那个[问题显然也已经解决](https://hackaday.com/2017/08/30/ultrasonic-array-gets-range-data-fast-and-cheap/)。