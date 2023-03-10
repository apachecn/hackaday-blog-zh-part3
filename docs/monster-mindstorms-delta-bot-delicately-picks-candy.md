# 怪物思维风暴三角洲机器人微妙地挑选糖果

> 原文：<https://hackaday.com/2017/07/24/monster-mindstorms-delta-bot-delicately-picks-candy/>

来自荷兰埃因霍温 Sioux Embedded Systems 的一组嵌入式开发人员希望获得使用 Microsoft .Net 的经验。为了让这个项目变得有趣，他们在荷兰的官方乐高大会 LEGO World 上与参观者一起制作了一辆乐高火车。该团队用 C#开发了一个应用程序来实现火车的完全自动化，用 Mindstorms NXT 和 EV3 砖块以及乐高 Power Functions 马达来控制一切。

[![](img/a891950409d83c6a1504a0f26d17bd84.png)](https://hackaday.com/wp-content/uploads/2017/06/train.jpg) 火车项目带有一个简单的前提:游客从四种颜色中选择一种，火车走过去拿起一块与之相配颜色的模拟糖果。该项目名为“轨道上的 Sioux.net ”,自 2012 年以来，每年都生产新的列车，并制定了改进目标，为每个版本添加功能。具有讽刺意味的是，该设置最不有趣的部分是实际的火车和轨道。该团队的创造力在项目的两个方面脱颖而出:选择糖果颜色的方法，以及将正确的颜色分配到火车车厢中的组件。

团队成员[Hans Odenthal]已经为不同年份的火车制造了糖果抓取器。他了解了 ABB FlexPicker，并于今年[决定为布局制造一个 delta 机器人](http://www.eurobricks.com/forum/index.php?/forums/topic/150135-building-of-a-robot-flex-picker-for-lego-world-2017-by-siouxnet-on-track/)。它包括由 5×9 和 5×11 技术梁框架构成的巨大横梁，这些横梁由更多的技术梁和数百个连接桩连接在一起。三个手臂各自在一对转盘上移动，转盘被减速以提供尽可能多的扭矩——假糖果很轻，但手臂本身很重。[汉斯]最终改造了变速箱，将传动比从 1:5 提高到 1:25。

[![](img/3e7be676a8881f3eaa0c79e938ee141f.png)](https://hackaday.com/wp-content/uploads/2017/06/compressor.jpg) 手爪的“商业端”是一系列三角形的横梁，围绕着要抓取的糖果，然后三个气动执行器关闭手爪的三个手指。[Hans]创建了一个子组件来运行气动系统——本质上是一个空气压缩机。它包括一个 Mindstorms NXT 砖监测一个 Mindsensors 气动压力传感器。与此同时，一对水泵保持着油箱的注满状态。制造这样一个大型的气动组件被证明是具有挑战性的,[汉斯]被迫升级他的气动箱和管道。

我特别赞赏的是，[汉斯]还在乐高数字设计器(LEGO Digital Designer)中制作了 delta bot，这是一个乐高免费分发的虚拟建筑工具。除了能够在没有零件的情况下制作出一件作品的原型之外，LDD 还擅长保存乐高作品以备将来重建。你做了一些很酷的东西，但需要另一个项目的零件吗？只要虚拟地构建它，你就可以随时重新创建它。

[![](img/e9c0725f2c7c2c1d71e8e0099a05b311.png)](https://hackaday.com/wp-content/uploads/2017/06/gantry.jpg) 这只手臂并不是[汉斯]生产的唯一一只夸张的糖果抓取器。2016 年的版本是一个[巨型龙门架](https://www.flickr.com/photos/siouxnetontrack/sets/72157660645729093)，可以安装在许多火车轨道上。龙门起重机具有爪式抓手，还包括由乐高零件制成的非常酷的电缆托架。参观者转动一个彩色转盘来选择糖果的颜色，用颜色样本装饰的卡片通过扫描仪，发送给火车去取正确种类的糖果。

[汉斯]还在一个令人印象深刻的 Mindstorms 手臂上工作。最初，它是 2017 年时装秀的糖果抓取器，但当[汉斯]受到启发，创造了一个三角洲机器人，它被搁置一旁。然而，这个尝试有很多值得喜欢的地方，有 6 个自由度和一个气动手爪，我可以看到这个版本对 delta bot 的改进。

为了跟随团队和他们的建设，[查看他们的博客](https://siouxnetontrack.wordpress.com/)，观看他们的 [YouTube 视频](https://www.youtube.com/user/siouxnetontrack)，或者[在 Flickr 上查看他们的照片](https://www.flickr.com/photos/siouxnetontrack/)。

 [https://www.youtube.com/embed/RsXVT973cLE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RsXVT973cLE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/HT6-U7wzmbs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HT6-U7wzmbs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

