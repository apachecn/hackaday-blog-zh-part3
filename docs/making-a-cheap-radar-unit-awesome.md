# 让一个便宜的雷达装置变得很棒

> 原文：<https://hackaday.com/2017/08/10/making-a-cheap-radar-unit-awesome/>

从一个 5 美元的多普勒雷达模块中榨取最后一滴性能，成功的秘诀是一半硬件，一半固件，全是黑客。

在硬件方面，第一个原型雷达喇叭由纸板制成，周围贴有铝箔。随着概念的验证，[JBeale]用薄覆铜板制作了第二个喇叭，但据报道，性能几乎相同。另一个硬件黑客只是在雷达模块的模拟输出上钉一根线，并添加一个简单的运算放大器增益级，从而将检测范围扩展到 10 英尺左右，这是这些东西通常用于的范围。

随着所有这些信号进入，[JBeale]通过对多普勒频移信号进行 FFT 来分离出噪声。假设人们每小时行走约 2.2 英里，[JBeale]将注意力集中在相应的 70 赫兹频率上，发现雷达可以探测到 80 英尺外的人。哇！

这种利用廉价雷达设备放大信号来做有用的事情的技巧对黑客来说并不新鲜。[Mathieu]在 2013 年用[完全相同的 HB-100 单元做到了这一点，然后又用](http://hackaday.com/2013/08/14/making-the-electronics-for-a-doppler-motion-sensor/)[更现代的 CDM324 型号](http://hackaday.com/2017/03/31/the-right-circuit-turns-doppler-module-into-a-sensor/)做到了这一点。但是[JBeale]被黑掉的 horn 和聪明的后端处理突破了你可以用这些廉价单元做什么的限制。值得称赞。

【通过[查看](https://www.pjrc.com/low-cost-doppler-radar/)