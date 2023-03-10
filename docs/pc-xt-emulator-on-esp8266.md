# ESP8266 上的 PC-XT 仿真器

> 原文：<https://hackaday.com/2018/02/26/pc-xt-emulator-on-esp8266/>

你还记得更简单的时代吗？那时你有一个 DOS 命令行，几个命令，通过几个 BIOS 和 DOS 中断与硬件对话。好吧，也许是有点局限，但怀旧不在乎。现在[mcuhacker]正致力于通过让 PC-XT 模拟器在 ESP8266 上运行来恢复这些记忆。

对于 x86 CPU 仿真器，他移植了用 C 编写的 [Fake86](http://fake86.rubbermallet.org/) ，并为其创建了一个 Arduino IDE 环境。MS-DOS 3.3 引导磁盘映像存储在闪存中，并作为 A:驱动器进行访问。目前还没有键盘，但他已经有了 640×200 的 CGA，在低通滤波电路的帮助下，可以在 3.5 英寸的 TFT 显示屏上显示 80×25 的字符。在下面的视频中，他展示了它引导到询问日期的地方。

在 ESP8266 上仿真其他硬件似乎是一种流行的做法。也许你是苹果用户，更喜欢在 ESP8266 上运行苹果 1 号的 [6502 仿真。我们甚至有一个运行 CP/M](https://hackaday.com/2017/12/30/espple-a-wireless-apple-1-on-an-esp8266/) 的 [Z80 仿真，以防你更喜欢它。](https://hackaday.com/2017/03/25/cpm-8266/)

 [https://www.youtube.com/embed/5-ledn5xpnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5-ledn5xpnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

