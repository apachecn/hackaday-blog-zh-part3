# arm 和 FPGAs 构成有趣的开发板

> 原文：<https://hackaday.com/2015/10/07/arms-and-fpgas-make-for-interesting-dev-boards/>

微型 Linux 计算机随处可见，在 BeagleBones、Raspberry 和 Banana Pis 以及其他上百种主板之间，有足够多的选择。Xilinx 公司有一款非常有趣的 ARM 芯片，在小型信用卡大小的计算机领域还没有被广泛采用:Zynq。它是一个 ARM Cortex-A9 和一个 FPGA。它非常适合构建通常不会包含在微控制器中的外设。使用 Zynq，您只需在 FPGA 中实例化自定义位，然后将它们与自定义 Linux 驱动程序连接。多亏了 CrowdSupply，现在有一个主板将这个有趣的芯片[带到一个合适的开发平台](https://www.crowdsupply.com/krtkl/snickerdoodle)。它被称为 Snickerdoodle，如果您想了解与快速处理器紧密耦合的 FPGA 的功能，这是值得一看的主板。

Snickerdoodle 的核心是一个 [Xilinx Zynq](http://www.xilinx.com/products/silicon-devices/soc/zynq-7000.html) ，它具有 667 MHz ARM Cortex A9 和 430k gate FPGA(在低端配置中)或 866 A9 和 1.3M gate FPGA。这给了 Snickerdoodle 多达 179 个 I/O 端口——远远超过任何其他小型 Linux 主板。

满载时，Snickerdoodle 配备了 2.4 和 5GHz WiFi、蓝牙、1GB 内存和 ARM Cortex A9，在功能上应该远远超过 BeagleBone 和 Raspberry Pi 2。不过，这是有代价的:顶级的 Snickerdoodle 的底价约为 150 美元。

尽管如此，快速 ARM 和大型 FPGA 的强大功能仍然具有很大的吸引力，我们预计未来会有更多这样的 Zynq 板。甚至有几个项目在 hackaday.io 上使用 Zynq，其中一个项目[将 Zynq 放在一个兼容 Raspberry Pi 的位置](https://hackaday.io/project/7817-zynqberry)。这太酷了，我们迫不及待地想看看人们会用一个小型、快速的 ARM 板和 FPGA 构建什么。