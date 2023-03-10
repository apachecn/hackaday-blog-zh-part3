# FPGA 中的树莓 Pi

> 原文：<https://hackaday.com/2016/04/26/a-raspberry-pi-in-an-fpga/>

不知何故，Raspberry Pi 已经成为单板计算机的标准外形。现在有了可以做任何事情的树莓派形状的物体，在 Odroid 和奇异的英特尔凌动主板之间，你想要的一切现在都被打包到看起来像树莓派的东西中。

当然，除了一件事，那就是[antti.lukats]参加 2016 年 Hackaday 奖的原因。他在一个小封装中结合了快速 ARM 处理器和 FPGA 的芯片上创建了一个版本的 Raspberry Pi。它被称为 ZynqBerry ，毫无疑问，它将成为学习 FPGA 诡计的最佳平台之一。

Xilinx 的 Zynq 配备了 1GHZ 左右的双核 ARM Cortex A9，仅从这一点来看，应该可以与最初的 Raspberry Pi 相媲美。Zynq SoC 内部还有一个非常强大的 FPGA，[antti]用它来驱动 60hz 的 HDMI，并可以将视频从 Raspberry Pi 摄像机传输到显示器。

去年的 Hackaday 奖，[antti]展示了一些非常酷的东西，包括一个比 DIP-8 芯片大不了多少的微型 FPGA 开发板[。他是 hackaday.io 的常驻 FPGA 向导，ZynqBerry 是过去一年左右大量工作的高潮。虽然怀疑它是否会像最新的 Raspberry Pis 和 Pi 克隆一样强大，但这是一项非凡的工作，为常见的 FPGA 开发板带来了有趣的变化。](https://hackaday.io/project/6592-dipsy)

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)