# 基于 ARM 的手势遥控

> 原文：<https://hackaday.com/2015/12/13/arm-based-gesture-remote-control/>

当我们对着电视挥手时，它什么也不做。不过，你可以用一个 ARM 处理器和一些传感器来改变这种情况。你可以在下面看到该项目的视频。[Samuele Jackson]、[Tue Tran]和[Carden Bagwell]使用手势传感器、声纳传感器、红外 LED 和红外接收器以及支持 mBed 的 ARM 处理器来完成这项工作。

接收器允许设备从现有遥控器加载 IR 命令，因此手势遥控器将适用于大多数设置。mBed 库处理与传感器和通用远程功能的通信。它还提供了一个简单的实时操作系统。这就在 [main.cpp](https://developer.mbed.org/users/cardenb/code/mbed_gesture/file/35878487eafe/main.cpp) 中留下了一些简单的逻辑，不到 250 行源代码。

遥控器让我们想起了今年早些时候我们报道的一个黑客项目，该项目使用相同的[声纳模块来控制电脑音量](http://hackaday.com/2015/10/07/bootstrapping-motion-input-with-cheap-components/)。如果你不喜欢电视，你可以随时使用[手势来控制你的无人机](http://hackaday.com/2014/10/16/controlling-a-quadcopter-with-gestures/)。

 [https://www.youtube.com/embed/ekOjm8Pc0e0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ekOjm8Pc0e0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

