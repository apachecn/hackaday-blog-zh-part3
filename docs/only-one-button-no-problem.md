# 只有一个按钮？没问题！

> 原文：<https://hackaday.com/2016/11/18/only-one-button-no-problem/>

有时候少即是多。在处理 I/O 引脚有限的微控制器时尤其如此。即使你有很多 I/O，有时你也需要在一个小空间里装很多。[Hugatry]的灵感来自许多手电筒上的简单界面:一个按钮。按一下它，它就打开了。再按一下，它就会切换模式。你在这些模式中循环，直到你最终关闭它。一个按钮提供多种功能。问题是你如何将电源开关用作 I/O 设备？毕竟，当你关掉电源时，微处理器就停止工作了，对吗？

【Hugatry 的】[答案很简单](http://www.hackvlog.com/2016/11/3-step-dim.html)。他将一个电阻/电容网络连接到一个 I/O 引脚(或多个引脚)。当处理器最初开启时，引脚将读取低电平，电容将充电。如果关闭电源，CPU 电压将迅速下降到零，但电容器上的电压将放电较慢。如果你等待足够长的时间并打开电源，这与第一次打开电源没有任何区别。但是如果你快速打开电源，电容电压仍然会高到足以读取为逻辑 1。

这意味着，作为启动的一部分，处理器可以检测到它最近被关闭，并采取一些行动。如果它在非易失性存储器中记住了以前的状态，你可以让代码在多个状态中循环，就像手电筒一样。你可以在下面看到一段视频。

[Hugatry]包含了一些简单的 Arduino 代码来说明这个概念。然而，这种技术非常简单，您可以很容易地将其应用到其他项目中。

认为一个按钮不足以做任何有趣的事情？[再想想](https://hackaday.com/2016/10/08/minimal-operating-system-one-button-one-led/)。话又说回来，亚马逊很可能对带有[一键](https://hackaday.com/2016/07/26/bending-the-new-amazon-dash-button-to-your-will/)的东西拥有专利。

 [https://www.youtube.com/embed/67rrjdR3EmI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/67rrjdR3EmI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

