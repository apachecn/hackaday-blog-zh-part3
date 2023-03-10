# 通用芯片分析仪:在几秒钟内测试旧的 CPU

> 原文：<https://hackaday.com/2018/04/11/universal-chip-analyzer/>

如今，收集旧 CPU 并重新启动它们非常流行，但是你怎么知道它们是否会工作呢？对于这些几十年前就已经停产的集成电路来说，从次品和假货中挑选好货是一个雷区。

测试旧芯片本身就是一个挑战。即使您可以找到正确的主板，逃脱时间对组件的影响(特别是电容器和 EEPROM 退化)的可能性很小，这使得可靠的测试设置很难实现。

进入【Samuel】，进入[通用芯片分析仪](https://x86.fr/uca/) (UCA)。使用 FPGA 来模拟主板，这意味着测试 IC 只需几秒钟的时间。为什么选择 FPGA？微控制器太慢了，以至于不能与 CPU 进行全速接口，即使是 80 年代的接口。

那么，它实际上是如何测试的呢？FPGA 内部集成了 CPU 需要主板才能运行的一切，包括 rom、RAM、总线控制器、时钟生成和中断处理。支持许多测试频率(这有助于识别假货)，如果通过 USB 连接到计算机，UCA 可以检查功耗，甚至对芯片进行基准测试。从自动检测数据总线宽度到支持的型号数量，我们无法在此详细介绍设计中考虑的因素，但您可以在此阅读更多技术细节[。](http://www.cpu-world.com/forum/viewtopic.php?t=29971)

Mojo v3 FPGA 开发板被选为该项目的核心，采用 ATmega32U4 和 Xilinx Spartan 6 FPGA。你们中的老谋深算者已经发现了一个问题——早期 CPU 使用的电压水平差异很大(英特尔 4004 的电压水平高达 15V)。[Samuel]降低成本的巧妙解决方案是为每个 IC 系列提供一个屏蔽，每个系列都有自己的电压转换器。

然而，由于需要存储不同盾牌的 FPGA 配置，Mojo 的板载 EEPROM 无法胜任工作，需要从 4MB 升级到 128MB。幸运的是，这种元件开关不需要对 PCB 进行任何更改，尽管 ATmega32U4 固件以及用于 FPGA 固件上传的原始工具必须进行修改。

兼容 IC 的列表令人印象深刻:Intel 8085/8086/8088、Zilog Z80、RCA/COSMAC 1802、NSC800、Intel 8051 & 8048 只是目前支持的几个系列，更多的系列正在以惊人的速度增加！RAM 和 BSP 的屏蔽也在进行中。

根据兴趣，[Samuel]正在考虑一个非盈利的 Kickstarter 或 Indiegogo，所以如果你喜欢它，一定要发表评论！

 [https://www.youtube.com/embed/ic-VPV17CHI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ic-VPV17CHI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

