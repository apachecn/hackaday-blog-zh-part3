# Gawkerbot 在看着你

> 原文：<https://hackaday.com/2017/04/23/gawkerbot-is-watching-you/>

几个月前患流感时，[克罗马侬]看到了一个景象。一张眼睛会跟着你的脸——不管你在房间里走到哪里。他以 Gawkerbot 的形式将这一愿景变为现实。这不是一件静态的艺术品。当你走过它的视野时，Gawkerbot 的眼睛会慢慢跟着你。一旦机器人盯着你，眼睛就会发出蓝色的光。这让人怀疑这是否是一件艺术品，或者机器人的其余部分是否会穿墙而出进行攻击。

Gawkerbot 的传感系统相当简单。PIR 传感器检测房间内的运动。如果检测到任何运动，组成机器人瞳孔的两个超声波传感器开始采集数据。运行在 ATmega328 上的代码确定一个人是在左边还是右边被检测到，并适当地移动眼睛。

[克罗马侬]用一个旧的光盘驱动器光学雪橇来移动 Gawkerbot 的眼睛。虽然马达很小，但蜗杆驱动器有足够的动力来移动 3D 打印的眼睛和连杆。Gawkerbot 的主脸是一个 3D 打印版本的消防员防烟头盔。

超声波传感器可以工作，但是需要相当多的软件来驯服抖动的噪声数据流。[CroMagnon]正在考虑在 Gawkerbot 2.0 上使用 PIR 传感器。超声波传感器不仅仅是用来感应的。如果有足够的能量，[你可以和他们](http://hackaday.com/2016/05/09/an-affordable-ultrasonic-soldering-iron/)焊接。超声波甚至为[无线通讯](http://hackaday.com/2016/04/15/hackaday-dictionary-ultrasonic-communications/)服务。

休息之后，请观看视频，了解 Gawkerbot 的运行情况。

 [https://www.youtube.com/embed/K3_LWbyF0Ec?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K3_LWbyF0Ec?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

