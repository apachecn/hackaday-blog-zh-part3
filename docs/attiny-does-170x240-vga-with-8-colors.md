# ATtiny 做 170×240 VGA，8 色

> 原文：<https://hackaday.com/2015/12/17/attiny-does-170x240-vga-with-8-colors/>

Arduino 是一个流行的微控制器平台，用于快速完成工作:它随处可见，有丰富的在线资源，并且是一个随时可用的原型开发平台。另一方面，如果你想享受对微控制器的 flash ROM 进行编程的乐趣，你可以从一个任意严格的资源约束开始，看看你能做到什么程度。~~【Lucas】~~【Radical Brad】的[演示可以在一个 8 针 DIP 微控制器上输出 VGA 和立体声音频](http://www.avrfreaks.net/forum/quark85-atiny-does-170x240-vga-8-colors)比仅仅闪烁一个 LED 更令人惊叹一点。

~~【卢卡斯】~~【RB】使用的是 ATtiny85，ATtiny 系列微控制器中较大的一款。在将所需的时钟信号连接到微控制器以获得 VGA 所需的 25.175 Mhz 信号后，他只剩下四个引脚来处理四色*和*立体声音频。这基本上是通过在 VGA 监视器不期待信号的时候发送音频来实现的(并且~~【卢卡斯】~~【拉德·布拉德】在他的项目页面上很好地解释了这个过程)。他对视频内核进行汇编编程，这有助于优化程序，并且除了时钟和微控制器之外，只使用无源元件。

请务必在休息后观看视频，了解只有 512 字节 RAM 的处理器如何输出需要 40 KB 以上的图像。这是一个真实的证明，如果你下定决心，你可以推动这些处理器走多远。我们还看到这些芯片实现了[无线 NTSC](http://hackaday.com/2015/02/26/attiny85-does-over-the-air-ntsc/) 、[蓝牙](http://hackaday.com/2015/02/09/an-attiny-bluetooth-board/)，甚至[以太网](http://hackaday.com/2014/08/29/bit-banging-ethernet-on-an-attiny85/)。

 [https://www.youtube.com/embed/rmx-2fTxsns?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rmx-2fTxsns?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

