# 了解使用 ICL71xx 的 3 位 ADC

> 原文：<https://hackaday.com/2017/01/31/get-to-know-3%c2%bd-digit-adcs-with-the-icl71xx/>

在翻我的旧项目箱时，我发现了一个我在 80 年代做的项目——一个发表在荷兰/英国 *Elektor* 杂志上的汽车万用表。它可以测量低电压 DC，高电流 DC，电阻，停顿角，发动机转速，并运行了一个单一的 9V 电池。除了用于停顿和 RPM 测量的 555 IC 和几个 CMOS 门芯片外，电路板的其余部分由少量无源器件和一个大的 40 引脚 DIP IC 组成，位于 3 位 LCD 显示器下方。我在盒子里又挖了一些，想出了当时的另一个 Elektor 项目——一个真正的 RMS 数字瓦特计，带有 3 位 LCD 显示器，测量功率高达 2kW。它也有同样的芯片。再深入调查，我发现了一个数字面板表。这有一个 7 段 LED 显示屏，但芯片也是来自同一家族。

![ICL7107 LED version](img/9ce9cda8a48b55f94d6725113e1dc9a4.png)

ICL7107 LED version

从 80 年代或 90 年代的任何具有 3 或 4 位、7 段、LCD 或 LED 的设备的罩下看，您可能会发现这种带有 Intersil 标志的 40 引脚 DIP(尽管后来许多其他晶圆厂也生产这种产品；哈里斯和马克西姆等)。承担所有重任的芯片很可能是 ICL7106 或 ICL7107。这些器件被描述为高性能、低功耗、3 位模数转换器，内置 7 个段解码器、显示驱动器、基准电压源和时钟。简而言之，一切你需要采取 DC 模拟信号，并显示它。随着时间的推移，产生了一系列的设备:

