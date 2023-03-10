# 请教 Hackaday:在 FPGA 上计算平方根？

> 原文：<https://hackaday.com/2016/12/26/ask-hackaday-computing-square-roots-on-fpga/>

Hackaday reader [nats.fr]用[写了一个项目](https://more-magic.org/2016/12/18/fpga-fast-rough-gamma-correction-for-low-quality-video-stream/)的一些代码，该项目使用 FPGA 动态调整视频流的大小。这样做意味着撤销任何已经应用于原始流的[伽马校正](https://en.wikipedia.org/wiki/Gamma_correction)，调整大小，然后重新应用伽马。为了让生活变得更简单，[nats.fr]选择了 2 的 gamma，这意味着要取一堆平方根，这在 FPGA 上并不快。

[nats]的算法非常简洁:它使用第一阶段的查找来计算值位于哪个较宽的范围内，然后使用 Hero 算法的一个步骤来改进。(我们认为这相当于说他做的是分段线性插值，但我们不能 100%确定。)反正效果还算体面。

当然，当你开始往特殊函数计算的深渊里看时，你就有掉进去的危险。[维基百科列出了比我们手指还多的计算平方根的方法。其中之一](https://en.wikipedia.org/wiki/Heron%27s_method#Babylonian_method) [CORDIC](https://en.wikipedia.org/wiki/CORDIC) 通过巧妙的位移和查找表避免了乘法运算。在这种情况下，我们的首选[切比雪夫多项式逼近](https://www.embeddedrelated.com/showarticle/152.php)，甚至没有成功。(尽管我们怀疑它会成为`gamma=1.8`或`gamma=2.2`情况下的竞争者，特别是如果像[nats.fr]那样在第一阶段结合射程缩减的话。)

那么，对于 FPGA 上的 16 位整数，`sqrt(x)`的最佳/最快近似值是什么？[nats.fr]用的是斯巴达 6，所以可以用乘法器，但是除法大概最好避免。那么任意的，可能是分数的根呢？