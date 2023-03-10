# USB 蚀刻素描风格的鼠标比你想象的更模拟

> 原文：<https://hackaday.com/2016/12/07/usb-etch-a-sketch-style-mouse-is-more-analog-than-youd-think/>

[Mitxela]想要制造一种不同的鼠标，一种像蚀刻素描玩具一样工作的鼠标，有一个 X 旋钮和一个 Y 旋钮。配备一些旋转编码器和一个微控制器，这应该不难。但是当你在 85 年使用 pin 码时，你需要一些技巧。

编码器会输出一个两位的格雷码，当你按下时会关闭一个按钮。另外，你还需要一些管脚给 [V-USB 堆栈](https://www.obdev.at/products/vusb/index.html)来处理 USB 接口。[Mitxela]决定使用一个简单的电阻 DAC 将编码器转换为输出模拟电压。这将只需要两个模拟输入，另一个模拟输入可以读取两个开关。

一个问题是:仍然没有足够的 I/O。当然，对于 AVR，您总是可以将 reset 引脚重新用作模拟引脚，但您无法在低电压下对器件进行编程。当然，对此也有一个解决办法，允许您保留 reset 引脚，同时仍然读取其模拟值。你只需确保该值不会低于约 2.5V，这样器件就不会复位。一旦完成，剩下的就容易了，正如你在下面的视频中看到的。

激光切割的外壳和旋钮完美地完成了这个项目。老实说，我们可能会想买一个更大的 CPU，但我们必须承认这是可行的。如果这是一个商业项目，我们可能会担心降低 reset 引脚的抗扰度，但对于一个黑客项目来说，这是可行的，这是对引脚的巧妙使用。

我们喜欢关于保存图钉的疯狂想法。一旦你的桌子上有了一个速写鼠标，你也可以给它配一个时钟[。](https://hackaday.com/2014/03/28/an-etch-a-sketch-to-fetch-the-time/)

 [https://www.youtube.com/embed/__hWliAwwNY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/__hWliAwwNY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

