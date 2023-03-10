# 3D 无人机视频

> 原文：<https://hackaday.com/2018/04/21/3d-drone-video/>

如果你喜欢飞行四轴飞行器，你最好买一架带摄像头的无人机。以前录个视频以后看就够了，但是现在你真的想看直播。真正酷的设置有护目镜，所以你可以感觉你实际上是在驾驶舱。[Andi2345]决定更进一步，建造一架能够播放 3D 视频的无人机。你可以在下面看到这个系统的视频。

在室外，拥有 3D 视图可能没有太多优势，但对于小型室内无人机来说应该很棒。当然，问题是，一架小型无人机没有太多的容量来容纳两个摄像头。最终产品使用两个保持同步的相机，一个同步分离器 IC 和一个微控制器，而一个模拟开关分散帧。

在观看方面，USB 帧抓取器和树莓 Pi 再次分割图像。起初，该系统使用一个 LCD 屏幕和一个谷歌纸板风格的护目镜，但最终，这变成了一个定制的 Android 应用程序。

如果你能让这两个摄像头使用同一个时钟，它们会工作得最好。如果你不这样做，那么一个图像可能会出现滚动。如果你旋转相机，使胶卷从右到左而不是上下移动，这可能会减少干扰。该系统引入了大约 100 毫秒的延迟，这并不完美，但显然是可行的。

小型无人机很容易找到，或者你可以[自己造](https://hackaday.com/2017/01/31/cheap-diy-fpv-micro-drone/)。我们以前见过摄像机[组合成 3D](https://hackaday.com/2007/10/14/3d-video-with-consumer-cameras/) ，但从来没有这么小的规模。

 [https://www.youtube.com/embed/COcnZMT6cqo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/COcnZMT6cqo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

