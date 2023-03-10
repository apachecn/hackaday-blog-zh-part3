# 认识一下机器人艺术家卡特西奥

> 原文：<https://hackaday.com/2016/04/09/if-your-robot-can-draw-sparky/>

[Robottini] [发布了他的机器人](http://robottini.altervista.org/cartesio-low-cost-cartesian-plotter-robot)Cartesio 的计划，这基本上是一个 Arduino 控制的绘图仪，用于创作艺术品。Cartesio 的好处是成本低。[Robottini]声称生产成本约为 60 美元。

这个机器人有一个 A3 大小的画床，实际上是 3D 打印机的 XY 部分。事实上，大多数零件都是 3D 打印的，机械零件包括 M8 光滑杆。LM8UU 轴承和 GT2 皮带和滑轮。如果你已经制造了一台 3D 打印机，这些零件(或类似零件)听起来应该很熟悉。

Arduino 使用 GRBL 从 GCODE 驱动电机。[Robottini]有三种不同的工作流程，可以从 Inkscape 等应用程序中生成绘图。你可以在下面看到一些结果图像。

 [![20150715_224445-640x480](img/8435c87551bc2b8d7abcf295d74e7034.png "20150715_224445-640x480")](https://hackaday.com/2016/04/09/if-your-robot-can-draw-sparky/20150715_224445-640x480/)  [![tiger](img/5906f3ea0421651bc30a30187dce90d8.png "tiger")](https://hackaday.com/2016/04/09/if-your-robot-can-draw-sparky/tiger-3/)  [![20150716_204807](img/60ddb91143f5ff360eb56193baf2886f.png "20150716_204807")](https://hackaday.com/2016/04/09/if-your-robot-can-draw-sparky/20150716_204807/) 

我们之前已经介绍过 [GRBL](http://hackaday.com/2014/09/16/usb-to-db25-adapter-uses-grbl-for-parallel-port-cnc-communication/) ，它是许多运动控制项目的核心。如果你宁愿画一些不那么永久的东西，你可以[试试这个项目](http://hackaday.com/2016/01/18/precision-cnc-drawing-with-etchabot/)。

 [https://www.youtube.com/embed/rF37Ew_WrGE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rF37Ew_WrGE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

