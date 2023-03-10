# 革新后院太阳能电池系统

> 原文：<https://hackaday.com/2017/07/19/innovating-a-backyard-solar-battery-system/>

安德烈斯·莱昂一直在寻找技术的创造性应用，他建造了一个太阳能电池系统来保持他的圣诞灯闪亮。它成功了，但是——推动创新——它现在有能力做更多的事情。

这个系统的简称是两个 100 安培小时的深循环 AGM 电池，由安装在可调角度木架上的四块 100 瓦太阳能电池板充电。然而，一旦回到设计阶段，[Leon]希望能够跟踪收集、存储和释放的电力的实时统计数据，并能够远程控制它。因此，他引入了运行 Raspbian Jessie Lite 的 Raspberry Pi，它将所有收集的数据发布到 Home Assistant 以供访问，并允许从他的智能手机的便利性控制系统。向 Pi 报告的一对 Arduino Deuemilanoves 控制为 12 V、800 W DC-交流逆变器供电的固态继电器，并监控线性电流传感器——尽管后者仍需要一些修补。休息之后，我们将对该系统进行深入的视频浏览！

 [https://www.youtube.com/embed/2U4h50DHW0A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2U4h50DHW0A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



所有的电子设备都装在一个气候控制的盒子里，当 Pi 的 CPU 变热时，它就会启动——这是在佛罗里达州的后院，伙计们——并关闭电池系统，组件之间有几个 40 安培的断路器，以确保安全。[Leon]提供了他使用的所有资源的链接，以及他在 GitHub 上的[代码](https://github.com/andres-leon/solar-system)。

我们喜欢自制的太阳能发电系统，但是如果有什么方法可以让 T2 带着它们上路就好了。