# 拜拜 ATmega328P，你好 328PB！

> 原文：<https://hackaday.com/2016/01/26/bye-bye-atmega328p-hello-328pb/>

微控制器上永远没有足够的外设。无论是硬件驱动的 PWM 通道、ADC 还是串行通信外设，我们最终总是想要多一个*这些*，但实际上并不需要那么多*那些*。Atmel 的[广受欢迎的 ATmega328 系列的新版本 ATmega328PB](http://www.atmel.com/devices/atmega328pb.aspx?tab=overview) ，似乎听到了我们的恳求。

我们手头没有芯片，但数据手册很吸引人。以下是新功能的简要介绍:

*   另外两个 16 位定时器/计数器。当您编写的代码没有操作系统支持，并且依赖硬件实现无抖动计时时，这是一件大事。
*   【USART、SPI 和 I2C 系列各两个，而不是一个。当您使用地址空间有限的 I2C 器件时，或者当您需要通过 SPI 非常快速地推出位时，这种方法非常有用。
*   **十个 PWM 通道**而不是六个。这(以及额外的 16 位定时器)对于任何使用 PWM 的人来说都是好消息——从驱动伺服系统到制作音乐。
*   **板载电容感应硬件:外设触摸控制器。**这对于 ATmega328PB 芯片来说是全新的，看起来在没有额外 IC 的情况下运行电容式感应按钮会很有趣。不过，它依赖于 Atmel 的 QTouch 软件库，所以看起来它不是一个独立的外设，而是一个内部多路复用器，可能有一些硬件级过滤。当我们拿到其中一个芯片时，我们必须仔细研究这个问题。

那么这对你意味着什么呢？快速搜索一下常见的可疑点，就可以看到现在有库存和出货的芯片，还有一个便宜的开发套件。如果你用 C 写你自己的代码，利用这些新特性应该是轻而易举的。Arduino 的人们将不得不等待芯片(和代码支持)进入生态系统。

感谢[彼得·范·德·沃尔特]的提示！