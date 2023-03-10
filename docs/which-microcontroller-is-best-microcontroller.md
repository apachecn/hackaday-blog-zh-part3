# 哪个微控制器是最好的微控制器？

> 原文：<https://hackaday.com/2017/11/07/which-microcontroller-is-best-microcontroller/>

假设你正在做一个项目，你需要一个微控制器。你伸手拿哪个芯片？可能是你最熟悉的那种，或者至少是程序员藏在你桌子角落里的那种。选择微控制器是一个方便的问题，但不一定是这样。光是 ARM 内核就有几十个，8051 克隆有几百个，还有更奇怪的东西，包括 Cypress PSoC 和 TI 的 MSP430。哪个最好？哪个价格低于一美元的微控制器最好？这是[Jay Carlson]试图回答的问题，[，这是我们读过的最好的微控制器枪战](https://jaycarlson.net/microcontrollers)。

[Jay]把十几个成本不超过一美元的微控制器放在一起，形成一个庞然大物。本文包括来自 Atmel 的:ATtiny1616、ATmega168PB 和 ATSAMD10。来自赛普拉斯的 PSoC 4000S。来自飞思卡尔的 KE04 和 KL03。霍尔特克的 HT-66 和英飞凌的 XMC1100。来自 Microchip 的 PIC16、PIC24 和 PIC32。来自 Nuvoton、N76 和 M051。恩智浦 LPC811、瑞萨 RL-78、三洋 LC87 和硅实验室 EFM8。ST 的 STM32F0 和 STM8。STCMicro 的 STC8，最后是 TI 的 MSP430。如果你在家里记录分数，其中大多数都是 ARM 或 8051 风格的核心，但 AVR 和 PICs 增加了“专有”核心设计的数量。

这篇评论和所有的技术评论一样，以技术规格的样本开始。一切都在那里，包括 RAM 的数量到 PWM 通道的数量。[Jay]在这篇评论中更进一步，检查了开发环境、编译器、开发工具，甚至不同内核在三个方面的性能:闪烁位、双二阶滤波器和 DMX 接收器。这方面的工作令人难以置信，目前，这是我们见过的关于微控制器的最佳资源。

有了这些数据和经历了十几个不同的微控制器平台后，[Jay]的收获是什么？STM32F0 很棒，Atmel/Microchip SAM D10 也有很好的性能，但你将依赖于一些第三方库。纯微芯片部件 PIC16、PIC24 和 pic 32——具有无限的产品寿命、广泛的封装和庞大的社区，但使用笨重的 ide 和昂贵的编译器。柏树 PSoC 还可以，PSoC5 或者 PSoC6 会更好。此次测试的惊喜包括瑞萨 RL-78 及其高性能、低成本和测试中最节能的 5V 器件。

说了这么多，最好的微控制器是什么？这是一个愚蠢的问题，因为最好的微控制器总是那个应用的最好的微控制器*。或者你放在零件抽屉里的任何东西，我们从来都不清楚答案到底是什么。也就是说，这是微控制器评论的新高潮，我们希望[Jay]将继续他对价格超过一美元的微控制器的研究。*