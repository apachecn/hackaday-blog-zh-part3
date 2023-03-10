# 在 ESP8266 上运行 RepRap

> 原文：<https://hackaday.com/2016/09/06/run-a-reprap-on-an-esp8266/>

5 美元的小 WiFi 模块不能做什么？现在【lhartmann】已经有了一个 [ESP8266 来控制 3D 打印机](http://forums.reprap.org/read.php?2,594898)的电机，这是清单上的又一个检查项目。

这个项目最酷的地方在于[lhartmann]的工作方式。小小的 ESP8266 远远没有达到所需的 GPIO 引脚数量，主 SPI 连接到板载闪存，辅助 SPI 记录很少，几乎没有人使用它。所以，[lhartmann]选择使用 I2S 输出。

I2S 通常是一种音频协议，所以乍一看这似乎是一个奇怪的选择。虽然 I2S 听起来像 I2C，但它实际上是一个 SPI 协议，第四根线交替指定右声道或左声道。实际上，它非常适合以高数据速率发送 16×2 位数据。

[lhartmann]将这 32 位送入[四个移位寄存器](https://github.com/lhartmann/Shift-out-32-HC595)，仅从四条 I2S 数据线产生 32 个输出。这些信号足够运行步进电机了。由于它以 192 kHz 的采样速率更新，足以驱动它们。

这项技术的另一个好处是，只需一点点软件，它就可以在单板计算机上工作。编程非常复杂的步进运动，然后成为一个问题，只是产生正确的“音频”文件，并播放出来。[lhartmann]之前用一个橙色 Pi 演示了这个[。那也很酷。](http://forums.reprap.org/read.php?2,685993)

将 ESP8266 和少量 74HC595s 转变为 3D 打印机控制器的代码在 GitHub 上[发布，所以去看看吧。](https://github.com/lhartmann/esp_rtos_reprap)

谢谢你的提示！