# 为 Pong 劫持一个索尼守夜人

> 原文：<https://hackaday.com/2018/03/07/hijacking-a-sony-watchman-for-pong/>

老式电视的时代是一个伟大的时代，其中一个过渡性的副产品是索尼守夜人。这是索尼在 1982 年开始销售的便携式电视，令人惊讶的是它有一个真正的 4 英寸阴极射线管或 CRT。[Sideburn]刚刚发布了一个视频，视频中他劫持了一个守夜人的内脏，将其制作成一个便携式的 Pong 游戏。

黑客首先移除内部的电视调谐器模块，为新居民腾出一些空间。接下来是 M51364P，这是 VIF 视频解码器芯片，令人惊讶的是，网上没有太多关于它的信息。他们找到了原理图的一部分，虽然是俄文的，但对爱好者来说可能仍然有用。移除 VIF 暴露了音频和视频引脚，这些引脚需要适当的信号才能使黑客攻击成功。在多层板时代，令人惊讶的是，两层 PCB 让修补者的生活变得如此轻松。

对于新的大脑，选择了 Arduino Nano 克隆，而不是添加现代按钮，现有的音量和波段选择开关被认为是拨片控制和播放/暂停按钮。没有调谐器模块，一切都很容易适应，瞧！新硬件。对于固件，[Sideburn]转向 Hackvision 固件，其中有许多游戏，如太空入侵者，小行星，甚至俄罗斯方块。

几年前我们曾将[hack vision](https://hackaday.com/2010/10/24/hackvision-is-build-your-own-retro-game/)作为硬件/固件捆绑包，如果你对 CRT 更感兴趣，那么可以看看 [Arduino 驱动的 6845 CRT 控制器](https://hackaday.com/2017/05/14/the-modern-retrocomputer-an-arduino-driven-6845-crt-controller/)。

 [https://www.youtube.com/embed/PuiLvJbx7Tk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PuiLvJbx7Tk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

