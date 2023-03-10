# 开源 96 MSPS 逻辑分析仪，售价 22 美元

> 原文：<https://hackaday.com/2016/10/26/an-open-source-96-msps-logic-analyzer-for-22/>

如果你在市场上寻找一个便宜的 USB 逻辑分析仪，你有几个选择，但很少有人在性能方面提供很多。中国有几美元的套件，核心使用微控制器，但它们无法提供显著的采样率。如果你要求更多，你将不得不支付它。

因此，看到[kevinhub88]的[sump 2 项目](https://blackmesalabs.wordpress.com/2016/10/24/sump2-96-msps-logic-analyzer-for-22/)是相当有趣的，这是一个开源逻辑分析仪，据称具有 96 MSPS 采样率，使用现成的[Lattice ice stick FPGA 评估板](http://www.latticesemi.com/icestick)，仅花费约 20 美元。~~它通过 USB 使用已建立的 SUMP 协议与主机对话，所以它的软件前端来自[sump.org 逻辑分析仪项目](https://sump.org/projects/analyzer/)~~ 。编辑:自从这篇文章发表后，[Kevin]联系了我们，告诉我们这个项目的能力已经超越了 SUMP 的能力，事实上它现在使用了自己的软件。

该项目有望为预算有限的工程师增加一件非常有用的测试设备，并为注重成本的读者提供大量文档和安装说明，以及 FPGA 代码。由于 2015 年更令人敬畏的黑客之一，这个晶格部分有一个完全开放的工具链，如果你想尝试一下，我们自己的[Al Williams]已经写了一个多部分入门指南[。无论如何，你可能需要其中的一个，现在它是一个逻辑分析器来启动。](http://hackaday.com/tag/learning-verilog-for-fpgas/)

这些年来，我们已经在这里介绍了不少廉价的国产数字仪器，包括[这个价格稍高的逻辑分析仪](http://hackaday.com/2009/07/23/open-source-logic-analyzer/)、[这个廉价的 VNA](http://hackaday.com/2016/08/13/a-vna-on-a-200-euro-budget/) 和这个[示波器板](http://hackaday.com/2016/10/06/open-design-oscilloscope-could-be-almost-free/)。也许有一天，我们梦想中的长椅将全部出现在一个 100 美元的开源 PCB 上，谁知道呢！