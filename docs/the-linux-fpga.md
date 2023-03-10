# Linux FPGA

> 原文：<https://hackaday.com/2017/09/26/the-linux-fpga/>

将 CPU 和 FPGA 放在一起并不罕见。毕竟各有各的优缺点。然而，像 Xilinx Zynq 这样的新设备在同一个封装中既有 CPU 又有 FPGA。这意味着您的设计必须跨越硬件、FPGA 配置和软件。[Mitchell Orsucci]在 ArtyZ7-20 板上使用 Zynq 设备，并决定使用 Linux 来操作 ARM 处理器，并提供用户空间工具来与 FPGA 接口并动态重新配置它。

这听起来像是一个大项目，而且无论如何也不是微不足道的。然而，Xilinx 工具做了很多繁重的工作，包括设置 Linux 内核和合适的根文件系统。[Mitchell]的大部分工作是为 Linux 程序开发用户空间工具，以便与 FPGA 硬件交互。你可以在下面看到一个短视频演示。

该设计为 Linux 端提供了一个 I2C 接口、一个 SPI 接口、一个 PWM 控制器和 10 个数字 I/O 引脚。GitHub 上有[原理图和源代码](https://github.com/mitchellorsucci/ArtyZ720)。

我们已经看到 Zynq 做了从[合成音乐](https://hackaday.com/2015/08/10/zynq-and-the-opl3-music-synthesizer/)到动力[天文摄影相机](https://hackaday.com/2017/01/07/custom-zynqcmos-camera-unlocks-astrophotography/)的所有事情。虽然将软件和硬件结合在一起需要大量的工作，但结果是值得的，工具也会有所帮助。

 [https://www.youtube.com/embed/GSKfWroZNQQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GSKfWroZNQQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

