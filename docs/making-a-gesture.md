# 做个手势

> 原文：<https://hackaday.com/2016/10/10/making-a-gesture/>

 [https://www.youtube.com/embed/rxWCJmp54sw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rxWCJmp54sw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



当[克里赫]切换键盘时，他失去了音量控制。所以他决定用一个 Arduino、一个旧软盘盒和一个 [Hover Labs 悬浮板](http://www.hoverlabs.co/products/hover/)(不是回到未来的那种)一起[做一个。你可以在下面的视频中看到结果。](https://hackaday.io/project/15867-gesture-based-pc-volume-control)

你会在视频中注意到，该设备读取一个类似圆形音量控制的“旋转”动作。该程序将模拟键盘按键发送到 PC 来控制音频。在文章中，[krich]提到它可能是第一个基于手势的音量控制。然而，[我们在](https://hackaday.com/2015/10/07/bootstrapping-motion-input-with-cheap-components/)之前做过，T2 和其他人也做过。

当然，悬浮滑板完成了所有艰苦的工作。它通过 I2C 向 Arduino 传送数据。PC 端由一些屏幕显示软件窗口处理， [3RVX](https://3rvx.com/) 。

不过，这个似乎与悬浮板配合得很好。很难反对任何使软盘容器升级的东西。

 [https://www.youtube.com/embed/PshAhPcTlz4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PshAhPcTlz4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/rxWCJmp54sw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rxWCJmp54sw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

