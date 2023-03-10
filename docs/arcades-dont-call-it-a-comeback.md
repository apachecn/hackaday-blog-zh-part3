# 街机:不要称之为东山再起

> 原文：<https://hackaday.com/2015/10/06/arcades-dont-call-it-a-comeback/>

视频游戏可能已经成为过去，但它们仍然存在，并且已经准备好在今年的世界创客大会上亮相。提供的不是旧的最爱，都是全新的游戏，许多是第一次展示，像期待已久的 VEC9。科学大楼的大厅里摆满了柜子，不需要任何硬币，所有的都是自由发挥。

音频街机的死亡在像[粒子锤](http://andymakes.com/particlemace/)和[88 意大利机动船](http://powerboat.robysoft.net/)这样的游戏中生效。我们个人最喜欢的是[这个](http://www.cartwheelgames.com/nothing-good-can-come-of-this/)不会有好结果。[迈克尔·p·康索利]设计了一个简单的游戏:两个玩家在一个空房间里。一颗子弹从天花板的一个洞里掉了出来，紧接着是一把枪。接下来会发生什么取决于玩家。简单的图形和游戏性赋予了这个标题它的魅力。[迈克尔]今年展示了一个新的游戏机柜。他自己建造了整个东西，一直工作到 Maker Faire 装货前的凌晨。

[Batsly Adams]、[Todd Bailey]和[Mike Dooley]联手打造了可能是几十年来第一个新的 vector arcade。 [VEC9](http://vec9.com/) 被调侃了 2 年多。他们终于完成了这个游戏，并在集会上展示了它。VEC9 始于一个由[Batsly]发现的旧的
小行星矢量监视器。

矢量显示器比光栅扫描电视更接近示波器。数模转换器产生驱动电压，控制电子束到需要的地方。结果是一个高分辨率的显示器，非常擅长画直线——而且是大量的直线。该视频系统是使用用 VHDL 编码的 Xilinx Spartan-3E FPGA 创建的。游戏逻辑本身是用很好的老式 c 语言编写的。不过矢量显示器并不是这款游戏的唯一显示器——还有一个单色光栅 CRT，可以向游戏玩家显示状态信息。这种史诗般的显示系统需要一个控制系统来匹配。该团队交付了一个真正的坦克控制轭，配有工作翼开关。

如果你不能从图片上看出来，VEC9 是关于俄罗斯母亲的。前提是 VEC9 是 1984 年造的[阴魂不散的](https://en.wikipedia.org/wiki/Dead_Hand_(nuclear_war))系统。因为它不能再联系控制者，系统已经假设苏联被美国的攻击摧毁了。报仇与否取决于玩家。查看[发布预告片](https://www.youtube.com/watch?v=rSPixmsLfn4)来真正体验这款游戏。

![sem](img/fbad5160c30f36a4757ce66900749473.png)[纽约电阻器]也没有袖手旁观。他们的街机项目是一款全身沉浸式游戏，名为[旗语英雄](http://www.nycresistor.com/2015/09/22/play-semaphore-hero-with-us-at-world-maker-faire/)。与《吉他英雄》非常相似，这款游戏要求玩家遵循屏幕上的模式，这次是用旗语而不是吉他音符。

玩家穿着一件挂有蓝色发光二极管的救生衣。带有绿色和红色发光二极管的旗语标志用于拼出旗语字母表。隐藏在黑色滤光片后面的摄像机分析发光二极管的位置，并确定玩家是否处于每个字母的正确位置。这个游戏是用 Unity 引擎用 C#编写的。纽约电阻器团队使用[单声道](http://www.mono-project.com/)在一台旧的 MAC mini 上运行它。这场比赛很艰难！我们最好的成绩是 26 分中的 11 分。

 [https://www.youtube.com/embed/KNX8vQPW8p0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KNX8vQPW8p0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

