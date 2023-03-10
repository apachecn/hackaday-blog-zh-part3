# 通过史诗 SDIO 黑客 2 美元的无线网络

> 原文：<https://hackaday.com/2015/12/09/raspberry-pi-wifi-through-sdio/>

这就是我们生活的时代:Raspberry Pi Zero 问世——一款售价 5 美元的全 Linux 片上电脑——人们抱怨它没有这个或那个。最迫切需要的可能是音频输出和 WiFi 连接。USB 是这两个问题的解决方案，但只有一个 USB 端口的话，它将是一种稀缺商品，所以欢迎任何帮助。

Hackaday.io hacker [ajlitt]正在寻找摆脱 WiFi 束缚的方法。他的解决方案？Raspberry Pi 系列芯片在一系列 GPIO 引脚上有特殊功能，使其更容易与 [SDIO](https://en.wikipedia.org/wiki/Secure_Digital#SDIO) 设备通话。SDIO 是类似 SPI 协议的扩展，用于 SD 存储卡。SDIO 的想法是，你可以把全球定位系统或其他东西插到你 PDA 的 SD 卡槽里。我们已经没有 PDA 了，但是 SDIO 规范仍然存在。

[ajlitt]找到了一个用于 ESP8089 芯片的 SDIO 驱动程序，并发现可以通过移除占用 SPI 线的闪存芯片来释放 ESP8266 的 SPI 总线。将 ESP8266 上的 SPI 线路连接到 Raspberry Pi 上的 SDIO 线路，其余的由驱动器处理。顺便说一下，“其余的”包括启动 ESP 的处理器，通过 SPI/SDIO 线向其注入新的固件，以说服它充当 SDIO WiFi 适配器，以及驱动程序所做的所有其他硬件通信工作。

结果是无需 USB 的 WiFi 连接，只需要一些合理的细间距焊接，并且[不像这个黑客](http://hackaday.com/2015/11/28/first-raspberry-pi-zero-hack-piggy-back-wifi/)你不必担心 USB 总线争用。所以现在你可以给你的 5 美元的电脑加一个 2 美元的 WiFi 板，你仍然可以免费使用 USB。它没有专用的 WiFi 加密狗快，但它能完成任务。接招吧，[哈卡戴自己的【路德·梅里安】](http://hackaday.com/2015/12/01/raspberry-pi-zero-or-minus-one/)！

感谢[J0z0r]的提示！