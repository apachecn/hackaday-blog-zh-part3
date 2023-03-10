# Hackaday 奖参赛作品:用于教育的微型机器人

> 原文：<https://hackaday.com/2016/06/14/hackaday-prize-entry-micro-robots-for-education/>

[Joshua Elsdon]和[Thomas Branch]需要一个教育硬件平台，以适应大学班级有限的空间和预算。因为没有足够便宜、简单和功能强大的机器人适合他们的项目，帝国理工学院机器人学会的两位机器人老师开始建造他们自己的机器人——并带着一个开源微型机器人军团进入了 Hackaday 奖。

这些小型机器人的底部面积为 2 厘米，一旦批量生产，每个机器人的价格约为 10 英镑(约 14 美元)。它们具有两个板载步进电机、一个 RGB LED、电池、一个线跟踪传感器、碰撞传感器和一个双向红外发射器，用于与主系统“上帝机器人”通信。主系统基于 Raspberry Pi，几乎没有额外的硬件。它与所有的小机器人进行多路红外通信，同时通过摄像头跟踪它们的位置和方向，通过它们的彩色机载 LED 识别它们。主系统还为机器人提供了一个编程接口，因此学生无需刷新固件就可以运行他们的代码。这是一个设计良好、低成本的多机器人系统，通过机载传感器、步进电机里程计和绝对定位反馈，这些小机器人可以学习相当多的技巧。

[![](img/df49011de51899c15f740f8cfa4bbe08.png)](https://hackaday.com/2016/06/14/hackaday-prize-entry-micro-robots-for-education/micro_robots_reworking/)[![](img/63a347d668a67c1af6e4c23a7bf78d46.png)](https://hackaday.com/2016/06/14/hackaday-prize-entry-micro-robots-for-education/micro_robots_assembled/)[![](img/942a24f61561303e8f68fa58a917b96f.png)](https://hackaday.com/2016/06/14/hackaday-prize-entry-micro-robots-for-education/micro_robots_wheels_tests/)[![](img/82fbc2f3183004ea99d82d683696cd57.png)](https://hackaday.com/2016/06/14/hackaday-prize-entry-micro-robots-for-education/micro_robots_batch/)

建造微型机器人面临着许多常规大小的挑战，我们很高兴跟随[Joshua Elsdon]和[Thomas Branch] [踏上他们的旅程](https://hackaday.io/project/11399/logs)，从组装微型 PCB 到试验 3D 打印和铸造技术生产微型轮子，再到 ROS 编程。勤奋的二人组两次出现在 Hackaday 奖中:他们自己的微型机器人项目和他们对之前报道的 [ODrive](http://hackaday.com/2016/05/23/hackaday-prize-entry-industrial-servo-control-on-the-cheap/) 的贡献——一个开源的 BLDC 伺服控制器。我们已经很好奇他们的下一个壮举了！下面的视频显示了摄像头反馈集成到 ROS 的成功测试。

 [https://www.youtube.com/embed/c5IDkxOKeu0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/c5IDkxOKeu0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)