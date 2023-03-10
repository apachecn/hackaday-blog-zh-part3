# 深度神经网络的硬件

> 原文：<https://hackaday.com/2017/09/08/hardware-for-deep-neural-networks/>

如果您今年没有参加 ISCA(国际计算机及其应用协会)会议，您可能会对麻省理工学院教授兼 NVIDIA 科学家 Joel Emer 的演讲感兴趣。与另一位麻省理工学院教授和两名博士生([Vivienne Sze]、[Yu-Xin Chen]和[Tian-Ju Yang])一起，[Emer]的演讲涵盖了深度神经网络的硬件架构。

本报告涵盖了深度神经网络的背景和基本理论。然后进展到深度学习细节。一个有趣的图表显示了神经网络如何每年在识别图像中的物体方面变得更好，截至 2015 年，在一组测试图像上，神经网络可以比人类做得更好。然而，真正的关键是使用硬件来加速网络的性能。

硬件加速很重要，原因有几个。首先，许多应用程序都有大量相关数据。此外，培训可能涉及许多迭代，这可能需要很长时间。

本演示涵盖了更多内容:工具概述、当前可用的硬件，以及对用于网络不同层的不同内核(算法)的探索。然而，真正的问题是如何构建硬件来最好地实现这些内核。在这项任务中使用并行元素是显而易见的，但是这篇论文指出内存访问是瓶颈。有几种策略可以降低通过网络访问数据的成本。这些策略利用了数据重用和结果的本地累积。但是，也可以通过使用单个内存池以牺牲性能为代价来降低功耗。

在文章的最后，我们仔细研究了不同的内存拓扑和设备。这包括在 IC 级使用忆阻器和存储单元堆。如果你正在寻找一个完整但可访问的深度神经网络景观的调查，这个演示的前半部分左右会让你很感兴趣。后面的部分更详细，如果你只是一个好奇的黑客，可能对你没什么用。但是如果你正在为神经网络开发 ASIC 甚至 FPGA 架构，这是很棒的东西。

我们最近谈论了很多关于神经网络的话题。这里有大量的[课程](https://hackaday.com/2016/12/21/practical-deep-learning/)和[教程](https://hackaday.com/2017/03/14/google-machine-learning-made-simpler/)让你入门。