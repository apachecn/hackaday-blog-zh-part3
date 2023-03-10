# arduino 是 aa 电池中的 arduino

> 原文：<https://hackaday.com/2016/04/18/the-aaduino-is-an-arduino-in-an-aa-battery/>

你可能会想，没有哪种外形是没有安装 Arduino 的。今天早上一个新的来了。[Johan Kanflo]的 AAduino 是一个 Arduino 克隆，带有一个板载 RF 模块，适合 AA 电池的外形。将 Arduino 放入它自己的电池组中，会使它成为一个非常整洁和紧凑的独立单元。

电路板的核心是一个时钟频率为 8MHz 的 ATmega328，以降低功耗，并在 1.7V 时熔断。无线电模块是一个 [HopeRF RFM69C](http://www.hoperf.com/rf_transceiver/modules/RFM69CW.html) ，它在供应时对于 AA 外形来说有点太大，因此[Johan]小心翼翼地锉掉 PCB 的边缘以使其适合。AA 电池的形状为一对 DS18B20 温度传感器和一个指示灯 LED 留出了足够的空间。他为不同版本的 3xAA 带盖盒子提供了方便的购买指南，所有与该项目相关的文件都可以在他的 [GitHub 库](https://github.com/kanflo/aaduino)中找到。

特别是通过板载无线电模块，我们可以看到 AADuino 板是一个非常有用的套件。例如，它可能被用作一个非常低功率的独立节点 [UKHASnet 节点](http://hackaday.com/2016/03/20/licence-exempt-network-has-high-ambitions/)。

这些年来，我们推出了不少 Arduino 克隆产品，试图以某种方式打破尺寸模式。[这个条形板 Arduino](http://hackaday.com/2013/07/10/build-a-bare-bones-arduino-clone-which-maximizes-its-use-of-real-estate/) 几乎但不完全等于 AAduino 的尺寸，[这个 PCB 版本](http://hackaday.com/2008/07/06/really-bare-bones-board-arduino-clone/)仅仅比其处理器的 DIP 封装宽一点。但 AADuino 有点不同，因为它是一个现成的外形，可在现场使用，而不仅仅是另一个试验板设备。我们喜欢这样。