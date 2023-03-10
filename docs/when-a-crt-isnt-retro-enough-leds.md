# 当 CRT 不够复古时:led

> 原文：<https://hackaday.com/2016/11/08/when-a-crt-isnt-retro-enough-leds/>

当我们想到老式的计算机终端时，它有一个 CRT 屏幕:要么是 20 世纪 70 年代带有集成键盘的大型 VDU，要么是 10 年后的一个更苗条的造型。你会发现在过去的几十年里还有其他的展示在使用，其中一个我们认为值得分享。

[![16 segments in action. (PD) Wikimedia Commons.](img/acd8f62f6e50db38e6f2a4eb8d74b69f.png)](https://hackaday.com/wp-content/uploads/2016/11/sixteen-segment_display_animated.gif)

[Dan Julio]从一个朋友那里得到了几管西门子 DL1416B 4 位 17 段 LED 显示屏，并决定将它们用作他的终端项目的[一种不同寻常的复古显示屏。这些设备是带有并行接口的字母数字显示器，可以显示 ASCII 字符集的子集以及光标。他有 213 个这样的部件，所以他计划用 64 个字符乘 16 行显示，但是在发现一些部件不起作用时，他不得不缩减到 12 行 48 个字符。](https://hackaday.io/project/17983-dl1416smarterm-led-computerterminal)

[![The terminal in action.](img/f422ddedc2443e8c18750fe85253ff35.png)](https://hackaday.com/wp-content/uploads/2016/11/terminal-overview.jpg)

The terminal in action.

显示器四个一组安装在印刷电路板上，由 PIC16F1459 和一些移位寄存器控制。然后，这些板通过 TTL 串行线以菊花链形式连接在一起。整个显示器与 Teensy 3.1 上的三个串行端口中的一个共享，[他的复古键盘](https://hackaday.io/project/12796-almost-pre-historic-computer-keyboard-lives-again)有自己的 PIC 控制器，其他端口服务于串行打印机端口和终端串行端口。Teensy 软件有两种模式:串行终端或微型 Basic 解释器，相关的库从项目页面链接。

由于每组 DL1416Bs 的功耗为 250 mA，因此在 5 伏电压下，整个显示器的功耗约为 9 A。除此之外，键盘还消耗 500 毫安的电流，因此必须集成足够强大的电源。这是与 Teensy 一起安装在一个制作精良的外壳中，整体安装在一个看起来像是多余的显示器支架上，以实现非常专业的效果。

为了让我们了解终端的功能，他在 YouTube 上发布了一个视频，我们把它放在了休息时间的下方。当他登录到一个 Raspberry Pi 并编辑一个文件时，它给我们留下了一个令人惊讶的可用机器的印象，并带我们了解了 BASIC 解释器的一些特性。

 [https://www.youtube.com/embed/um_2RunHDl8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/um_2RunHDl8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



像这样的多段显示器相当罕见，所以我们没有在大量项目中使用它们。有[这个带有另一个 16 段部分的小时钟](https://hackaday.com/tag/16-segment-display/)，还有这个[相当不错的 14 段数组](http://hackaday.com/2012/09/23/led-array-uses-ridiculous-amount-of-14-segment-displays/)，但是那个远没有这个大。不过我们也有很多更传统的终端，比如这个 [DEC VT100 带一个鹰钩鼻](http://hackaday.com/2013/10/16/vt100-gets-beagleboned/)，还有这个 [VT510 带一个树莓派](http://hackaday.com/2016/10/19/dumb-terminals-and-raspberry-pis/)。

16 片段动画，迈克尔 J，(PD) [维基共享资源](https://commons.wikimedia.org/wiki/File:Sixteen-segment_display_animated.gif)。