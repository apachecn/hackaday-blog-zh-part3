# ATMega328 3D！

> 原文：<https://hackaday.com/2017/08/08/atmega328-3d/>

如今，小型有机发光二极管显示器并不昂贵——便宜到让它们与 8 位微处理器搭配在一起在经济上是可行的。但是你能用一个小小的显示器和不完全强大的处理器做什么呢？如果你是【ttsiodras】你可以做一个[实时 3D 渲染](https://github.com/ttsiodras/3D-on-an-ATmega328p)。你可以在下面的视频中看到结果。对于一个 8 位 8 MHz 处理器来说，这已经不错了。

该代码是一个“仅点”渲染器。该设计通过 SPI 引脚驱动有机发光二极管，并通过串行端口输出每秒帧数信息。

正如你所料，3D 输出需要大量的数学运算，而这个芯片并不擅长处理实数。[Ttsiodras]使用一种旧技术来处理这个问题:定点算术。这个想法很简单。通常，我们认为 16 位字包含 0–65535 的无符号值。但是，如果您愿意，也可以用它来表示数字，例如从 0 到 50.999。在精神上，你将所有东西缩放 1000，然后在你想要输出的时候反向操作。加法和减法很简单，但是乘法和除法需要一些额外的工作。

如果你想了解更多关于[定点数学](https://hackaday.com/2016/04/22/embed-with-elliot-keeping-it-integral/#more-201511)的知识，你来对地方了。我们还介绍了[，一个很棒的外部教程](https://hackaday.com/2012/07/15/a-detailed-explanation-on-speeding-up-avr-division/)。但是，如果你认为这是我们第一次为 ATmega 部件报道 3D 图形引擎，[你就错了](https://hackaday.com/2016/01/02/better-3d-graphics-on-the-arduino/)。

 [https://www.youtube.com/embed/nsqmnkfZtSw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nsqmnkfZtSw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

