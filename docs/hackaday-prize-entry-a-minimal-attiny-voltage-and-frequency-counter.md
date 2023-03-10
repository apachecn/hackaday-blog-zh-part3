# Hackaday 奖品入口:一个最小的 ATtiny 电压和频率计数器

> 原文：<https://hackaday.com/2016/07/02/hackaday-prize-entry-a-minimal-attiny-voltage-and-frequency-counter/>

有时候，当你在构建一个东西的时候，是因为你已经在头脑中有了一个清晰的想法或规范，但并不总是这样。以[kodera2t]的项目为例，他开始掌握 ATtiny 系列微控制器，并从简单的 LED 闪光灯开始，但最终达到了相当有用的东西。[at tiny 10 DVM 和 DFM 一体机，配有 i2c LCD 显示屏和最少的其他组件](https://hackaday.io/project/10116-minimalist-a-go-go)。

DFM 使用 ATtiny 的内部 16 位定时器，该定时器具有能够由外部时钟驱动的便利特性。要测量的频率驱动计时器，计时器返回的时间与系统时钟进行比较。它不是最好的频率计数器，因为它依赖于 ATtiny 的时钟，而不是校准的晶体参考，但它可以工作。

结果如下图视频所示，所有代码已经[发布在他的 GitHub 库](https://github.com/kodera2t/Magical_tweezersIV/blob/master/Tiny10_freqANDvolt.asm)中。我们可以看到，在这个电路中有一个方便的小仪器的基础，尽管廉价万用表的价格如此之低，即使是这样一个最小的电路也很难在成本上竞争。

 [https://www.youtube.com/embed/ZQcvm9J0-E8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZQcvm9J0-E8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这不是我们展示的第一个自制频率计数器。我们已经见过不止一个[基于 Arduino 的计数器，](http://hackaday.com/2013/02/09/arduino-as-an-inexpensive-ham-radio-frequency-counter/)一个[基于 74 逻辑](http://hackaday.com/2012/11/06/7400-frequency-counter/)，还有一个[基于 PIC 的计数器，带有串行输出](http://hackaday.com/2011/03/15/pic-based-frequency-counter/)。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)