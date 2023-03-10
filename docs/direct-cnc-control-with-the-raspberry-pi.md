# 使用 Raspberry Pi 进行直接 CNC 控制

> 原文：<https://hackaday.com/2018/05/15/direct-cnc-control-with-the-raspberry-pi/>

如果你正在建造一个数控路由器，激光切割机，甚至是 3D 打印机，你通常会看到一个专用的控制器。该板接收来自计算机的命令，通常以 g 代码的形式，并将其解释为连接的步进电机的运动命令。从历史上看，这是一种不可避免的邪恶，因为真的没有办法用足够快的计算机直接控制步进电机。情况可能不再是这样了。

[![](img/807c7d634c2a3ebfaeb906c66c3a96ea.png)](https://hackaday.com/wp-content/uploads/2016/09/tmc_bottom.jpg)

A stepstick driver

多亏了 Raspberry Pi(和类似的主板)，我们现在有了带有大量 GPIO 引脚的 Linux 计算机。唯一缺少的是解释 g 代码和通过 GPIO 命令步进器的软件，多亏了[pantadeusz]，我们现在有了。[该软件名为 raspigcd，它解释 g 代码的子集](https://github.com/pantadeusz/raspigcd),对连接的步进机进行实时控制，速度足以驱动小型 CNC 路由器。

当然，你不能直接控制一个强大的步进电机到 Pi 的 GPIO 管脚。你会放出所有的魔法烟雾。但是你可以直接把它连接到步进驱动板上。这些小模块连接到一个专用电源，并处理步进器的相当大的电流消耗，你需要做的只是向它们提供步数和行进方向。

这种直接控制的方法为小型、低成本的 CNC 项目提供了一些非常有趣的可能性。你不仅可以跳过控制板，还可以在同一个界面上操控机器的用户界面(直接通过触摸屏或者通过网络)。

在过去的中，我们已经看到了创建[一体化 Linux 步进控制器的尝试，但事实上，任何拥有 Raspberry Pi 2 或 3(该软件目前已在其上测试的主板)的人都可以参与其中，这应该真正有助于推动开发。有人用过这个吗？](https://hackaday.com/2018/03/25/turning-the-beaglebone-on-a-chip-into-a-3d-printer-controller/)