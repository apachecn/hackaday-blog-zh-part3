# 关于逻辑探头你需要知道的一切

> 原文：<https://hackaday.com/2017/07/29/everything-you-need-to-know-about-logic-probes/>

我们刚刚花了最后一个小时[看了一个视频](https://www.youtube.com/watch?v=dobU-b0_L1I)，嵌入在下面，这是关于一个主题的最全面的信息宝库，我们都应该了解更多——嗅探逻辑信号。当然，这是一个很长的视频，但是[OpenTechLab]的[Joel]已经竭尽全力了。

[![](img/df86c2bf09eb2ef774d10b85640237f2.png)](https://hackaday.com/wp-content/uploads/2017/07/mpv-shot0001-shot0004_norm.jpg) 视频的中心是开源的 [sigrok](https://sigrok.org/wiki/Getting_started_with_a_logic_analyzer) 逻辑捕获和分析器。它很棒，因为它支持各种各样非常便宜的硬件平台，包括 Salae logic 及其克隆产品。逻辑是它的亮点，但它甚至会记录来自某些示波器、万用表、电源、[和更多](http://sigrok.org/wiki/Supported_hardware)的数据。sigrok 不仅可以将原始电压解码成比特，还可以使用 Python 编写的[协议解码器插件](https://sigrok.org/wiki/Protocol_decoders)来解释这些比特。这一切意味着有一天，它将解码一切。免费的。

[Joel]对 sigrok 略知一二，因为他为它启动了令人难以置信的光滑的 [PulseView](http://sigrok.org/wiki/PulseView) GUI 项目，但这并不妨碍他带你通过命令行界面，这对于自动化数据捕获和分析非常有用，如果这是你喜欢的那种东西的话。两者都值得了解。

但其实是硬件细节让这段视频大放异彩。他在工作台上分解了所有的逻辑探针，指出了它们的设计优缺点，并以此为基础解释了 20 美元左右的价格可以带来什么样的性能。您将对整个工具链有一个深入的了解，从 grabber 探针到 GUI。

事实上，到最后，[Joel]模拟了使用跨线连接器的寄生电感，并演示了它如何破坏高频信号。即使逻辑分析仪能够足够快地采样，也没有信号能走那么远。但是他不会对这个问题挥挥手——他会向你展示。然后，他提到了对核心黑客友好的技术，以达到数百兆赫，并向[Bunnie Huang]致敬。

在我们看来，sigrok 及其支持的 el cheapo 硬件逻辑探测器应该在每个黑客的工具箱中占有一席之地。这个视频是我们所见过的对这个软件和这个主题最好的介绍。

我们从[OpenTechLab]中精选了另外两个视频，一个是关于 [ICE40 FPGA](http://hackaday.com/2017/04/13/lattice-ice40-fpga-configured-by-linux-kernel/) 的，一个是关于[高频合成](http://hackaday.com/2017/04/12/4-4-ghz-frequency-synthesis-made-easy/)的，你可能也会喜欢。所以，收起架子上那些脑残的好莱坞大片，为高质量的书呆子时光做些爆米花吧。

 [https://www.youtube.com/embed/dobU-b0_L1I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dobU-b0_L1I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

