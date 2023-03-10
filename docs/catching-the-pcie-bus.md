# 赶(PCIe)公共汽车

> 原文：<https://hackaday.com/2018/02/17/catching-the-pcie-bus/>

如果你想学习 FPGAs，你只能用普通的闪光灯和 VGA 输出。最终，你想做更多的事情。虽然不算太便宜，但你可以买到 PCIe 外形的 FPGA 板，并直接与 PC 软件一起使用。容易吗？嗯，它不是闪烁的 LED，但有工具可以帮助。[安杰洛·基里亚科斯]做了一篇关于这个主题的硕士论文，并使用了一个被称为[RIFFA](http://riffa.ucsd.edu/)的项目来帮助完成这项任务。

RIFFA(FPGA 加速器的可重用集成框架)是一个简单的框架，用于通过 PCI Express 总线从主机 CPU 向 FPGA 传输数据。该框架需要一个支持 PCIe 的工作站和一个带 PCIe 连接器的板上 FPGA。RIFFA 支持 Windows 和 Linux，Altera 和 Xilinx，绑定 C/C++，Python，MATLAB 和 Java。通过适当的设计，RIFFA 可以在短时间内在您的计算机和 FPGA 之间传输相当多的数据。

当然，问题是找到一个合适的 FPGA 板，这些都不便宜。此外，RIFFA 依赖于供应商的 PCIe 端点块。在某些情况下，这些是通过开发工具获得许可的，但在其他情况下，您也必须为此付费，因此请务必了解您选择的 FPGA 和电路板的情况。

当然，RIFFA 不是唯一的选择。OpenCores 上有几个 PCIe 内核，尽管你的里程可能会因硬件支持或它们的通用或完整程度而异。

你只能希望硬件的成本会降下来。目前，RIFFA 的例子使用 Xilinx 板，价格约为 2000 美元。Numato 有一些价格在 300-500 美元之间的主板。这种[板看起来很有前途](https://www.devboards.de/startseite/produkte/produkte-details/article/db4cgx15/)，尽管据我们所知，它们在美国似乎不容易买到。说到美国以外的地方，总会有[和](https://www.enterpoint.co.uk/products/cyclone-iv-development-boards/raggedstone3/)。然而，这些主板都没有低于 100 美元的范围，所以要准备支付一些钱。

但不要因此而分心。我们之前已经讨论过如何利用 FPGAs 以很少的投资做很多事情。此外，你可以不使用 PCIe 界面与电脑对话。使用串口，或者以太网，或者[甚至 SPI](https://hackaday.com/2016/01/20/a-linear-time-sorting-algorithm-for-fpgas/) 。它可能没有带宽，但会便宜很多。