# GameGirl:更好的便携式树莓 Pi

> 原文：<https://hackaday.com/2016/04/17/gamegirl-a-better-portable-raspberry-pi/>

不管是好是坏，树莓派最受欢迎的用途是媒体中心和复古游戏机。不，大多数无知的人不会为他们的 Pi 外设开发 Linux 驱动程序，很少有人会处理裸机 ARM 编程。这并不意味着创建一个基于 Pi 的手持控制台是不值得追求的。

作为 2016 年 Hackaday 奖的参赛作品，[David]和[Jean-André]正在打造一款便携式 Pi 控制台，这款控制台比塞满热熔胶和电线的老式 Bondo 外壳游戏机要好得多。[他们用硬件加速显示屏、定制软件和高质量外壳以正确的方式完成了这个项目](https://hackaday.io/project/10207-gamegirl-the-retro-console-done-right)。

[大卫]负责硬件，这意味着要做一个非常非常小的掌上游戏机。这款 GameGirl 的设计与老派的 Game Boy Pocket(或者 Game Boy Light)极其相似。有一个数字键盘，四个按钮，选择，开始，后面还有两个肩膀按钮。构建基于 Raspberry Pi Zero，由于 Pi 的标准 40 引脚接头，[David]能够配置显示器[使用 RGB565 DPI 接口](https://hackaday.io/project/10207-gamegirl-the-retro-console-done-right/log/34528-display)。这意味着[显示器便宜得离谱](https://hackaday.com/2015/03/05/using-cheap-displays-with-the-raspberry-pi/)，同时还为 SPI、按钮、背光和 PWM 音频留了几个 GPIO 引脚。

[Jean-André]是团队的另一半，他对开源软件的贡献使他非常适合这个项目。他是 DIY 复古仿真控制台 [Lakka](http://www.lakka.tv/) 的主要开发者，也是第五大复古贡献者。不，这个项目没有使用 retro pie——这是有原因的。模拟器黑客花了很多时间为 Raspberry Pi 优化模拟器，仅仅是因为 RetroPi。如果这些模拟器黑客把时间花在优化像 [LibRetro](http://www.libretro.com/index.php/api/) 这样的 API 上，你最终可以在 Raspberry Pi 和 LibRetro 可用的任何其他平台上玩一个 *Pilotwings 64* 的工作版本。让一款游戏能够在树莓 Pi 上运行的所有努力都是为了让这款游戏能够在 PSP、Wii、iOS 和 PC 上运行。是的，这是哲学上的，一边说‘这是社区应该做的’；毕竟这是开源软件。

随着正确的想法进入硬件和软件，[David]和[Jean-André]手中有一个惊人的项目。这是最受欢迎的参赛作品之一，在社区投票自举活动中接近排行榜的顶端，在这个活动中，一个项目中的每个赞都会为团队的项目赢得一美元。GameGirl 正在形成一个伟大的项目，我们迫不及待地想看到它的行动。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/186c8fd237cf75fd0ea0cc799fcf2eac.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)