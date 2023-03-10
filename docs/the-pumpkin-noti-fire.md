# 南瓜不着火

> 原文：<https://hackaday.com/2016/10/28/the-pumpkin-noti-fire/>

每个人在年轻的时候都有一段插曲，包括使用喷雾作为即兴喷火器。拿一些轻度醉酒的青少年来说，给他们一个除臭剂罐和一盒火柴，他们中的一两个人迟早会掉眉毛。

对我们大多数人来说，一个有趣的青少年时期的插曲是气雾喷火器仍然存在。然而，当上周对 DNS 基础设施的 DDoS 攻击夺走了他的工作能力时，人们的注意力转向了一个万圣节项目。他创造了一个雕刻南瓜，当收到短信或电子邮件时，它会喷火作为通知信号。

![flame-test](img/a4a81744ace7e9dbefaaefc7c4e0d539.png)该项目的关键是[林间空地自动喷雾空气清新剂](https://www.glade.com/en/products/sprays/automatic-spray)。这是一个电池供电的装置，带有一个由电子定时器或按钮开关控制的喷雾罐。拆下开关，其线路显示为喷雾的低电平有效触发器。[Mike]用来自微控制器的线路替换了开关，并在喷嘴前放了一根点燃的茶光蜡烛，以获得完全可控的(如果不是完全安全的)火焰喷射器乐趣。早期的测试证明了这个概念，所以剩下的只是雕刻南瓜和安装系统。

在这种情况下使用的微控制器是 [Lightblue Bean](https://punchthrough.com/bean) ，尽管几乎任何类似的电路板都可以放在它的位置上。通知是通过蓝牙从 iPhone 经由 [ANCS](https://developer.apple.com/library/content/documentation/CoreBluetooth/Reference/AppleNotificationCenterServiceSpecification/Introduction/Introduction.html) (苹果通知中心服务)处理的，Bean 可以查询它来触发它的 fiery 警报。有一个简短的视频显示，该设备在行动中烧伤[迈克]的手，我们把它放在休息。

 [https://www.youtube.com/embed/ScVQEZZuLLU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ScVQEZZuLLU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们之前已经展示了一些带有[蜡烛点火](http://hackaday.com/2015/10/16/make-a-cheap-and-dangerous-automated-flamethrower/)和[火花隙](http://hackaday.com/2015/12/16/rc-mini-flame-thrower-brings-the-burn/)的气溶胶火焰喷射器，尽管没有一个使用方便的 Glade 机制。这并不是说我们不喜欢电子清新剂，不管是[修理它们的动作](http://hackaday.com/2008/12/02/stop-wasting-your-air-freshener/)控制、[把它们当作机器人](http://hackaday.com/2011/03/07/remote-controlled-robot-toy-from-air-freshener-parts/)，还是[为它们刮擦最后一个零件](http://hackaday.com/2010/09/24/gutting-an-air-freshener-for-the-parts/)。

哦，我们在骗谁，你只是想看火。请允许我们向您介绍[腕式丙烷喷火器](http://hackaday.com/2014/09/25/a-wrist-mounted-flamethrower-sure-why-not/)。