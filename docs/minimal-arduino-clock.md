# 最小 Arduino 时钟

> 原文：<https://hackaday.com/2016/11/02/minimal-arduino-clock/>

用 Arduino 这样的普通微控制器制作时钟并不困难。然而，如果你尝试过，你可能会发现，如果没有一些外部硬件，跟踪墙壁时间是很困难的。[Barzok]有一个非常小的时钟版本。它需要一些带有集成驱动器的 LED 阵列、Arduino Nano、实时时钟模块和电压调节器。

该软件使用定制的 6×9 字体，并将 led 作为一个单独的显示器进行寻址。因为实时时钟模块非常精确，所以没有设置时间的规定。[Barzok]说他一年两次连接 Arduino，用新的开始时间刷新程序，这似乎就足够了。

不过，添加几个按钮来设置时间或接受其他用户输入不会太难。话说回来，这是一个最小的构建。对于希望从事微控制器项目建设的人来说，这将是一个很好的起步项目。

如果你真的想要最小的，你可以用一个 4 LED 时钟(但是你最好知道电阻颜色代码)。当然，[ESP8266 可以作为一个简单的时钟](http://hackaday.com/2016/09/11/simple-clock-from-tiny-chip/)，它可以通过 NTP 设置，这甚至更好。

 [https://www.youtube.com/embed/yoBDhjfy_UA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yoBDhjfy_UA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

