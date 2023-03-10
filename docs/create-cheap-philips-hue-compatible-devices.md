# 创造廉价的飞利浦色调兼容设备

> 原文：<https://hackaday.com/2017/03/01/create-cheap-philips-hue-compatible-devices/>

飞利浦 Hue 系列是为您的家庭添加无线可控照明的绝佳方式，但协议是专有的，这使得我们很难添加自己的定制硬件。[Peter]找到了一种方法，基于能够连接到色调桥的廉价 JN5168 模块，创建自己的[色调兼容设备](https://peeveeone.com/?p=187)。这意味着您可以使用廉价的 RGB 或白色 led、电源和 JN5168 Zigbee Light Link 模块推出自己的灯具。

他开始尝试将 Zigbee Light Link 设备克隆到 MeshBee 上，mesh bee 是 Seeed studio 基于恩智浦 JN5168 的开源 Zigbee Pro 模块。即使 MeshBee 使用与色调灯相同的设备，它也不会连接到色调桥。但他从当地五金店购买的另一款名为 Innr 的克隆灯确实很容易连接。使用恩智浦的开源工具，他能够从 Innr 下载 flash 和 EEPROM 内容，并将其复制到 MeshBee 中。

在 EEPROM 传输技巧之后，他想出了如何修改用于 ZigBee 协议的两个密钥——一个用于家庭自动化，另一个用于 Light Link。有了这个最终的发现，他就能够使用 Beyond Studio 编辑 ZigBee Light Link 演示项目，然后在 MeshBee 设备上加载二进制文件，以便它可以连接到 Hue bridge。

所有这些工作最终产生了[两个定制的固件二进制文件](https://github.com/peeveeone/ZLL_Lights)；一个用于白光可调光灯，另一个用于 RGB 可调光灯。它甚至可以在他花几块钱找到的这些[便宜的 JN5168 突破套件](http://www.nkcelectronics.com/JN5168-breakout-PCB-KIT-PCB-Version-2_p_613.html)上运行。有了所有的软件，有了便宜的 ZigBee Light Link 兼容模块，构建低成本色调兼容灯就变得非常简单了。

谢谢你的提示。