*   [7106](http://www.intersil.com/en/products/data-converters/precision-a-d-converters/integrating-display-output-a-d-converters/ICL7106.html)–3 位 7 段液晶显示器
*   [7107](http://www.intersil.com/en/products/data-converters/precision-a-d-converters/integrating-display-output-a-d-converters/ICL7106.html)–3 位，7 段 LED
*   [7116](https://www.maximintegrated.com/en/products/analog/data-converters/analog-to-digital-converters/ICL7116.html)–3 位 7 段 LCD，带显示保持(冻结)
*   [7117](https://www.maximintegrated.com/en/products/analog/data-converters/analog-to-digital-converters/ICL7116.html)–3 位 7 段 LED，带显示保持(冻结)
*   7126–改进的 7106
*   7136–改进的 7126
*   [7135](http://www.intersil.com/en/products/data-converters/precision-a-d-converters/integrating-display-output-a-d-converters/ICL7135.html)–4 位 7 段液晶显示器

有许多类似的器件可用，但 ICL71xx 系列是迄今为止最受欢迎的器件之一，因为它易于使用，零件数量少，单芯片实施。这里有几个部分(链接到 PDF 数据表)来说明我的观点: [TC14433/A](http://ww1.microchip.com/downloads/en/DeviceDoc/21394d.pdf) 需要几个外围设备， [ES5107](http://www.cyrustek.com.tw/spec/ES5107.pdf) (克隆的克隆——阅读下文)， [CA3162](https://www.intersil.com/content/dam/Intersil/documents/ca31/ca3162.pdf) (具有 BCD 输出，需要 CA3161 或类似器件与显示器接口)，或者 [AD2020](http://www.analog.com/media/en/technical-documentation/obsolete-data-sheets/AD2020.pdf) (也需要大量支持电路)。

ICL71xx 成为首选设备是有原因的。让我们来看看这个迷人的芯片背后的工程和业务。

### 诉讼

首先，讲一点历史。1977 年，福禄克推出了 8020A 型，这是他们的第一款手持数字多用表。里面是一个标记为 429100 的芯片——A/D 转换器和显示驱动器。该芯片由 Fluke 与 Intersil，Inc .合作开发，Intersil，Inc .由 Jean Hoerni 于 1967 年创建，生产数字手表和计算器微处理器。8020A 推出一年后，Intersil 推出了 ICL7106，这是 429100 的克隆产品。

为了使其功能不同，Intersil 屏蔽了允许 429100 在 200mV 和 2V 范围之间自动调节的开关(这是福禄克的专利)。这使得 7106 不适合作为 429100 的直接替代产品。但福禄克发现 7106 内部的硅仍然带有福禄克的标志，一场诉讼随之而来。这是庭外解决，因为福禄克无法承受失去 Intersil 的工厂设施。但 7106 现在可供所有人使用，并将最终出现在当时制造的大量产品中。你可以在 [EEVblog 论坛](http://www.eevblog.com/forum/testgear/history-of-the-fluke-8020-series/)上阅读这段时间在 Fluke 工作的【drtaylor】回忆这件事。

### 快速进带

如果我们今天要设计类似的产品，7106 肯定会被微控制器和更强大的模拟前端所取代。我们可以从运行 SPI 或 I C 等标准协议的各种类型的显示器中进行选择。但 7106 及其系列中的其他产品在首次推出近 40 年后的今天仍然可用。似乎仍有许多使用案例证明选择这种设备是合理的。尤其是如果产品需要简单的设计，不需要连接到计算机，必须是手持的，功耗低，并且不需要任何软件校准。

### 在后台

连接到 7106 的一堆无源器件是构建一个使用 9V 电池、能够测量 200mV 输入的设备所需要的全部。2V 范围需要一些元件变化(C2、R2、C3 ),在输入端增加一个分压器可以测量更高的电压。可以使用 trimpot (R4+R1)来调整芯片的参考电压，从而完成校准。

![7106 reference circuit](img/6342fd4fe1249e9a9115c43044fbf544.png)

差分输入和可调基准电压允许应变仪、称重传感器或类似比率电桥型输入等传感器轻松接口。例如，很多这样的芯片被用于称体重。

为此，该器件使用“积分型模数转换”方法，也称为双斜率转换。这个 [Wiki 存根](https://en.wikipedia.org/wiki/Analog-to-digital_converter#Integrating)简洁地解释了这个过程。这一分为三的过程需要 4000 个时钟周期(如果是 4 位器件，则需要 40000 个周期)，自动调零阶段需要 1000 个周期，信号积分阶段需要 1000 个周期，解积分或参考积分阶段需要多达 2000 个周期。为了实现 50Hz 噪声抑制，信号积分相位需要是 50Hz 的倍数。例如，为了获得对 50Hz、60Hz、400Hz 和 440Hz 噪声的良好抑制，振荡器需要处于 40kHz，并且每 2 秒产生 5 个读数。因此，振荡器部分(R3，C4)需要特殊选择。

影响性能的另一个参数是其内部基准电压的稳定性。许多情况下，一个简单的分压器连接到调节供电轨，以获得基准电压。但为了提高性能，强烈建议使用更稳定的基准电压源，使用齐纳二极管或专用基准电压(带隙)器件。

LED 版本 7107 和 7117 遇到了另一个问题，即自热导致的板载参考电压不稳定。与 LCD 相比，LED 消耗的电流要高得多，内部发热会导致性能大幅下降。为了帮助解决这一问题，Intersil 提供了一种带有“S”后缀的特殊设备，仅用于 LED 版本。

走在记忆的车道上是非常有趣的，尤其是像这样的零件，它们隐藏在如此多的套件和产品中。你们有什么有趣的 ICL71xx 故事可以在评论里分享吗？本文建立在[Jenny List]的想法基础上，从她的 *[开始，用 a 723](http://hackaday.com/2016/12/02/get-to-know-voltage-regulators-with-a-723/)* 了解电压调节器。如果你有一个心爱的部分非常适合这种治疗，我们很乐意在下面听到它。