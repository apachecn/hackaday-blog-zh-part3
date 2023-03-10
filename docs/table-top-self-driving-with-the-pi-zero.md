# 圆周率为零的桌面自动驾驶

> 原文：<https://hackaday.com/2017/09/16/table-top-self-driving-with-the-pi-zero/>

自动驾驶技术现在是一个热门话题，因为各大公司都在争先恐后地推出更强大的自动驾驶汽车。游戏的顶端有很高的进入门槛，但这并不意味着你不能在家修补。[【理查德·克劳德】一直在家里用树莓派 Zero 打造自动驾驶汽车。](https://hackaday.io/project/27173-a-self-driving-car-using-a-raspberry-pi-zero)

![](img/246e8390ee29d2f165fde4abbc46e324.png)

The self-driving model is trained by first learning from the human driver.

[Richard]的项目基于 [EOgma Neo 机器学习库](https://github.com/ogmacorp/EOgmaNeo)。使用一种称为稀疏预测层次或 SPH 的机器学习类型，该算法首先根据用户输入进行训练。[Richard]驾驶模型在一条小跑道上跑来跑去。该算法考虑了来自人类驾驶员的转向和油门输入，还监控来自 Raspberry Pi 摄像机的反馈。在对模型进行几圈训练后，汽车就可以自动驾驶了。

从根本上说，这是在比全尺寸自动驾驶汽车简单得多的层面上工作。[如视频所示](https://www.youtube.com/watch?v=9GNbVkMb8Qw)，转向角是根据摄像机输入的灰度像素数据预测的。赛道非常简单，墙壁与驾驶表面的对比使机器学习算法更容易计算出它应该去哪里。观看视频让我们想起多年前简单的循线机器人；这个项目以完全不同的方式达到了类似的效果。就目前的情况来看，这是一个关于如何使用机器学习系统的很好的学习项目。

[Richard]的文章包括如何复制构建的说明，如果你刚刚开始机器学习项目，这很好。令人印象深刻的是，这个版本实现了它所做的事情，只需要一分钟树莓 Pi Zero 的马力，并将其全部放在一个只有 102 克的包装中。我们以前见过类似的依靠更大马力的建造——在处理和推进方面。

 [https://www.youtube.com/embed/9GNbVkMb8Qw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9GNbVkMb8Qw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

