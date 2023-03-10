# 黑客日获奖作品:迷你萨姆-零

> 原文：<https://hackaday.com/2016/07/11/hackaday-prize-entry-minisam-zero/>

多亏了 Arduino，Atmel 的 SAM 系列 ARM 微控制器被大量用作 32 位学习工具。在他的 Hackaday Prize 项目中，[Jeremey]使用了这些芯片中的一种，没有任何 Arduino 戏剧。他制作了一个微型 Atmel SAM 开发板,便宜、简单，有趣的是对于一个 32 位 ARM 开发板来说，很容易编程。

对于这款主板，[杰瑞米]使用的是 Atmel 的 SAM D09，这是该家族中最小的成员，还包括新的 [Arduino Zero](https://www.arduino.cc/en/Main/ArduinoBoardZero) 和 [Arduino M0](http://www.arduino.org/products/boards/arduino-m0) (由 *other* Arduino 制造)上的芯片。MiniSam-Zero 使用一个稍小的芯片，带有 8 kB 的片上闪存。眼尖的投诉者会注意到，SAM D09 没有内部 EEPROM，因此在板上增加了一个 EEPROM。板上还有一个温度传感器和一个用于串行通信的 Silicon Labs CP2102。

最后一个芯片——串行 USART——如果固件做得好，可以实现相当有趣的构建。串行引导加载程序将允许任何人将 USB 电缆插入该板，并直接从 IDE 上传代码，而不是在对设备编程时与 ARM SWD 混为一谈。这可能是 MiniSam-Zero 最酷的特点，也是[杰里米]孜孜不倦努力做好的事情。他可以直接从 Atmel Studio 上传，再做一点工作后，[Jeremy]就可以直接从 Arduino IDE 对这个板进行编程了。这是一项伟大的工作，尽管该板不如其他 ARM 微控制器产品强大，但它仍然是一个非常有用的设备。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)