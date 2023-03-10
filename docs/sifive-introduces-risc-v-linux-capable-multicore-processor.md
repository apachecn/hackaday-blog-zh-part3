# SiFive 推出支持 RISC-V Linux 的多核处理器

> 原文：<https://hackaday.com/2018/02/03/sifive-introduces-risc-v-linux-capable-multicore-processor/>

RISC-V，从微控制器到服务器 CPU 的开源架构，正在缓慢但肯定地进入社区。现在，SiFive，将 RISC-V 芯片植入实际硅片的主要公司，正在发布一种更强大的芯片。在本周末的 FOSDEM 上，SiFive 宣布发布一款基于 RISC-V ISA 的支持 Linux 的单板计算机。它被称为 HiFive Unleashed ，是第一款能够在 RISC-V 内核上运行 Linux 的芯片。

[![](img/6fcdbb44f2591dab960056f0d39cd3e6.png)](https://hackaday.com/wp-content/uploads/2018/02/hifiveunleashed.jpg)

SiFive’s HiFive Unleashed

HiFive Unleashed 围绕 Freedom U540 SOC 构建，这是一款基于 28 纳米工艺构建的四核处理器。该芯片本身拥有四个 U54 RV64GC 核心和一个额外的 E51 RV64IMAC 管理核心。该芯片支持带 ECC 的 64 位 DDR4 和一个千兆以太网端口。这些规格只是芯片，你真的需要一个单板计算机的完整系统。这是 HiFive Unleashed，一款配有 Freedom U540、8GB 带 ECC 的 DDR4、32MB 四通道 SPI 闪存、千兆以太网和一个用于存储的 microSD 卡插槽的主板。如果你不介意在向一个技术青年描述这个的时候有一点不准确，你可以说这相当于一个 Raspberry Pi，但是有一个完全开源的架构。

然而，这种口径的消息不会没有一些失望，在这种情况下，HiFive Unleashed 将于今年夏天上市，价格为 999 美元。是的，与 Raspberry Pi 或 BeagleBone 相比，这是一个非常高的价格，但必须记住，这是一个定制的芯片和 28 纳米工艺上的低容量硅。在路由器或手机制造商为一些商用设备选择 RISC-V 芯片之前，这种架构将非常昂贵。

这款全单板计算机的发布是在 SOC 本身的发布之后几个月发布的。GCC 支持已经起作用，Linux 的东西正在向上游发展，整个开源社区似乎对 RISC-V 相当热情。很高兴看到未来几年的发展趋势，以及我们何时能以不到一千美元的价格获得支持 Linux 的 RISC-V 芯片。