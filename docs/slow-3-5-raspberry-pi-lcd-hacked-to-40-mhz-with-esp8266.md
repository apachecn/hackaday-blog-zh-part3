# 慢速 3.5 英寸 Raspberry Pi LCD 通过 ESP8266 降至 40 MHz

> 原文：<https://hackaday.com/2016/11/17/slow-3-5-raspberry-pi-lcd-hacked-to-40-mhz-with-esp8266/>

随着微控制器变得越来越普遍，我们看到了更多从一个芯片中获得大量性能的方法。这方面的一个很好的例子是 ESP8266，它最初被视为一种廉价的 WiFi 卡，但由于内部隐藏的马力，它已经发展成为自己的开发平台。为此，[马丁]正试图通过从头开始推出自己的 LCD 驱动程序来进一步推动现在无处不在的 WiFi 芯片。

选择的显示器是 KeDei LCD 3.5”模块，该模块最初打算与 Raspberry Pi 一起使用。[Martin]指出这款显示器并未针对速度进行优化，但在说了这么多并做了这么多之后，他让它的时钟线以 40 MHz 运行。为了从 LCD 获得这种速度，他减少了第一个移位寄存器，并添加了自己的快速传播电路，以建立更传统的串行寻址模式。通过使用[马丁]也写的 WLCD 驱动程序，现在用 ESP 模块在屏幕上快速绘图相对容易。看看下面的视频吧。

如果你正在寻找自己的小，便宜，快速的显示器，这是一个很酷的方法，但我们建议为 ESP 和附加电路旋转载板。我们期待着未来的项目，将这样的设备放入非常小的魔镜中，或者用在其他方便使用小型图形显示器的地方。

 [https://www.youtube.com/embed/7dyVdiZUw1o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7dyVdiZUw1o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Hemal]的提示！