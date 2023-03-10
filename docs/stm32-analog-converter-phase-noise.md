# STM32 模拟转换器相位噪声

> 原文：<https://hackaday.com/2017/05/01/stm32-analog-converter-phase-noise/>

[Avian]一直在使用 STM32 ARM 处理器对各种应用的 RF 进行采样。起初，他接收的电视信号相对较宽。不过最近，他开始处理非常窄的信号，他发现[他的样本在频域中有很多他没有预料到的扩展](https://www.tablix.org/~avian/blog/archives/2017/04/phase_noise_in_microcontroller_adcs/)。

接下来是一些检测工作，最终确定相位噪声是罪魁祸首。但是为什么呢？[Avian]进行了一些测量，发现相位噪声几乎完全符合 STM32 锁相环(PLL)的相位噪声规格。

不幸的是，在不对电路的其余部分进行重大修改的情况下，似乎没有一种好方法可以避免使用 PLL。然而，当指望内置转换器进行高精度测量时，这是一次很好的学习经历和需要注意的事情。

这篇文章最大的好处之一是提供了更多信息的参考。有关于相位噪声的精彩解释，以及关于时钟抖动和模拟转换器的具体应用笔记。

我们已经多次讨论过直接数字合成中的[相位噪声。但通常情况下，这是非常明显的，就像你要求](https://hackaday.com/2015/10/13/triple-frequency-vfo-on-a-bamboo-breadboard/)[一个 CPU 兼做射频发射器](https://hackaday.com/2015/02/16/morse-code-rf-transmitter-from-a-micros-clock-output/)。(艾维安的)帖子更像是一个侦探故事。