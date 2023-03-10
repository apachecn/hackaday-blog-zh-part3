# GNU 无线电驱动示波器

> 原文：<https://hackaday.com/2015/11/22/gnu-radio-drives-oscilloscope/>

这些天我们被许多廉价的测试设备宠坏了。然而，你只需要一个示波器就可以进行大量的测量。添加一个类似信号发生器的东西，你可以做得更多。例如，频率测量的一种经典技术是使用示波器来显示李萨如图形。[Franz Schaefer]有一个视频展示了如何用 GNU Radio 生成这些有用的曲线。

正如我们之前指出的那样，GNU Radio 不一定是关于无线电的——它实际上只是一个基于 Python 的信号处理实验室。[Franz]使用 GNU Radio Companion 创建块，这些块反过来在旧的模拟示波器上创建模式。

那么，你为什么会关心利萨如模式(除了它们让你的示波器看起来像 20 世纪 50 年代科幻电影中的道具)？图案是用一种频率驱动示波器的 X 轴，用另一种频率驱动 Y 轴的结果(通常，X 轴是时间)。通过绘制两个频率的对比图，你可以了解这两个信号的很多信息。

如果两个信号具有完全相同的频率和相位，您将在显示屏上看到一条漂亮的 45 度斜线。如果相位不同，根据相对相位的不同，直线将形成一个椭圆或圆或一条斜率不同的直线(见左图)。

如果频率不同，这种模式会变得更有趣。最终的图案看起来几乎像是用肺活量描记器玩具生成的东西。通过计算循环次数，可以确定两个信号之间的关系。例如，2:1 的频率比在示波器上形成一个小蝴蝶结(两个环)。正如你在上面的图像中看到的，更高的频率比会产生更多的循环。你可以在下面的视频中看到更多的例子，或者——更好的是——加载 GNU Radio 并在你自己的示波器上尝试。对于非常懒惰的人来说，[你可以只使用你的网络浏览器](http://devadutta.net/lissajous/)。

为什么要测量相位？也许你正在[建造一个变压器](http://hackaday.com/2014/10/02/transformer-inductive-coupling-simulation-is-sfw/)。顺便说一下，这些模式是和声图的特例，如果你是机械黑客而不是电子黑客，[我们有另一个建议给你](http://hackaday.com/2010/07/02/three-pendulum-harmonograph/)。

 [https://www.youtube.com/embed/WVfdkI6twgM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WVfdkI6twgM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



克里希纳维达拉的相移模式“李沙育相位”——自己的作品。经 CC BY-SA 3.0 通过 Commons 授权-[https://Commons . wikimedia . org/wiki/File:Lissajous _ phase . SVG #/media/File:Lissajous _ phase . SVG](https://commons.wikimedia.org/wiki/File:Lissajous_phase.svg#/media/File:Lissajous_phase.svg)