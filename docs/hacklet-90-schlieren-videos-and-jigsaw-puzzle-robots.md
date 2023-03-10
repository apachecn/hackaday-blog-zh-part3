# Hacklet 90:纹影视频和拼图机器人

> 原文：<https://hackaday.com/2016/01/09/hacklet-90-schlieren-videos-and-jigsaw-puzzle-robots/>

新年快乐，欢迎来到 2016 年第一期 Hacklet！Hacklet 是我最喜欢写的专栏之一，因为我可以在 [Hackaday.io](https://hackaday.io) 谈论人们正在进行的伟大项目。通常这些文章遵循一个主题，但今年是新的一年，我将尝试一些新的东西。作为 Hackaday 的社区编辑，我密切关注 Hackaday.io 上的新项目和更新项目。每周我都会看到让我感到惊讶、印象深刻和鼓舞的项目。本周，我将重点介绍我认为非常棒的一对夫妇。

[![torch](img/2dd6a6d7e5d49ae6c4d2d5d81d7dd0e9.png)](https://hackaday.io/project/9034) 【嘉娜·玛丽】创建了[纹影摄影](https://hackaday.io/project/9034)项目。纹影摄影用于拍摄液体中密度的变化，包括捕捉空气中的密度变化。超级和高超音速风洞经常使用这种技术来显示测试模型周围的气流。在风洞之外，纹影非常适合显示由于热量或不同气体引起的密度变化。这正是[Jana]在这个项目中所做的。

有几种方法可以创建纹影图像，从激光，衍射光栅，到刀片都可以使用。[Jana]正在使用一个简单的莫尔图案和一些视频技巧来捕捉纹影视频。当密度变化使来自莫尔条纹的光弯曲时，高密度莫尔图案将出现闪烁。[Jana]只需拍摄一张参考图像，然后从实时视频中减去该图像。减法的结果就是你在上面看到的纹影图像。[Jana]不仅解释了她用来制作视频的技术，她还上传了一个处理草图，执行视频减法魔法。

[![jigsolve](img/9445dfce893d20659f84d8df2d2ed2b6.png)](https://hackaday.io/project/9055-jigsolve) 【丹·罗耶】有一个更家庭化的问题——他的家人喜欢开始拼图游戏，但似乎从来没有完成过。他决定邀请大约 30 亿他最亲密的朋友，以联网拼图机器人 [JigSolve](https://hackaday.io/project/9055) 的形式。JigSolve 的笛卡尔平台是基于 [CoreXY](http://corexy.com/) 的设计。[Dan]使用 CoreXY 作为指导方针，但自己设计和构建硬件。电子硬件方面借鉴了 RepRap 3D 打印机。Arduino Mega2560 和斜坡板控制两个 NEMA 17 步进电机。Arduino 正在运行来自 [Makelangelo【丹】自己的开源艺术机器人](http://www.makelangelo.com/)的固件。

该项目的互联网连接部分以基于 Java 的 IRC bot 的形式出现，并连接到 Freenode IRC 网络。连接互联网的大众将不得不看到他们在做什么，所以罗技网络摄像头将视频流传到网上。

到目前为止，JigSolve 最难的部分是喷嘴。很像 SMT 拾取和放置机器，吸嘴需要用真空拾取零件，然后将它们旋转到所需的方向。[Dan]正在研究不同种类的硅，他在寻求建议。停留在[项目页面](https://hackaday.io/project/9055)上，帮他一把！

这就是本周的 Hacklet。一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！