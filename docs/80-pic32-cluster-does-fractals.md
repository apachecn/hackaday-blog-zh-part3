# 80-PIC32 集群不分形

> 原文：<https://hackaday.com/2016/12/19/80-pic32-cluster-does-fractals/>

绕过计算资源限制的一个方法是投入更多的计算机来解决这个问题。这就是为什么即使是廉价的消费级电脑和手机也有多个内核。在超级计算中，拥有许多具有复杂共享机制的处理器是很常见的。

[亨克·维尔比克]决定用 80 块便宜的 PIC32 芯片[构建他自己的集群](https://www.zapptronics.com/diy-parallel-computing),所有东西都用 BASIC 编程。这些设备通过 I2C 相互通信。他的示例应用程序在另一台具有 VGA 输出的基于 PIC32 的计算机上绘制分形。你可以在下面看到该设备运行的视频。

从板很简单，使用跳线在 I2C 总线上选择不同的地址。每个都有一个多色 LED，显示何时正在执行任务以及任务何时完成。所以从闪光灯的角度来看，电脑是成功的。

这种设置的一个问题是如何有效地在处理器之间进行通信。[Henk]发现 I2C 是瓶颈。尽管他有 80 个 CPU，但他发现如果应用超过 12 个处理器，分形程序就会停滞不前。

Hackaday 的一个好处是，你永远不必问自己为什么要做这样的事情。事实是，作为并行超级计算机，这可能不太实际。但这仍然是一个有趣且有教育意义的项目，可能是我们见过的一起运行 BASIC 的 CPU 最多的项目。

当然，一簇簇的树莓馅饼并不新鲜。我们也看了一些更实用的。

[https://videopress.com/embed/G99TUlky?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0](https://videopress.com/embed/G99TUlky?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0)