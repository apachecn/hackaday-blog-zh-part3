# 如果软件无线电的 I 和 Q 是你的克星，请继续阅读

> 原文：<https://hackaday.com/2017/05/16/if-the-i-and-q-of-software-defined-radio-are-your-nemesis-read-on/>

对于我们这些对无线电感兴趣的人来说，遇到我们的第一个软件定义无线电肯定普遍被视为一个奇迹。这是一个令人惊讶的简单设备，本质上是一个聪明的混频器和一组模数或数模转换器，可以将传统无线电的所有复杂和棘手的设置部分输入到计算机中，其中所有的信号处理都可以使用软件来完成。

[![A quadrature mixer. Jugandi (Public domain).](img/8bf047a2c8f8a4b4630c26ed7a021169.png)](https://hackaday.com/wp-content/uploads/2017/05/quadrature_demodulator.gif)

A quadrature mixer. Jugandi ([Public domain](https://en.wikibooks.org/wiki/File:Quadrature_demodulator.gif)).

当你的好奇心占了上风，开始窥视软件无线电的工作原理时，你会遇到一些在传统无线电中从未见过的事情。有两个混频器，由两个频率相同但具有 90 度相移的本振馈电，在接收机中，产生的混频器乘积馈入两个独立的 ADC。你会遇到与这两条信号路径相关的字母 **I** 和 **Q** ，并想知道这到底是什么意思。

你刚才看到的是一个正交混频器。正交是指任何涉及四分之一圆的数学运算，在这种情况下，两个本地振荡器之间的 90 度相移。这种 90 度相移不仅可以揭示信号中的频率和幅度信息，您可能会从传统无线电中的单个混频器中熟悉这些信息，还可以揭示两个 90 度异相 **I** ( **I** n 相位)和**Q(Q**u 相位)分量信号保留的相位信息。

[![I and Q data as side views of a spiral. Mikael Q Kuisma, I/Q Data for Dummies.](img/158b592b62dd218c66d9be90a8f9a806.png)](https://hackaday.com/wp-content/uploads/2017/05/corkscrew.png)

I and Q data as side views of a spiral. Mikael Q Kuisma, [I/Q Data for Dummies](http://whiteboard.ping.se/SDR/IQ).

如果你想完全弄清楚这是如何工作的，有大量的数学知识需要消化，这可能最好是将好奇的[引向更长的解释](http://whiteboard.ping.se/SDR/IQ)。为了快速理解，最好将示波器上看到的信号的正弦波幅度视图想象为信号的 2D 侧视图，实际上是一个 3D 螺旋，因为它也有相位分量。如果螺旋的这个侧视图是你的 **I** 分量，那么螺旋顶部的一个类似的 2D 视图将是你的 **Q** 分量，相同的信号，但是有 90 度的相位差。从这两个 **I** 和 **Q** 信号可以重构整个原始信号，包括其复杂的相位关系，而不仅仅是示波器上看到的 2D 幅度视图。

[![Producing a 90 degree phase shift with flip-flops.](img/8eea408ee6beffbdec78a22a89705de2.png)](https://hackaday.com/wp-content/uploads/2017/05/phase-shifter1.png)

Producing a 90 degree phase shift with flip-flops.

令人高兴的是，这并不只是教科书中的一个理论，你可以根据上面的正交混频器图轻松构建一个简单的 SDR 接收机前端。如果您准备将接收器的带宽限制在计算机声卡的带宽内，通常在 50 kHz 范围内，您可以将左右音频输入分别用作您的 **I** 和 **Q** ，并运行众多 SDR 应用程序中的一个。 [Linrad](http://www.sm5bsz.com/linuxdsp/linrad.htm) 只是一个例子。

至于硬件，混频器和相关的低通滤波器可以非常简单地构建，例如，您可以尝试使用 CMOS 模拟开关提升[这种设计。虽然您可能认为产生 90 度相移会有问题，但事实上，用一对触发器也可以轻松实现。添加一个逻辑电平振荡器，就有可能实现几乎完全由逻辑芯片构成的软件定义无线电前端，只需几个运算放大器。它的性能不会超过 HF(短波)频率，但即使您只是用它来查看您当地的 AM 广播电台，它仍然可以让您亲自了解 SDR 硬件。](http://www.schripsema.org/pa3hdf/projects/dc-receiver/dc-rx.html)

有时候，SDR 似乎是一个神奇的黑匣子，被一团营销的乌云包围着。除了著名的 RTL 芯片组 USB 电视接收器，它们似乎吸引了与宣传相匹配的价格。但事实是，从硬件的角度来看，它们可能出奇的简单。为什么不拿出一块试验板，自己动手做一个简单的呢！

标题图片:Bob K [ [CC0](https://commons.wikimedia.org/wiki/File:In-phase_and_quadrature_components_of_angle_modulation.gif) 。