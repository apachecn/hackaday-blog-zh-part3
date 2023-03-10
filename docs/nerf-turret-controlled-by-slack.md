# 由松弛控制的 Nerf 转台

> 原文：<https://hackaday.com/2016/02/15/nerf-turret-controlled-by-slack/>

当你给一个前海军武器工程师一些开发板，让他去造“很酷的东西”，会发生什么？当你给一个孩子指画时会发生什么？[Seb]显然建造了一个通过团队通信 app 控制的[物联网 Nerf 炮塔炮。](https://www.bluechilli.com/blog/introducing-the-turret/)

该武器是一个 Nerf 踩踏被黑客攻击，所以它可以电子发射。安全开关被旁路，继电器提供点火信号。电子堆栈由一个[英特尔伽利略](http://www.intel.com/content/www/us/en/embedded/products/galileo/galileo-overview.html)、一个电机屏蔽和一个继电器屏蔽组成。炮塔组件是使用[机器人](https://www.sparkfun.com/actobotics)的现成结构部件建造的。步进电机为转台提供运动。乐趣始于软件是如何实现的。一个 [iBeacon 网络](http://www.spaceconnect.co/)检测人们在办公室坐在哪里。因此，当你在一个信息应用程序中输入你的目标的名字时，它知道他们坐在哪里，瞄准他们，并向他们发射一枚 nerf 飞镖。

吸取的经验教训使得这些项目物有所值。比如 USB 就是一个标准。标准规定 USB 电缆不能超过 1.8 米长。当[Seb]的电子设备在工作台上工作时，他想起了这一点，但当他被放置在原位并通过一根 3m 长的电缆连接时，他拒绝工作——串行链路就是不起作用。

将枪安装得非常平衡是另一个挑战。最终，他不得不使用几个粘在枪前面的 AA 电池来使它正确。这可能是有用的，因为他计划用一个照准相机来代替静重。最后一次破解是把散热器和马达驱动器绑在一起，他有一个很好的理由这么做。请在他的博客中了解更多信息。通过团队消息应用程序 [SLACK](https://slack.com/) 查看视频，看有人瞄准并射击目标。

 <https://video.twimg.com/ext_tw_video/692937338297696256/pu/vid/1280x720/V9u-YzT2CC4ImeZN.mp4?_=1>

[https://video.twimg.com/ext_tw_video/692937338297696256/pu/vid/1280x720/V9u-YzT2CC4ImeZN.mp4](https://video.twimg.com/ext_tw_video/692937338297696256/pu/vid/1280x720/V9u-YzT2CC4ImeZN.mp4)