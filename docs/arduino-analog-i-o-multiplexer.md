# Arduino 模拟输入/输出多路复用器

> 原文：<https://hackaday.com/2018/06/09/arduino-analog-i-o-multiplexer/>

[SeanHodgins]心中有一个项目，他需要对 500 多个模拟传感器进行采样。为了做好准备，他为他想要使用的 32 通道模拟多路复用器设备制作了一个分线板。他在 [Hackaday.io](https://hackaday.io/project/158880-megamux-32-channel-to-1-multiplexer) 上发布了这个项目，还有一个视频教程，你可以在下面看到。

该芯片有五个输入引脚，允许您将一个模拟引脚连接到 32 个模拟引脚中的任何一个。当然，除了五条控制线，你还需要一些握手线，这样你就可以使用多达八个数字引脚来控制设备。

相关器件是 ADG732。电路板布局和源代码都可以在 [GitHub](https://github.com/IdleHandsProject/megamux) 上找到。因为开关是模拟的，所以它们是双向的。也就是说，它并没有真正将一个输出连接到 32 个输入。它更像是一个 32 位开关，将 32 个引脚中的一个连接到另一个引脚。

请记住，这些类型的设备有一些实际的限制。例如，室温下开关电阻的标称值为 4 欧姆。路由信号的开关也有一些电容，这些电容根据开关的开或关而变化。当然，这些都没有错。但这与拥有一个 32 位旋转开关并不完全相同。当然，它可以比机械开关更快地切换，并且易于控制，所以——一如既往——这是一个权衡。

另请注意，mux 芯片可以轨到轨工作。然而，对于某些应用，您需要负电源，而该器件可以接受+/- 2.5V 电源。

像这样的东西有很多用途。例如，路由音频信号，或者在自动测试系统中的多个测试点之间切换。去年我们看到一个多路复用器[只有微不足道的八个通道](https://hackaday.com/2017/05/17/a-few-of-our-favorite-chips-4051-analog-mux/)。话又说回来，你总是可以去守旧派[制造机械多路复用器](https://hackaday.com/2017/01/19/relay-computing/)。

 [https://www.youtube.com/embed/e4h7akFXovM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e4h7akFXovM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

