# 公民科学家:福里斯特·米姆斯

> 原文：<https://hackaday.com/2015/10/13/citizenscience/>

在现代公民科学家的概念之前，是独立科学家的早期理想。学术界之外但参与其中的科学家。如今，公民科学家通常被视为科学过程中有价值的助手，帮助收集和处理大量数据，否则这些数据将难以处理。

然而在过去，独立科学家的作用要重要得多。伽利略、开普勒、达尔文和胡克在他们职业生涯的不同阶段都是靠自己资助的。最近，独立科学家彼得·米切尔因其对细胞生物化学的基础性研究和化学渗透假说的发展获得了 1978 年诺贝尔化学奖。

可悲的是，由非研究机构资助的科学家发表的同行评议的科学论文现在少之又少。在这个简短的系列中，我们希望强调这些孤独的研究人员的努力，并特别提到他们在科学探索中不得不在预算内拼凑的工具(如果你认识一位你认为我们应该介绍的独立研究人员，请在下面评论！).

在黑客圈里，福里斯特·米姆斯最出名的可能是他的一系列电子书籍[和不可伪造的](http://www.forrestmims.org/biography.html)[雅达利朋克游戏机](http://hackaday.com/2015/09/17/the-ubiquitous-atari-punk-console/)。但是他作为独立研究者通过一系列深思熟虑的[科学文章](http://www.forrestmims.org/publications.html)与科学界接触的能力让我们在这里感兴趣。由于缺乏正规的科学训练，他的贡献显得更加重要。

## 作为光传感器的 led

福里斯特的主要贡献在于光的环境测量。特别是臭氧和其他基于太阳辐照度(阳光)的测量。他的工作从一个简单的技巧开始，使用发光二极管，不是为了照明，而是为了感知光线。福里斯特的实验[始于高中](https://www.osapublishing.org/opn/abstract.cfm?id=185687)，在那里“观察到电磁扬声器可以兼作麦克风，我想知道半导体光探测器是否也可以发光”。福里斯特的实验继续进行，他发现他确实可以从光电二极管和光电池产生少量的光。当 led 在 20 世纪 70 年代变得广泛可用时，他发现这些也可以用作光探测器。

[![led-5-alt](img/7fe9464a80b7a9378dda9e6a7c64979a.png)](https://hackaday.com/wp-content/uploads/2015/10/led-5-alt.jpg)

The LED Transimpedance amplifier circuit (see [his Make article](http://makezine.com/projects/make-36-boards/how-to-use-leds-to-detect-light/) for details)

LED 光传感器[电路相当简单](http://makezine.com/projects/make-36-boards/how-to-use-leds-to-detect-light/)，只需将一个光电二极管换成运算放大器跨阻放大器中的一个 LED，就可以测量 LED 产生的电流(我[本周亲自尝试了这个](http://41j.com/blog/2015/10/leds-as-light-sensors/)，可以证明这是一个简单而有趣的实验)。

与光电二极管相比，LED 光传感器有许多优点。led 不仅通常更便宜，而且具有更好的波长选择性。这使得特定波段成为目标，从而提高灵敏度。LED 传感器也具有难以置信的稳定性。虽然在某些应用中，基于滤波光电二极管的检测器可能需要每年校准，但 Forrest 二十年来一直使用同一种基于 LED 的检测器，漂移极小。

 [https://www.youtube.com/embed/XpZ_-ufadao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XpZ_-ufadao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



福里斯特用这些探测器建造了各种各样的[仪器](http://onlinelibrary.wiley.com/doi/10.1029/2001JD900103/pdf)，其中有一个臭氧测量装置。20 多年来，每天中午，福里斯特都会在他位于德克萨斯州南部的家中进行测量。他的设备如此精确，他的工作如此一致，以至于他能够确定美国宇航局 Nimbus-7 卫星上的臭氧总量绘图光谱仪所做测量的漂移。NASA 最终承认了这个错误，这个错误被[发表在了备受瞩目的科学杂志 *Nature* 上](http://www.nature.com/nature/journal/v361/n6412/abs/361505a0.html)。

## 真菌火灾

[![sarahmims](img/c8c80ae7d9f0b35bd0f020b0fe14e882.png)](https://hackaday.com/wp-content/uploads/2015/10/sarahmims.jpg)

Sarah using a kite to collect spores transported by a forest fire.

福里斯特也鼓励其他家庭成员发表他们的发现。他的女儿莎拉和福里斯特一起发表了一篇关于真菌孢子的文章，真菌孢子会被森林大火传播很远。Sarah 的工作作为一个科学展览项目而闻名，该项目导致了一份科学出版物。真正使这项工作与众不同的是出版物，制作出版物和与科学界接触所需的精确度和努力令人印象深刻。

独立的科学研究可能是个人黑客从事科学进步的一个很好的方式。虽然独立科学家可能缺乏资金，但他们有自由承担他们认为重要和有趣的项目，而不必追逐最新的资金热潮或增量出版物。记住[“生活是一个科学展览项目！”](http://www.theamphour.com/171-an-interview-with-forrest-mims-snell-solisequious-scientist/)。