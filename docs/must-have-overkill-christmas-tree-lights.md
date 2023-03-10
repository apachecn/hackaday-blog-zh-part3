# 必备过度装饰圣诞树灯

> 原文：<https://hackaday.com/2015/12/30/must-have-overkill-christmas-tree-lights/>

圣诞之火熄灭了，所以我们开始收到今年的圣诞礼物。[Chris]给我们发来了他令人敬畏的视频映射树照明技术。他的项目巧妙地利用了一系列很酷的工具，所以即使你没有想到明年 12 月，也值得一看。静态图像没有做到公正；请看休息时间下面的视频。

最终结果是一串可寻址的 WS2812B LEDs 连接到一个 Raspberry Pi Zero，即使它缠绕在一个大致圆锥形(松树)的物体上，也可以显示视频图像。但这实际上比你最初想象的更令人印象深刻；如何将平面图像映射到缠绕在树上的一串发光二极管上？

[Chris]的解决方案是编写一个例程，以独特的模式点亮 led，然后使用 OpenCV 和网络摄像头检测它们，直接进行映射。然后，他从一段视频中的图像中，在像素位于树上的准确点上进行采样，并将数据发送给 led。

这里的基本框架应该很容易转换成一个随机放置的 led 的通用图像映射程序，所以我们认为这是一个比这一季更持久的黑客。因为它运行在 Pi Zero 上，所有东西都是用 Python 写的，所以对于初学者来说，这是一个很好的复制项目。然而，项目页面上的代码部分仍然将其列为即将推出。我们希望如此！

 [https://www.youtube.com/embed/Sd6lr40pnu0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Sd6lr40pnu0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

