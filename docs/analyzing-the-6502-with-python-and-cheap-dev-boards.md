# 使用 Python 和廉价开发板分析 6502

> 原文：<https://hackaday.com/2017/10/29/analyzing-the-6502-with-python-and-cheap-dev-boards/>

以前的时代充满了花哨的逻辑分析仪。将这些分析仪上的导线连接到一个系统上，找到那个超级特殊的 ROM 盒，你就可以实时观察计算机系统的总线。从那时起，我们已经走过了漫长的道路。现在，我们有了可以同时查看多个输入的快速、廉价的硬件，也有了显示和解释数据总线上的 1 和 0 的开源解决方案。[【猪仔】用 Sigrok 和一个便宜的 16 通道逻辑分析仪搭建了一个非常聪明的 6502 协议解码器](http://forum.6502.org/viewtopic.php?f=4&t=4963)。

这个协议解码器能够查看基于 6502 的计算机的数据总线上的 1 和 0。现在，[猪仔]能够将 200 万个 6502 周期直接传输到内存中，因此他能够捕捉到 BBC 微型电视的整个启动序列。这种构建的硬件首先是 Papilio One FPGA 板上的开放式逻辑嗅探器。这个硬件被改成了一个非常便宜的 Cypress FX2 开发板，它被重新配置成一个 16 通道逻辑分析仪。

软件栈才是真正的亮点，在 stardot 论坛上[hoglet]记录了大部分构建[。基本的捕获是通过 Sigrok 完成的，Sigrok 是一个开源的信号分析工具链。这个项目比简单地将 1 和 0 记录到文件中更进一步。【hoglet】用 Python 设计了一整套 6502 协议解码器。这里有一些奇妙的东西:这是[hoglet]的第一个主要 Python 项目。](http://stardot.org.uk/forums/viewtopic.php?p=182742#p182742)

为了捕捉来自 6502 的 1 和 0，唯一的连接是数据总线上的 8 个引脚，RnW、Sync、Rdy 和 Phy2。这只有 12 个引脚，没有连接到地址总线，但协议解码器很快开始预测当前的程序计数器应该是什么。这真的是一件了不起的工作，在任何 6502 计算机上实现完整的堆栈跟踪，部分成本不到 20 美元。