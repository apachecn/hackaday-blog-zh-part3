# 廉价的 DIY MIDI 转 USB 适配器

> 原文：<https://hackaday.com/2017/09/26/cheap-diy-midi-to-usb-adapter/>

[Joonas]对便宜但蹩脚的 MIDI 转 USB 转换器感到沮丧，更好的商业转换器超出了他的预算。他用一个小小的 LC 为自己造了一个，而且做得很好。但是他需要几个转换器，而使用这个小小的 LC 要花费他很多钱，超出了他的承受能力。经过一些修补，他能够用一个有板载硬件 UART(但没有 USB)的 Adafruit Pro 饰品来建造一个。缺乏 USB 支持对他来说是一个杀手，所以在寻找了更多之后，他决定克隆 Sparkfun Pro Micro。基于 ATmega32U4，这些克隆正好适合他的应用程序，并且是最便宜的。他估计制造每一个便宜的 USB MIDI 适配器花费了他大约 5 美元，这些适配器从键盘的 MIDI 输出接收音符和踏板数据，并将它们传输到电脑

除了 Pro Micro clone，他使用的唯一其他部件是一个通用的光耦合器，一对电阻器和一个 MIDI 连接器。在面包板上测试了他的简单电路后，他设法将它全部塞进一个旧的 USB 加密狗外壳，以死虫的方式塞进去。

繁重的工作都在固件中完成，为此[Joonas]使用了[LUFA](http://www.fourwalledcubicle.com/LUFA.php)——AVR 的轻量级 USB 框架。他编写了自己的代码来处理 MIDI (UART)到 USB MIDI 消息的转换。有趣的部分是他使用 32.15 kbps 的波特率，尽管 MIDI 规范要求 31.25 kbps。他发现，略高的波特率解决了 AVR USART 实施中的一个问题，即由于未检测到起始边沿，可能会丢失连续字节。除此之外，他的代码在功能上仅限于处理一些信息，主要用于演奏钢琴，并不具备成熟的 MIDI 功能。

这些年来，我们在这里展示了几个[Joonas]的黑客，最近的是 [Beaglebone Pin-Toggling 酷刑测试](https://hackaday.com/2016/04/21/beaglebone-pin-toggling-torture-test/)和更早的[如何通过敲击和修饰打开电脑](https://hackaday.com/2013/10/21/turn-a-pc-on-with-a-knock-and-an-attiny/)。