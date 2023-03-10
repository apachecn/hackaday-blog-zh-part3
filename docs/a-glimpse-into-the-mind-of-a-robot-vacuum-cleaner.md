# 一瞥机器人吸尘器的思维

> 原文：<https://hackaday.com/2016/10/25/a-glimpse-into-the-mind-of-a-robot-vacuum-cleaner/>

当你的自主真空清洁机器人穿过房间时，它们在想什么？有不同的方法可以找到答案，比如用泥土覆盖地板，然后观察剩下的东西(一种不太理想的方法)，或者在顶部安装一个 LED，拍一张长时间曝光的照片。[Saulius]决定用鱼眼镜头从天花板附近拍摄他的机器人，然后制作结果的热图。他不满足于仅仅是一张完成的照片，他制作了一个视频，展示了遍历房间时所采取的路径，让我们一瞥算法本身。

![Looking down on the room and robot](img/e23993fcd97e12c5dc4fff7e5ab86e32.png)

Looking down on the room and robot

他使用的机器人是他借来测试的 Vorwerk VR200。在准备过程中，他清理了房间，并有策略地放置了一些障碍物，其中一些他知道机器人不会从中穿过。他启动照相机，让机器人做它的事情。然后将生成的视频文件加载到一些快速编写的 Python 代码中，这些代码使用 OpenCV 库进行背景减法、归一化、灰度化，然后进行热图绘制。每一帧都被渲染成动画 gif 和视频，如下图所示。

观看视频可以清楚地看到，机器人首先发现一个障碍，然后遍历其周界，直到它回到最初发现障碍的地方。如果障碍定义了可到达区域的外部边界，那么它通过来回穿越来填充该区域。这让我们想知道机器人程序员是否可以从绘图程序中使用的填充例程中获得一些优化提示。如果你确实想尝试其他算法，那么你可以使用 iRobot 的可黑客攻击的 Roomba 没有太多麻烦，iRobot 创建了 T1，尽管你必须添加回真空。你还会注意到它放不进房间中间的两个盒子里。我们猜测它意识到了这个遗漏的区域。你会怎么解决这个问题？

 [https://www.youtube.com/embed/wmvgq9rOU0w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wmvgq9rOU0w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

