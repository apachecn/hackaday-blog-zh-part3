# 眼睛 Pi

> 原文：<https://hackaday.com/2016/10/01/oculus-pi/>

[WayneKeenan]写了一个概念验证的虚拟现实系统，它使用了一个 Raspberry Pi 和一个 Oculus Rift。它大约有一千行 Python 代码，带着电池组，它甚至是便携式的。问题是 Pi 很难创建 3D 视图。

[Wayne]最近重新看了演示，发现一切都变得更好了:Pi 3 更快了，Python 库也变得更好了。他花了一些时间建立了一个库——VR Zero(虚拟现实)然后用 80 多行 Python 重新创建了原始演示。你可以看一个视频，在下面。

图书馆提供:

*   键盘、鼠标和其他输入设备的默认输入事件处理。
*   Oculus Rift DK1 和 DK2 以及 Xbox 游戏手柄的配置。
*   用于校正镜头失真的 OpenGL ES 桶形着色器。

一些演示在 Pi 3 上的峰值速度约为每秒 25-30 帧。不算太寒酸。

我们已经看到了 Rift 的一些很酷的用途，比如[虚拟监视器](https://hackaday.com/2014/12/11/using-the-oculus-rift-as-a-multi-monitor-replacement/)和[起重机控制](https://hackaday.com/2014/07/08/the-crane-game-oculus-style/)。

 [https://www.youtube.com/embed/e6jcBTLeOB0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e6jcBTLeOB0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

