# 仔细看看大家最喜欢的 Blinky

> 原文：<https://hackaday.com/2017/03/10/closer-look-at-everyones-favorite-blinky/>

承认吧，你喜欢看芯片镜头，尤其是当你有帮助走过所有不同部分的功能。这个很简单，有几个原因。[electronupdate]将他的显微镜对准了 WS2812 上的芯片。

WS2812 是一种可寻址的 RGB LED，通常称为 neo pixel(ada fruit 为其指定的品牌名称)。该器件封装在一个 5×5 mm 外壳中，正面有一个透明窗口。这样，当二极管点亮时，您可以很容易地看到它们，同时也很容易看到控制器件的逻辑电路芯片。

该芯片负责在数据移入时读取数据，将其移出到链中的下一个 LED，并相应地设置三个二极管中的每一个。功能性很简单，这使得弄清楚骰子的每个部分对工作的贡献要容易得多。二极管驱动器是一个致命的漏洞，因为有一根焊线连接到它们的一部分。听说第四个足迹可能用于测试，这很有趣——如果你能推测出那些测试包括什么，请在评论中发表意见。

我们毫不费力地找到了逻辑电路。这种探索不像许多[[Ken shir riff 的]硅逆向工程](http://hackaday.com/2016/12/27/ken-shirriff-takes-us-inside-the-ic-for-fun/)那样深入到门级，但[electronupdate]使用的过程同样有趣。他抓起一个微型太阳能电池，在二极管运行时观察它，以捕捉用于使每个 LED 变暗的 PWM 模式。这是一个巧妙的小技巧，可以放在你的后口袋里，在对别人的工作进行逆向工程时，用来证实你关于时钟频率和实现的理论。

 [https://www.youtube.com/embed/a2IY89FAjZE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/a2IY89FAjZE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [危险原型](http://dangerousprototypes.com/blog/2017/02/05/a-look-at-the-neopixel-controller-die-teardown/)