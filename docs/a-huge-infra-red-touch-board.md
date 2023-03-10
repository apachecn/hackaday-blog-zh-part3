# 一块巨大的红外线触摸板

> 原文：<https://hackaday.com/2017/04/11/a-huge-infra-red-touch-board/>

我们都习惯了笔记本电脑上的触摸板和触摸屏。现在有一种预期是，一款带屏幕的新设备将支持触摸功能。

然而，对于非常大的表面，触摸仍然是一种昂贵的奢侈品。如果你是一个硬件黑客，除非你足够幸运地获得一个特殊的抛弃物，在一个装备良好的教育机构中偶尔瞥见一个微软 PixelSense 或交互式白板将是你可能得到的最好的机会。

[Adellar Irankunda] [也许能满足你对大尺寸触控板的需求](http://www.instructables.com/id/Inexpensive-Wireless-Interactive-Board/)如果你手头不宽裕，他用一种有趣的方法做了一个，用一排红外发光二极管和光电晶体管包围触控区域。通过研究阵列中不同发光二极管对光电晶体管的照射，他可以计算出任何物体的位置，比如进入空间的手指。这是一种古老的技术，你可能在早期的触摸屏 CRT 显示器上发现过。

他的硬件建立在安装在一个正方形中的 12 个试验板上，其上有 144 个 LED/光电晶体管对，由一对 Arduino Nanos 通过一堆 4051 CMOS 多路复用器管理。如果你自己喜欢一个，他提供了所有的代码，尽管要组装的复杂的电路板阵列可能不适合胆小的人。你可以在我们发布在休息时间下方的视频中看到它的运行。

 [https://www.youtube.com/embed/FLSvA2DQJQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FLSvA2DQJQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



对于一个大型指点设备来说，这是一个可信的努力，但公平地说，这项技术已经取得了进展。我们之前已经向你展示了使用红外网络摄像头的多点触控桌子，如果你想要一个真正漂亮的桌子，那么 T2 这款 Kinect 驱动的 3D 显示器怎么样？