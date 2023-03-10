# Arduino Cinque–RISC-V、ESP32、WiFi、蓝牙 Arduino

> 原文：<https://hackaday.com/2017/05/20/arduino-cinque-the-risc-v-esp32-wifi-bluetooth-arduino/>

本周末，Arduino 与开源 RISC-V micros 的无晶圆厂供应商 SiFive 合作，在湾区 Maker Faire 上[推出了 Arduino Cinque](http://makerfaire.com/maker/entry/60546/) 。这是一款运行速度最快的微控制器的主板，此外，该主板还包括 Espressif 的 ESP32，这是另一款出色的芯片，具有 WiFi 和蓝牙功能，以及非常强大的 SoC。

目前关于 Arduino Cinque 的细节很少，但从我们迄今为止看到的情况来看，Cinque 是一个令人印象深刻的强大主板，具有 SiFive 的 RISC-V FE310 SoC、ESP32 和 STM32F103。STM32 似乎致力于为电路板提供 USB 到 UART 的转换，这是第一个兼容 RISC-V 的 Arduino 用 FTDI 芯片解决的问题。使用 FTDI 芯片当然是一个有问题的设计决策，当构建一个大写的“O”开放式微控制器平台时，我们很高兴 SiFive 和 Arduino 找到了一个更好的解决方案。目前还不知道 STM32 是否可以与 FE310 和 ESP32 一起使用。

我们已经看了 SiFive 的 FE310 SoC，它是一款极其强大的芯片。[它首先在 HiFive1](http://hackaday.com/2016/11/29/hifive1-risc-v-in-an-arduino-form-factor/) 上发布，[我们的实际测试](http://hackaday.com/2017/01/05/hands-on-with-the-first-open-source-microcontroller/)显示这是一款超越 Arduino 世界当前性能冠军 Teensy 3.6 的芯片。当然，对于任何新的架构，将大量的库移植到 FE310 上会有一些问题，但 SiFive 已经包括了一个 Arduino 兼容的 SDK。它很有前途，我们已经迫不及待地想在更多的板中看到 SiFive 的作品。