# Novation Launchpad MIDI 控制器走向开源

> 原文：<https://hackaday.com/2015/09/30/novation-launchpad-midi-controller-moves-toward-open-source/>

Novation Launchpad 是一个 MIDI 控制器，最常用于 Ableton Live 数字音频工作站。这是一个 8×8 的按钮网格，带有 RGB LED 背光，通过 USB 向你的电脑发送 MIDI 命令。它经常被用来触发剪辑，这是由艺术家 Madeon 在[这个视频](https://www.youtube.com/watch?v=lTx3G6h2xyA)中演示的。

Launchpad 作为 MIDI 输入设备很有用，但它过去只能做这么多。但是现在，Novation 为 [Novation Pro](http://global.novationmusic.com/launch/launchpad-pro) 发布了一个[开源 API](https://github.com/dvhdr/launchpad-pro) 。这使得编写自己的代码在控制器上运行成为可能，这些代码可以使用 USB 引导加载程序进行刷新。API 允许您访问硬件，并提供了示例代码。

给我们这个提示的[Jason Hotchkiss]一直在用 API 进行[黑客攻击。Launchpad Pro 有一个很好的老式 5 针 MIDI 输出，可以直接连接到合成器。[Jason]的自定固件将 Launchpad Pro 用作独立的 MIDI 音序器。休息之后你可以看看这个视频。](http://hotchk155.blogspot.co.uk/2015/09/novation-release-custom-firmware-api.html)

不幸的是，Novation 没有开源工厂固件。然而，这种开放的 API 对于音频设备通常的闭源特性是一种受欢迎的改变。

 [https://www.youtube.com/embed/OWO5yih11nE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OWO5yih11nE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

