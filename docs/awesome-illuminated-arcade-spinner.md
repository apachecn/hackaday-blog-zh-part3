# 令人敬畏的照明街机旋转器

> 原文：<https://hackaday.com/2017/01/23/awesome-illuminated-arcade-spinner/>

[Tinker_on_Steroids]制造了一些看起来很棒的旋转器,它们不仅在旋转时发光，而且本身看起来也很专业。在我们看他的组装视频之前，我们确信他只是在他买的东西上加了东西，但结果是这都是定制设计和制作的。

如果你从来没有玩过旧的街机游戏，旋转器是一种游戏输入设备，例如 Tempest 或 Breakout，你可以向任一方向旋转旋钮，告诉游戏向哪个方向移动东西以及移动的速度。在《暴风雨》中，你可以在屏幕中间旋转东西，而在《突围》中，你可以在游戏场地的底部来回移动球拍。

他甚至用自制的正交编码器来检测旋转。对于每个旋转器，他使用两个 [ITR9608](https://elektronik-lavpris.dk/files/sup2/ITR9608.pdf) (PDF)光开关，或光断续器。每一个都是 U 形的，U 形的一边有一个 LED，另一边有一个光电晶体管。当有东西从两条腿之间通过时，光被暂时阻挡，光电晶体管检测到，即开关关闭。当那东西移开时，灯就被打开了，它又亮了。移动的方向是通过让物体一个接一个地穿过两个 ITR9608 之间来确定的。穿过其间的“东西”是 3D 打印的编码器轮的齿。

为了给它一个额外的令人敬畏的外观，他在每个旋转器中安装了 4 个新像素的 led，这样它们在不旋转时会发出蓝色的光，当旋转起来时会从粉红色变成红色。

所有用于 3D 打印的 STL 文件都在[他的 Thingiverse 项目页面](http://www.thingiverse.com/thing:2021152/#files)上，还有一个 BOM 和购买零件的链接。这两个旋转器的大脑是一个 Arduino Pro Micro，它使用定制的防护罩连接到其中一个旋转器上。他还提供了 Arduino 的源代码和十六进制代码，使 spinners 在连接到计算机时看起来像一个 USB 鼠标设备，当然，除非您为它们编写 on 代码。

[Tinker_on_Steroids]在设计所有 3D 打印部件方面做得非常好，使其成为一个专业的旋转器，如果只是为了看到一个设计良好的 DIY 对象，您应该在休息后查看第一个视频。另外两个视频展示了它的实际应用。

长期阅读 Hackday 的读者可能记得[这些其他的 DIY 旋转器](http://hackaday.com/2008/08/17/scratch-built-jog-wheel/)，其中一个使用 RC 汽车轮胎作为旋钮和鼠标的光学编码器。一些旧照片不见了，但细节都在。

 [https://www.youtube.com/embed/xyOA1leHPJQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xyOA1leHPJQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/WCIApuEYZXw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WCIApuEYZXw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[EVR]的提示。