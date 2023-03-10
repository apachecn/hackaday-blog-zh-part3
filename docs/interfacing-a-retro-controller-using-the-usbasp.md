# 使用 USBASP 与复古控制器接口

> 原文：<https://hackaday.com/2017/06/22/interfacing-a-retro-controller-using-the-usbasp/>

ISP 加密狗是制造商工作台上非常常见的设备。然而，它作为黑客设备的潜力通常被忽视了。USBASP 的核心是 ATmeg8L，罗布森决定将这个不起眼的 USB 设备用作他的个人电脑和 SNES 游戏手柄之间的接口。

SNES 控制器需要三个引脚与主机通信:时钟、数据和锁存。在他的黑客中，[Robson]使用一个小型 DIY 适配器将控制器连接到 ISP 接口，并使用 [V-USB 库](https://www.obdev.at/products/vusb/index.html)对 AVR 进行编程。V-USB 是一个用于小型微控制器的软件 USB 库，在这种情况下非常方便。

[Robson]在记录创建界面的整个过程方面做得非常好，包括 USB HID 代码以及 SNES joypad 串行协议。他的黑客技术可以在 Windows 和 Linux 上运行，代码可以在 GitHub 上下载。

像这个项目这样简单的实现对于任何想尝试 DIY USB 设备的人来说都是一个很好的起点。退伍军人可能会发现一个完全 DIY 的游戏杆更适合他们，也会受到一些塑料技术的启发。