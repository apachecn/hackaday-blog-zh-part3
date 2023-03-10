# ArduinoCade 上的复古游戏是不可能的

> 原文：<https://hackaday.com/2015/09/17/retro-games-on-arduinocade-just-shouldnt-be-possible/>

在当今的微控制器上制作复古视频游戏带来了许多挑战，尤其是当仅使用微控制器本身来处理整个体验时。复杂的图形、声音、游戏逻辑和输入对小芯片来说已经够累了，再加上 NTSC 彩色图形，你就有了一只完全不同的熊。

[rossum]开始使用超频的 Arduino Uno 制作 Arduinocade 复古游戏系统，仅此而已。支持 4 个语音声音和红外游戏控制器，该系统还拥有 27 种软件同步颜色。如果没有图形芯片来分担一些工作，这些颜色和分辨率似乎是不可能的。在做所有这些的同时，ATmega328p 也在玩一些经典街机游戏的忠实再现。

使用了一些有趣的技巧。色彩是由 [NTSC 彩色伪像](https://en.wikipedia.org/wiki/Composite_artifact_colors)产生的，其中屏幕实际上是黑白的，但由于信号产生中的一两个延迟，这些位与参考“彩色突发”信号不同相，并在屏幕上显示为独特的颜色。这种方法被用于 8 位苹果 II 个人电脑来产生它的颜色，也在早期的 IBM 个人电脑上使用 CGA 卡来大幅增加颜色深度。在这种情况下，芯片采用 28.6363 MHz 晶振(NTSC 时序的倍数)超频，SPI 硬件用于移出所有必要的像素。休息之后看看它的外观和声音有多棒。

很高兴在新项目中看到老把戏，我们要去玩一些游戏了！

 [https://www.youtube.com/embed/nGIujZiEu_o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nGIujZiEu_o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

