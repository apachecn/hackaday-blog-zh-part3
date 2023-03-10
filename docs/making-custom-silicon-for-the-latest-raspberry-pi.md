# 为最新的树莓派定制芯片

> 原文：<https://hackaday.com/2018/04/12/making-custom-silicon-for-the-latest-raspberry-pi/>

最新的 Raspberry Pi，Pi 3 Model B+，是 Raspberry Pi Foundation 最新的硬件迭代。不，它没有 eMMC，它不支持蜂窝连接，它没有 USB 3.0，它没有 SATA，它没有 PCIe，它没有对一台 35 美元的计算机的任何其他不切实际的期望。这并不意味着新版 Pi 中没有大量的工程设计；相反，最新的 Pi 充满了定制硅和新技术，它甚至有一个整洁的浮雕射频屏蔽。

在 Raspberry Pi 博客上，[James Adams]回顾了可能是新的 Raspberry Pi 最重要部分的工作。[它的电源中有新的定制硅](https://www.raspberrypi.org/blog/pi-power-supply-chip/)。这是一个为树莓派设计的芯片，这是一个很好的教训，告诉你当你知道你将会制造数百万个东西时你能做什么。

树莓派的前几代产品，从最初的 B 型到 Zero，都使用片内电源。当 RAM 直接焊接到 CPU 上时，这就是你所期望的。随着 Raspberry Pi 2 的推出，RAM 与 CPU 分离，这意味着为更多内核提供更多功率，以及 LPDDR2 内存所需的轨道。Pi 2 需要 5V、3.3V、1.8V 和 1.2V 的电压，以及使它们按顺序上升的顺序。这是电源管理 IC (PMIC)的工作，但令人惊讶的是，所有可用的 PMIC 都比 Pi 2 的分立式解决方案更贵。

[![](img/4985e6b8b48f47577d9e77fd43d2ffa9.png)](https://hackaday.com/wp-content/uploads/2018/04/pipsu.jpg)

The MXL7704, with four switching power supplies. The four symmetric gray and brown bits are inductors.

然而，只要有半导体公司，就有可能定制芯片。[James]在 2015 年与 Exar 的[Peter Coyle]谈过关于构建一个定制芯片来提供树莓 Pi 中的所有电压的问题(Exar 去年被 MaxLinear 收购)。结果是 MXL7704 及时交付，用于生产树莓派 3B+。

新芯片从 USB 端口接收 5V 电压，并将其转换为两条 3.3V 电压轨，1.8V 和 1.2V 用于 LPDDR2 内存，1.2V 标称用于 CPU，可以通过 I2C 升高和降低。这是一个令人印象深刻的工程，正如任何硬件设计师都知道的那样，获得正确的电源是成功产品的第一步。

随着树莓 Pi 3B+中发现的新 MXL7704 芯片，Pi 生态系统现在有了一个简单而廉价的芯片，可用于他们未来的所有修订。它可能不是 SATA 或 PCIe 或 eMMC 或厨房水槽，但这是一种给你一个成功产品的工程，而不是一个很快就会被遗忘的单板计算机。