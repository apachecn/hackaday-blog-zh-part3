# 在惠普上运行的迷你苹果 IIe。

> 原文：<https://hackaday.com/2017/06/13/the-mini-apple-iie-that-runs-on-c-h-i-p/>

[Cupcakus]的迷你 Apple IIe 肯定是运行 Apple II 模拟器的最小计算机的竞争者。几个月前，我们在[的一个链接帖子](http://hackaday.com/2017/02/12/hackaday-links-february-12-2017/)中提到过它，当时它和几个视频一起被发布到一个论坛上，但现在受欢迎的 YouTube 频道【已测试】，发布了[的一个视频](https://www.youtube.com/watch?v=8lT-nHeKR9g)，在视频中，他们不仅展示了里面的东西，并采访了【Cupcakus】关于他在制作它时的考验和磨难，还讲述了制作他们自己的一个视频的步骤。此外，在写链接这篇文章的时候，[Cupcakus]还没有公布他关于它的详细的[GitHub 页面](https://github.com/Cupcakus/AppleIIMini)。

这款迷你苹果 IIe 运行在一台 9 美元的小型单板电脑上，有一个扬声器和一个 T2 TFT LCD 显示屏。通过全尺寸无线键盘输入。他没有操纵杆，但这是一个疏忽，他意识到有多少游戏需要操纵杆，他计划增加对它们的支持。这款保护套是由 Thingiverse 上的模型 3D 打印出来的，GitHub 页面上有相关链接，以及所有其他自己制作保护套的细节。

他确实需要做一些黑客工作。引脚接头上没有来自 C.H.I.P .的视频信号，所以他不得不把一根电线直接焊接到电路板上。C.H.I.P .需要 3.3 V 至 5 V，而显示器需要 6 V 至 12 V，为了适应这两种电压，他从 12 V 无人机电池获得电源，并为 C.H.I.P .使用 5 V 降压转换器，他必须修改仿真器，以便在显示器的低分辨率下清晰可见。GitHub 页面也提供了相关代码。

虽然他将显示器用作 Apple II 模拟器的屏幕，但它实际上有两个视频输入。因此，万一他想在显示器上显示来自另一个来源的内容，也许是观看视频，他可以使用背面的插座提供第二个视频输入。

想亲自查看所有细节吗？请查看下面[已测试]的视频。

你更怀念苹果///？我们之前也展示过为苹果/// 精心设计的[迷你包。或者也许你有一个全尺寸的工作 Apple II，并希望它与你的树莓 Pi 来回通信？我们已经讲述了](http://hackaday.com/2016/05/21/build-a-replica-apple/)[如何制作一个适配器](http://hackaday.com/2013/12/26/apple-and-raspberry-pis/)来实现这个功能。

 [https://www.youtube.com/embed/8lT-nHeKR9g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8lT-nHeKR9g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过[测试](https://www.youtube.com/watch?v=8lT-nHeKR9g)