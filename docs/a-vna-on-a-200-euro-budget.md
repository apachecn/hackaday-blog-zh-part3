# 200 欧元预算的 VNA

> 原文：<https://hackaday.com/2016/08/13/a-vna-on-a-200-euro-budget/>

如果你问一个经常与 RF 打交道的人，他没有足够的运气为一个财大气粗的商业实体工作，他们想要的测试仪器是什么，他们的回答很可能会提到矢量网络分析仪。VNA 是一种测量 RF 电路 S 参数的仪器，作为一名电子工程专业的学生，在这些讲座中了解谁的数学知识对我们中的一些人来说是一种痛苦的记忆。

你的 RF 工程师调查对象的工作台上还没有 VNA 的原因很简单。vna 贵得惊人。二手的要几千块，新的需要诺克斯堡的钥匙。然而，所有这一切对[Henrik Forstén]来说都不是障碍，[他用 200 欧元的低得惊人的预算为自己建造了一个 30MHz 到 6 GHz 的 VNA。](http://hforsten.com/cheap-homemade-30-mhz-6-ghz-vector-network-analyzer.html)

[![The operation of a VNA](img/6a0659b6dd8ca160862466301c9f16da.png)](https://hackaday.com/wp-content/uploads/2016/08/xvna_4receiver-pagespeed-ic-z8kp5e1eof1.png)

The operation of a VNA

理论上，VNA 的操作非常简单。已知功率水平的 RF 通过被测器件进入负载，利用一组定向耦合器在其输入和输出端对正向和反向 RF 进行采样。四个耦合器中的每一个都馈送相当于一个 SDR 的量，由此产生的样本由计算机处理。他的文章包含了电路每一部分的详细介绍，是关于 VNA 操作的有趣的初级读本，

[Henrik]承认他的 VNA 不像它的商业表亲一样准确，但对于他的小预算，他的工作质量是显而易见的，因为它是一个功能性的 VNA。他可以组装一批这样的产品，即使考虑到他的定价，他也会找到一批愿意购买的人。

【亨里克】的作品[在](http://hackaday.com/?s=hforsten.com)之前已经在这些页面上出现过好几次，每次他都传递了一些特别的东西。我们见过他的[雷达系统](http://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/)，国产[喇叭天线](http://hackaday.com/2015/03/22/building-a-horn-antenna-for-radar/)，以及一台制作非常精良的 [ARM 单板电脑](http://hackaday.com/2014/07/11/an-amazing-diy-single-board-arm-computer-with-bga/)。这家伙值得关注。

谢谢[工程师]的提示。