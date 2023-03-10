# ESP8266 基本 WiFi 恒温器非常简单

> 原文：<https://hackaday.com/2015/11/28/basic-on-the-esp8266/>

如果您在过去几年中阅读过我们的任何帖子，您会注意到我们的社区非常热衷于通过 ESP8266 模块以低廉的价格将互联网引入他们的设备。为什么？这篇[论坛帖子详细介绍了 WiFi 恒温器的制作](http://www.picbasic.co.uk/forum/showthread.php?t=20908&p=135556#post135556)真正说明了这一点:制造具有互联网功能的设备是如此容易和便宜，以至于你几乎无法抗拒。

当 ESP8266 第一次出现时，几乎没有文档，更没有代码支持。从那以后 [Espressif 的 SDK](http://espressif.com/en/products/esp8266/) 有所改进， [NodeMCU](http://hackaday.com/2015/01/01/a-dev-board-for-the-esp-lua-interpreter/) 项目带来了 Lua 支持，甚至还有 [Arduino 支持](http://hackaday.com/2015/03/28/arduino-ide-support-for-the-esp8266/)。最近， [BASIC 被添加到 ESP stable](http://hackaday.com/2015/08/29/basically-its-an-esp8266/) 中，这确实降低了创建简单 WiFi 小部件的障碍，比如这里的恒温器示例，它使用 Dallas DS18B20 温度传感器和 LED 作为加热器元件的替身。

这个项目的硬件是从 ESP8266 基础文档中重新构建的[这个演示代码，只不过是一些现成的部件焊接在一起。不需要原理图。](http://www.esp8266basic.com/ds18b20-wifi-thermostat.html)

让这个项目在幕后工作的是 ESP8266 论坛上[Rotohammer]的一些聪明的代码重用。本质上，他包装了 Arduino 的单线库，给了它简单的基本绑定。接下来，基本编码器要做的就是读取数值，并将其打印到网页上。

这里隐藏着各种各样的细节，那些习惯于裸机编程的人肯定会怒不可遏。但是有时候你可以自己建造一台注塑机来 DIY 乐高积木，有时候你只需要把积木组装在一起。这个项目，以及使之成为可能的 BASIC 解释器，展示了一个人仅仅把零件组装在一起就能得到多少快乐。