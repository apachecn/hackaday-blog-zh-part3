# 无 Arduino 的线路跟随器

> 原文：<https://hackaday.com/2016/09/27/line-follower-with-no-arduino/>

几乎没有一天没有 Arduino 项目引发惯常的评论。一半的评论者会抱怨这个项目不需要 Arduino。另一半人会坚持认为，从 ARM CPU 到 Cray 的更大的计算机会更好地服务于该项目。

[威尔·摩尔]一直对光束机器人感兴趣——用模拟硬件代替微控制器的机器人。他的最新项目是一个复杂的线路跟随器。你可能见过“bang-bang”线跟随器，它只是用一个光电池将机器人转向一边或另一边。[Will 的]使用硬件 PID(比例积分微分)控制器。你可以在下面看到结果的视频。

看看[Will]如何利用仿真来设计一个带运算放大器和 PWM 发生器的 PID 就很能说明问题。从视频中可以看到，效果不错。

我们之前已经看过[光束](https://hackaday.com/2012/05/18/a-rocking-and-walking-beam-robot/)了。我们甚至看到了将传统光束电路与微控制器相结合的[突变体](https://hackaday.com/2013/10/13/turbot-is-a-beampicaxe-hybrid/)。但偶尔看到纯模拟版本运行还是很不错的。

 [https://www.youtube.com/embed/ued3Bk0KnHY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ued3Bk0KnHY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

