# 使用 SDR 的射电天文学级联 lna 和滤波器

> 原文：<https://hackaday.com/2017/08/02/cascade-lnas-and-filters-for-radioastronomy-with-an-sdr/>

它可能不是拥有所有点击率和最佳下午驾驶节目的电台，但 1420.4058 MHz 是宇宙中最受欢迎的频率。那是氢的电磁光谱线，它永远在空气中。但是，研究 H 线是一项重要的任务，除非你知道如何级联低噪声放大器和滤波器，以使用 SDR 进行射电天文学。

因为宇宙大部分是由氢构成的，所以 H 线发射很丰富，它们的分布可以告诉我们很多星系的结构。21 厘米的发射线如此有特点，如此普遍，以至于我们在先锋探测器上的铭牌上以及在回放旅行者号记录的说明中使用它作为测量单位。但是在地球上收听 21 厘米需要一个特殊的设置，这在[一篇关于这个主题的详细论文](https://www.dropbox.com/s/g5lh24xtmmn5gir/Radioastronomy%20Hydrogen%20line%20frontend%20on%20a%20budget.pdf?dl=0)中有所描述。[Adam]分析了他销售的 lna 和滤波器的多种配置，以确定 21 厘米工作的最佳前端。他的分析是 lna 的良好入门，解释了为什么前端器件需要尽可能靠近天线。使用他的 lna 和滤波器以及 SDR 加密狗，一个合理的 21 厘米钻机大约只需 200 美元左右，不包括天线。他承诺会发表一篇关于自制 21 厘米天线的后续论文；我们会期待的。

不喜欢球体的音乐，而更喜欢听我们自己的飞船？然后仔细阅读[深空网络](http://hackaday.com/2017/07/21/serious-dx-the-deep-space-network/)以及如何窥探。