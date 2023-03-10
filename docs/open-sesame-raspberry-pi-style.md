# 芝麻树莓派风格

> 原文：<https://hackaday.com/2015/12/17/open-sesame-raspberry-pi-style/>

[Don]在他妻子的车上安装了一台 Android 平板电脑，并意识到他想让它操作和监控车库门。他最大的挑战？满足(他所指的)WAF 或妻子接受因素。他决定在树莓派上使用网络应用程序[，以及一些开关和继电器](http://dhowdy.blogspot.com/2015/10/opening-garage-door-from-internet.html)。他的目标很简单:

*   提供门的状态(开/关/未知)
*   打开和关闭门
*   跨多个平台工作
*   足够安全，可以连接到互联网
*   可靠且简单

Pi 使用两个开关来确定门的位置，并使用继电器来触发现有车库门遥控接收器的操作按钮。这个简单的电路可以服务于许多不同的目的，不仅仅是打开车库门。如果出于其他目的需要一个以上的开关，复制继电器驱动器也很容易。

这个网络应用程序可以在 [GitHub](https://github.com/dhowdy/GarageDoor) 上下载。有一个很酷的 SVG 动画(见左)显示了门打开和关闭时的状态——大概是为了帮助 WAF 升高。对于那些刚刚接触 Pi 或 Web 应用的人来说，这将是一个很好的起步项目。今年早些时候我们看到了很多[车库门开启器](http://hackaday.com/2015/02/23/another-garage-door-opener-this-time-with-security/)，包括[一个猫用的](http://hackaday.com/2015/02/17/automatic-garage-door-opener-takes-the-cake/)。尽管如此，我们喜欢这一个的简单和迷人的动画。