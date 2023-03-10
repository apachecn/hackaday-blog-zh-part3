# Blinktronicator 的视角让我们的眉毛飙升

> 原文：<https://hackaday.com/2016/07/01/blinktronicators-pov-sends-our-eyebrows-rocketing-skyward/>

你认为你已经看到了所有关于 led 闪烁的东西，然后一个简单的小技巧证明你错了。我们的朋友[Zach Fredin]，又名[Zakqwy]，在他的 blinky board 上添加了一个 pander 模式，显示 Hackaday Jolly Wrencher 处于视觉暂留模式。我们喜欢迎合，显然你只需要启动模式，来回挥动板子。但是从明显的角度来看，你错了。

[![blinktronicator-board](img/6ab5864094b0804523940f44c34e50e6.png)](https://hackaday.com/wp-content/uploads/2016/06/blinktronicator-board.jpg)

Badass deadbug soldering to “fix” a mirrored shift register footprint

在休息后的视频中，[扎克]展示了[blinktronicator 的所有功能，以及它最近完成的固件](https://hackaday.io/project/8331-blinktronicator)。这个小小的板是一个 USB 加密狗，有两个按钮和一个弧形的 16 个彩色 led。当我们说小的时候，我们是认真的。这些发光二极管是 0402 元件，电路板足够小(也足够有趣)，可以在平方英寸项目中获得[荣誉奖](http://hackaday.com/2016/01/13/the-best-projects-that-fit-in-a-square-inch/)。

你可能会认为手工焊接所有这些 led 是一个技巧，但[扎克]完成了一个更困难的壮举。仔细看这里的图片(或点击 embiggen)。原型上的两个移位寄存器足迹是镜像的。他用一些 28 AWG 绞线的单股来焊接它们。你先生，得到硬核手焊接徽章，然后一些。

好吧，我们就不拐弯抹角了。这块板上的 ATtiny45 没有连接到 USB 数据线，它们只是用来供电的。这意味着，在本质上，这纯粹是一个闪烁的 LED 项目，尽管它使用了 PICOLED 系列零件的大量颜色。[Zach]在只有两个用户输入的情况下做得很好，但真正吸引我们的是非常简单的 POV 聚会技巧。[Zach]不用挥动板子，而是用金属刮刀作为镜子。来回移动它会展开精心定时的闪光，在空中画出你的信息。如此简单的一个概念，但看到它以稍微不同的方式应用，却令人如此满意。

 [https://www.youtube.com/embed/jjdHfPybr94?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jjdHfPybr94?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

