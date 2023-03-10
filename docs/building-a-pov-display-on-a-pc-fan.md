# 在 PC 风扇上构建 POV 显示

> 原文：<https://hackaday.com/2018/04/21/building-a-pov-display-on-a-pc-fan/>

我们之前已经报道过很多视觉暂留(POV)显示器，但来自[Vadim]的这个相当有趣:[它建立在 PC 风扇](https://www.shortn0tes.com/2018/04/ws2811-pov-display-on-pc-fan.html)之上。他很快就要参加一个机器人制造比赛，并希望有一个 POV 展示。那么，为什么不一石二鸟，将显示器安装在一个还可以用来通风的风扇上呢？

显示器是一个独立的模块，包括电池、Neopixels、Arduino 和接收待显示图像的 NRF240L01 无线电。这可能看起来有点夸张，但是将整个东西放在一个旋转的平台上确实可以解决向旋转显示器供电和发送信号的常见问题:不需要滑动连接。

[Vadim]详细介绍了他是如何构建显示器的，包括他在诊断故障 LED 芯片时遇到的问题，以及为什么在每个阶段进行测试很重要，因为当显示器不高速运转时，调试更容易。

这是一个有点粗糙的构建，使用了比可能需要的更多的原型板，但我们会祈祷它不会在比赛中飞走。

 [https://www.youtube.com/embed/NRSyY1QcY88?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NRSyY1QcY88?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

