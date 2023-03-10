# Arduino 上更好的 3D 图形

> 原文：<https://hackaday.com/2016/01/02/better-3d-graphics-on-the-arduino/>

中国有便宜的液晶显示器，当插入 Arduino 时，这些显示器可以作为有用的界面，甚至是你最新项目中更闪亮的小玩意。[迈克尔]拿起一些这样的展示，希望把一些动画。上面有 gif。对于 ATMega 微控制器来说，这是一项不可能完成的任务 Arduino 没有 RAM 或处理能力来播放全屏动画。[可以显示 3D 矢量图形](http://crawlingrobotfortress.blogspot.com/2015/12/better-3d-graphics-engine-on-arduino.html)，用更新的图形库【Michael】写的。

有问题的显示器使用 ILI9341 LCD 驱动程序，可在[Adafruit 库](https://learn.adafruit.com/adafruit-gfx-graphics-library/overview)和[一个优化的 3D 图形驱动程序](http://www.mrt-prodz.com/blog/view/2015/05/tiny-3d-engine-on-the-atmega328-arduino-uno)中找到。当动画更新时，这两个驱动程序都有明显的闪烁，这是由擦除上一帧和绘制新帧之间的延迟引起的。

对于 16 位颜色和 320×240 像素的分辨率，ATMega 微控制器上根本没有足够的内存或处理能力来在显示单帧所需的时间内渲染任何东西。也没有足够的内存在屏幕外渲染。为了解决这个问题，[Michael]构建了他的渲染库，只渲染与前一帧不同的像素。

3D 渲染有其自身的问题，凸面可以相互重叠。为了解决这个问题，[Michael]的库从前到后渲染对象——如果像素不变，就不需要渲染。这将自动处理遮挡。

在一个演示应用程序中，[Michael]的 LCD 和 Arduino 可以显示斯坦福兔子、低多边形 3D 脸和几何对象。这还不是一款视频游戏，但[迈克尔]认为他可以将经典游戏 *Spectre* 移植到这个平台上，并让它以合适的帧率运行。

下面的演示视频。

[https://player.vimeo.com/video/150386845](https://player.vimeo.com/video/150386845)