# 10 美元开发板上的 PSoC VGA

> 原文：<https://hackaday.com/2015/12/27/psoc-vga-on-a-10-development-board/>

我们一直认为柏树是一种有趣的动物。这是一个具有功能块的 CPU，您可以配置它来构建各种 I/O 设备，包括使用 Verilog 合并 FPGA 逻辑。[MiguelVP]有一个优秀的多部分项目，即[从 PSoC](http://www.eevblog.com/forum/projects/no-bitbanging-necessary-or-how-to-drive-a-vga-monitor-on-a-psoc-5lp-programmabl/) 产生 VGA 输出。到目前为止，它只是生成一个固定的模式，但帧缓冲区正在工作中，并且有很多关于如何为该任务配置 PSoC 的细节。

虽然 PSoC 具有一些模拟功能，但[MiguelVP]使用廉价的 R2R DAC 和 VGA 连接器来连接 VGA 监视器。你可以花大约 10 美元买到这个项目使用的相同的 PSoC 板。不幸的是，该软件只适用于 Windows，所以如果你运行 Linux 或 Mac，请准备好启动一个虚拟机。我们自己的[Bil Herd]做了一个关于 PSoC 的视频介绍，你可以在休息后观看。

帖子多集中在芯片的配置上(有大量截图)。然而，Verilog 有足够的评论和足够的操作理论，如果你对 VGA 逻辑如何工作更感兴趣，你仍然会发现这篇文章是值得的。

驱动一个 VGA 并不那么困难，我们已经看到用[小型 CPU](http://hackaday.com/2015/12/17/attiny-does-170x240-vga-with-8-colors/)甚至 [7400 TTL 逻辑](http://hackaday.com/2015/10/15/spit-out-vga-with-non-programmable-logic-chips/)就能做到。然而，重点不在于 VGA 的驱动，而在于它是帮助您开始使用 PSoC 的一些华而不实的东西。

 [https://www.youtube.com/embed/3h-TkP-iInM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3h-TkP-iInM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

