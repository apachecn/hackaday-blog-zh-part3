# 克里斯塔尔·戈登:传感器、融合和神经生物学

> 原文：<https://hackaday.com/2017/12/12/christal-gordon-sensors-fusion-and-neurobiology/>

有些事情听起来不像是应该在一起的，但它们确实在一起。花生酱和巧克力。奶油蛋糕和油炸食品。培根和枫糖浆。有时候把事情混在一起会产生很好的结果。[克里斯塔尔·戈登博士]的专业知识就属于这一类。她是一名电气工程师，但她也研究神经科学。这可以导致一些有趣的知识分子里斯的花生酱杯。

在 2017 年 Hackaday 超级大会上，【Christal】[谈到了传感器融合](https://www.youtube.com/watch?v=VCTyxR3VgCY)。如果你做过有多个传感器的系统，你可能以前遇到过这种情况，即使你没有这样称呼它。然而，[Christal]带来了生物系统如何融合传感器数据与电子系统如何执行类似任务的对比视角。你可以在下面的视频中看到她讲话的视频回放。

[![](img/cf42a58f09716000d54b50b04ec3fff3.png)](https://hackaday.com/wp-content/uploads/2017/12/nsensor.png) 传感器融合的精确定义是从多个传感器获取数据，以减少测量的不确定性。例如，自动驾驶汽车可能想要测量其相对于其他物体的位置，以导航和避免碰撞。全球定位系统会给你一个很好的位置概念。然而，你可以使用[惯性方法](https://hackaday.com/2013/07/31/an-introduction-to-inertial-navigation-systems/)在 GPS 的不确定性范围内更好地了解你的位置，尽管它们往往会在更长的时间内积累误差。通过使用两种来源的数据，有可能比试图单独使用任何一种更好地了解位置。

另一个数据来源可能是激光雷达或超声波测距仪。Fusion 将所有这些数据关联起来，以形成更好的环境运行状况。当然，导航并不是唯一的应用。[Christal]提到了其他几个项目，包括融合数据，让机器人腿在跑步机上跑步。

[Christal]提到的一个非常重要的传感器融合工具是[卡尔曼滤波器](https://hackaday.com/2012/09/10/kalman-filter-keeps-your-bot-balanced/)。该算法采用具有不同确定度的多个噪声传感器输入，并得出比单独的传感器输入更精确的值估计。

我们从生物系统中寻找传感器融合的灵感是有道理的。毕竟，我们所知道的最好的融合系统是人脑。你的大脑处理来自令人眼花缭乱的传感器阵列的数据，并让你对你的世界有所了解。它并不完美，但在大多数情况下确实运行得很好。想象一下，比如说，一只候鸟的导航能力。现在想想那只鸟的大小和重量。然后意识到这种鸟可以自我补充燃料，并且可以——在一点帮助下——产出更多的鸟。相当惊人。我们的机器人很幸运，如果他们能很好地导航，他们可能不加油和重建，加上他们可能更大更重。

你在 40 分钟内只能涵盖这么多，但[Christal]将让你思考我们的系统如何类似于生物系统，以及我们如何结合来自多个来源的数据，以在机器中获得更好的传感器数据。

超级会议最大的好处之一就是可以接触到观点非常不同的人的新观点。[克里斯塔尔的]谈话是一个很好的例子，感谢互联网的魔力，你可以在自己的客厅里观看。

 [https://www.youtube.com/embed/VCTyxR3VgCY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VCTyxR3VgCY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

