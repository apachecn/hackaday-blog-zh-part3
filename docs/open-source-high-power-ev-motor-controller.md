# 开源高功率电动汽车电机控制器

> 原文：<https://hackaday.com/2017/09/11/open-source-high-power-ev-motor-controller/>

对于任何对电动汽车感兴趣的人来说，尤其是对电动汽车的驱动和控制系统感兴趣的人，无尽领域论坛是经常去的地方。它充满了一些令人惊叹的项目，涵盖电动滑板到汽车以及介于两者之间的一切。[马科斯·恰帕罗]最近公布了他的控制器项目的细节——[VESC 控制器](https://endless-sphere.com/forums/viewtopic.php?f=30&t=89056)，一种能够驱动高达 200 马力电机的开源控制器。

[Marcos]的控制器是[Benjamin Vedder] 的[VESC 的一个分支，他在论坛中有一群近乎狂热的追随者，因为“创造了所有 DIY 电动滑板制造商一直渴望的东西，一个开源、高度可编程、高电压、可靠的速度控制器，用于 DIY eboard 项目”。我们已经在 Hackaday 采访了](https://endless-sphere.com/forums/viewtopic.php?f=31&t=66958&hilit=VESC#p1007172)[几个 VESC 项目](https://hackaday.com/?s=VESC+vedder)。

![](img/08d46295b04a00a8607860d903bd3b1a.png)虽然[Vedder]的控制器针对的是滑板电机等低功耗应用，但[Marcos]的版本将其放大了几个等级。它使用 600 V 600 A IGBT 模块和 460 A 电流传感器，能够为 BLDC 电机提供高达 150 kW 的功率。由于控制逻辑与栅极驱动器和 IGBT 分离，因此可以将其用于高功率应用。所有的设计文件都可以在 [Github 库](http://www.github.com/paltatech/VESC-controller)上找到。这个令人惊讶的构建的特性列表太长了，最好去论坛查看一下细节。马科斯已经在考虑在下一次改版中去掉所有的模拟传感，改用带数字输出的电压和电流传感器。他认为使用 FPGA 加闪存可以取代材料清单中的大部分模拟部件。这将消除与模拟器件相关的容差、漂移和噪声问题。

[Marcos]还致力于改进电源接口板的参考设计，包括栅极驱动器、功率 mosfets、DC 链接和差分电压/电流检测。这个接口板的设计文件也可以从他的 [GitHub](https://github.com/paltatech/VESC-controller/tree/master/adaptor%20boards/power_integrations_2SP0115T2A) repo 中获得。根据马科斯的说法，有了更好的传感器和更强大的功率级，同样的控制板应该可以为超过 500 马力的电机工作。休息之后，请观看视频，视频显示 VESC 控制者正在接受初步测试。

 [https://www.youtube.com/embed/7G35nryvwx8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7G35nryvwx8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

