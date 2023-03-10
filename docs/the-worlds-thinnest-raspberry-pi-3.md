# 世界上最薄的树莓 Pi 3

> 原文：<https://hackaday.com/2017/09/13/the-worlds-thinnest-raspberry-pi-3/>

我们已经习惯于容易获得的单板计算机，这些计算机的外形尺寸非常大，仅仅在几年前还显得小得不可思议。但是，即使是像 Raspberry Pi 这样的信用卡大小的板，仍然会有可用空间太小而不适合计算机的时候。

大胆的硬件黑客采用的解决方案通常是从电路板上移除无关的元件。例如，如果不需要全尺寸 USB 端口或以太网插孔，它们可以安全地拿走。由于有时这些尝试会导致电路板的意外损坏，皮莫罗尼的海盗们让观众观看了他们的舱底舱系列视频，在这个过程中，他们创造了他们所谓的“世界上最薄的树莓皮 3”。

USB 和以太网端口是最容易处理的大型通孔组件。一些剪切和折断移除了锡器和塑料，然后剩下的可以手工拆焊。GPIO 引脚拒绝尝试移除塑料以方便脱焊，因此他们不得不求助于热风枪。然后，对于剩余的摄像头、HDMI 和显示端口，唯一的选择是热风。一些清理与脱焊编织，他们有他们的超薄 Pi。虽然他们还没有完全完成，但是他们带着读者修改了一个 Raspbian Lite 发行版，去激活那些已经被删除的组件。这不仅可以释放计算机资源，还可以节省一些功耗。

你可能会指出，他们可能只是使用了 Pi Zero，它的 SD 卡在顶面上，甚至更薄一点。除了额外计算能力的问题，你是对的。但是他们的观点是有效的，人们这样做并不总是取得好的结果，所以他们把它作为一个如何做的方法是一个有用的贡献。我们怀疑超薄的 Pi 3 仍然需要注意热量管理。

看一下视频，我们把它放在休息下面了。

 [https://www.youtube.com/embed/NQvRNU3sTtI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NQvRNU3sTtI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



轻薄的单板机已经不是什么新鲜事了，我们给你带来了一台小巧的笔记本电脑中的瘦身版 Raspberry Pi 2，以及一台掌上游戏机中的 Odroid Pi 克隆版[。与此同时，皮莫尔尼有时会使用](https://hackaday.com/2015/01/03/the-smallest-portable-pi/)[工具，但不那么巧妙*。*](https://hackaday.com/2017/01/16/review-hammer-installed-solderless-raspberry-pi-pin-headers/)