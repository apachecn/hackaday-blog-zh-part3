# 将 USB 设备引入苹果桌面总线

> 原文：<https://hackaday.com/2016/11/20/bringing-usb-devices-to-the-apple-desktop-bus/>

在 Apple II 家族最伟大的成员 Apple IIgs 的开发过程中，有人向[Woz]建议，键盘、鼠标、轨迹球和其他桌面外设需要一种通用串行总线。[沃兹]消失了一段时间，然后带着一些奇妙的东西回来了:一个可以从键盘到图形输入板再到鼠标的菊花链协议。这种协议很容易在廉价的微控制器上实现，为整个总线提供 500mA 电流，用于从许可证加密狗到调制解调器的所有东西。

苹果桌面总线，或称 ADB，领先时代十年，是 Mac 平台的中流砥柱，直到苹果有勇气用 iMac 消灭它。当时，一个 ADB 转 USB 转换器的行业在一夜之间兴起。即使在今天，也有一些机械键盘爱好者在他们最喜欢的输入设备上安装了一个 USB 接口。

虽然将旧的苹果键盘插入现代电脑是一种高尚的追求——这篇文章是在带有 salmon Alps 开关的苹果 M0116 键盘上写的——但有时你想走另一条路。用现代的 USB 鼠标和键盘搭配旧的 Mac 电脑不是很酷吗？这就是[安森]所想的，所以他开发了亚行的卫生员。

ADB Busboy 与[【tmk】为青少年](https://github.com/tmk/tmk_keyboard)开发的 ADB 转 USB 转换器固件完全相反。[anthon]的 ADB Busboy 不是把一个旧的 ADB 键盘变成 USB 设备，而是把 USB 键盘和鼠标变成 ADB 设备。现在，除了 128、512、Mac Plus、PowerBook 150 和其他几款便携式电脑，几乎所有的 USB 键盘和鼠标都与 T2 生产的所有麦金塔电脑兼容。

为什么会有人想这么做？因为它很整洁。看看[安森]制作的动画:

[https://gfycat.com/ifr/SpanishVelvetyHornedviper](https://gfycat.com/ifr/SpanishVelvetyHornedviper)

亚行的餐馆工还没有发布。[anthon]仍然需要实现和测试一些功能，设计一个 PCB，一个外壳，并希望将这些 USB 到 ADB 转换器出售给一些在地下室有太多旧计算机的书呆子。他们是收藏家的物品，少罗嗦。

[anthon] [有一个网站，他最终会在那里宣布这个项目的发布。当这种情况发生时，你可以注册一个电子邮件提醒。](http://www.astrospark.com/adbbusboy/)