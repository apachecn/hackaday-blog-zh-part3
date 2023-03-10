# 从头再来

> 原文：<https://hackaday.com/2016/01/28/back-to-the-drawing-board/>

试过用鼠标或轨迹球签名吗？没那么容易。你可以买一个带笔的图形输入板。拉胡尔·罗摩克里希南有一种不同的方法。他拿了两个 10 转的罐子，系上一些绳子和一个垫圈。一支铅笔穿过垫圈，一只比格犬阅读罐子以确定它在纸上画的是什么。几个可伸缩的徽章挂绳保持绳子的张力。

这种巧妙的设计很容易用任何能读取两个电位计的微控制器来复制。唯一尴尬的部分是，当你想让设备将铅笔视为向下时，需要按下一个按钮(见下面的视频)。可能很容易在铅笔上安装一些开关，使操作更平稳一些。

在计算机端，[Rahul]包含使用 Processing.js 和 BoneScript 库来捕获输入绘图的 HTML 代码。当然，真正的平板电脑不会这样工作，但这是一种非常简单的方法来获取铅笔的 X 和 Y 坐标。我们已经在逻辑分析仪和[的核心](http://hackaday.com/2015/01/31/passion-project-turns-beaglebone-into-standalone-super-nes/)[看到了小猎犬骨，甚至在超级 NES](http://hackaday.com/2015/05/19/hackaday-prize-entry-a-beaglebone-logic-analyzer/) 的重新设计中也是如此，并且该板以拥有强大的马力而闻名，同时仍然拥有[功能的真实世界 I/O](http://hackaday.com/2014/06/22/an-introduction-to-the-beaglebone-pru/) 。

 [https://www.youtube.com/embed/Adoah9AO_zU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Adoah9AO_zU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

