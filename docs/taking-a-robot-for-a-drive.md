# 带着机器人兜风

> 原文：<https://hackaday.com/2017/02/27/taking-a-robot-for-a-drive/>

Instructables 用户[Roboro]有一个疯狂的 Catz Xbox 方向盘控制器，他最近没怎么用过，所以他决定破解并使用它作为机器人的[控制器，而不是](http://www.instructables.com/id/Controlling-Robot-Over-Bluetooth-Using-Xbox-Steeri/?ALLSTEPS)。

可以想象，你可以使用任何遥控车，但[Roboro]正在重复使用他几年前用于机器人相扑比赛的一辆车。打开控制器，会发现一大堆电线——令人惊讶的是，令人惊讶的是——被分组并贴上标签，使得黑客攻击过程变得不那么痛苦。当然，[Roboro]只是使用 Xbox 按钮来供电，player-two LED 来显示连接状态，轮子和踏板，但知道哪些电线可能会在以后派上用场。

车轮中的 Arduino Uno 和机器人中的 Nano 通过 CC41-A 蓝牙模块连接，尽管功能不如克隆它们的 HM10 模块，但性能令人钦佩。一段[代码](http://www.instructables.com/id/Controlling-Robot-Over-Bluetooth-Using-Xbox-Steeri/?ALLSTEPS#step6)和一个 SN754410 H 桥电机驱动器的集成 Arduino 不能为[Roboro]的机器人电机提供足够的电流——这个小机器人已经准备好进行试驾了。

 [https://www.youtube.com/embed/E3GNwqPtElA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E3GNwqPtElA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Roboro]建议的改进是机器人的伺服转向，升级到 HM10 模块，更多的传感器以利用方向盘上的其他按钮，以及一个摄像头——因为谁不喜欢一些老式的 FPV 赛车呢？