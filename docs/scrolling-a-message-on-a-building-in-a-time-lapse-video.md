# 在延时视频中滚动建筑物上的信息

> 原文：<https://hackaday.com/2016/01/26/scrolling-a-message-on-a-building-in-a-time-lapse-video/>

[Saulius Lukse]有一种非常有趣的方式将几栋建筑变成他自己的可寻址显示器。这种效果在现实生活中是看不到的，但这是一个巧妙的视频渲染，用的是他从延时相机中提取的素材。现在，如果你想在建筑物的窗户上玩俄罗斯方块，你可以在每个窗户上安装无线灯泡。但那是很大的工作量。你可以假装玩俄罗斯方块(或者在这种情况下滚动消息),如果你只是展示一个建筑物的视频，并交换你自己的图像处理。

![4](img/cc89eb15fba4c2c45b5f50844bbc7bf4.png)

[Saulius]从一个城市景观的延时序列开始。它需要有一个或两个大建筑，以提供一个良好的滚动表面。建筑物从背景透明的场景中提取出来。真正耗时的部分是创建一个独特的图像，为每个将要使用的窗口点亮一个窗口。这组窗口是用来创建滚动图像的“像素”。这是通过在关闭所有办公室灯的情况下遮蔽建筑物的一个图像，然后在办公室照明的情况下单独遮蔽每个窗户来实现的。这种遮蔽意味着建筑周围发生的一切(交通、天气、人)都将被保留，而窗户可以单独操作。

接下来，程序 [jinx](http://www.live-leds.de/) 用于创建建筑动画。这个程序被设计用来在 LED 面板上创建滚动消息。[Saulius]提供了一个 Python 脚本，该脚本获取 jinx 的输出图像，并将它们组合起来以创建最终的运动图像集。

结果是一座城市祝你“新年快乐！”

 [https://www.youtube.com/embed/KczYUK2eIXY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KczYUK2eIXY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

