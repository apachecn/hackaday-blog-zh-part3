# Hackaday 奖参赛作品:中风后痉挛康复助手

> 原文：<https://hackaday.com/2017/09/21/hackaday-prize-entry-post-stroke-spasticity-rehab-helper/>

当流向大脑的血液不足导致细胞损伤，导致大脑的这一部分停止运作时，就会引发中风。常见原因是血管堵塞或内出血，影响取决于大脑受影响的部分。在大多数情况下，痉挛(肌肉收缩)，不良的运动控制和无法移动和感觉是常见的后果。恢复通常是一个漫长而缓慢的过程，需要重新学习受影响的技能。这就是使用辅助技术的物理治疗变得重要的地方。康复必须尽早开始，因为最初几周对良好的恢复至关重要。[Sergei V. Bogdanov]正在制造一种廉价而简单的中风后痉挛康复助手来解决这个问题。

他正在使用十个连接到 Arduino Nano 的业余微型伺服系统，所有这些都安装在厨房的案板上，并加入一些其他部件来完善这一构建。每个手指都有一对伺服系统。五连杆机构将伺服旋转转换成二维运动。连杆的末端有一个旋转金属盘。患者的手指通过磁性金属垫附着在这些圆盘上，磁性金属垫使用胶带附着在手指末端。两个按钮可在多种锻炼模式中循环，两个电位计可帮助调节速度和平滑度(为所需运动计算的点数)。连接到 Arduino 的两个 7 段 LED 显示模块提供了一个可视界面，显示程序模式、速度、循环次数和其他相关信息。复制该项目应该非常简单，因为该设备使用现成的部件，使用[Sergei]项目页面上发布的详细构建说明、照片和代码，可以很容易地将这些部件组装在一起。看看下面的视频，看看康复助手的行动。

 [https://www.youtube.com/embed/KH-IJ0NU5pE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KH-IJ0NU5pE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/LWCHI8DpslQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=32&wmode=transparent](https://www.youtube.com/embed/LWCHI8DpslQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=32&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)