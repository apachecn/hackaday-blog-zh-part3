# 令人惊叹的交互式 LED 桌子

> 原文：<https://hackaday.com/2017/01/31/an-awesome-interactive-led-table/>

如果你想创建一个 led 矩阵的大显示器，这是一个相对简单的过程。多亏了可寻址 LED 胶带和微控制器，它变得更像是一个软件问题，而不是一个硬件问题。[Vincent de conick]有一些便宜的 WS2812 条，所以他把它们切成一个便宜的宜家咖啡桌，[把它们安装在亚克力板下面的格子里](http://blog.deconinck.info/post/2016/12/19/A-Dirt-Cheap-F-Awesome-Led-Table)。一些人后来用 Arduino Nanos 和 Raspberry Pi 工作，他有一个非常好的 LED 矩阵表。

你可能会说，这是一次吸引人的黑客攻击，就此打住吧。但是他不满足于就此罢休，所以为了让事情变得更特别，他决定增加互动性。由于每个像素都有一个红外发射器和接收器，他能够将 LED 桌子变成 LED 触摸屏，尽管有点学究气，它并没有感应触摸。

红外传感器的设计并不完全简单，因为为了确保可靠的检测和避免 LED 的照明，它们必须小心安装并封装在一个管子中。他还详细介绍了他用来驱动更多 Arduinos 和一个 GPIO 扩展器的整个阵列的多路复用电路。

关于这个项目的报道很长，但它非常值得一读，因为结果非常令人印象深刻。有几个视频，但我们会给你看最后一个，玩触摸屏俄罗斯方块的桌子。

 [https://www.youtube.com/embed/_74hIv6vHGE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_74hIv6vHGE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们推出了另一款带 led 灯的 Lack 桌，但你可能会说它缺少这款的触摸元素。当然，还有 [York Hackspace 的俄罗斯方块桌](http://hackaday.com/2016/12/18/led-tetris-table/)。