# 探索 BBC Micro:Bit 软件堆栈

> 原文：<https://hackaday.com/2017/12/02/exploring-the-bbc-microbit-software-stack/>

BBC micro:bit 已经和我们一起工作了大约 18 个月，虽然这个基于 ARM 的小董事会已经在它的目标教育市场上为自己赢得了声誉，但我们在我们的社区中并没有看到我们预期的那么多。

如果您或您生活中的年轻人有一个 micro:bit，您可能已经使用几种基于 web 的 ide 之一、图形编程系统、TypeScript 或 MicroPython 为它创建了代码。但是这些高级语言只是主板软件栈的一部分，正如[Matt Warren]向我们展示的他对各个层次的详细检查。

micro:bit 夹层的顶层当然是你的代码。这被基于网络的 IDE 的编译器转换成一个十六进制文件，然后放在你的设备上。有趣的是，只有微软的 TypeScript IDE 将 TypeScript 编译成本机代码，而其他人用解释器将你的代码打包。

下面是 micro:bit 的硬件抽象层，再下面是 ARM 的 Mbed OS 层，因为 micro:bit 实际上是另一个 Mbed 板。[Matt]详细介绍了该设备的内存映射如何容纳所有这些组件，考虑到只有微不足道的 16kb RAM，这是非常重要的。

您可能希望使用 Mbed 工具链对更接近金属的 micro:bit 进行编程，但即使是这种情况，阅读其官方堆栈的剖析仍然是有意义的。同时，看看[我们对董事会](https://hackaday.com/2016/06/03/hands-on-with-the-bbc-microbit/)的回顾，从 2016 年夏天开始。