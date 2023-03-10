# 便携式、精确、低成本、开源的空气粒子计数器

> 原文：<https://hackaday.com/2016/11/13/a-portable-accurate-low-cost-open-source-air-particle-counter/>

如果你生活在一个空气质量差的城市，你可能会意识到微粒是问题的主要原因之一。燃烧产生的小于 10μm 的微小烟尘颗粒，因此通常被称为 PM10。这些是危险的，因为它们可以在肺部深处积累，从而导致各种疾病。

有商业传感器可以检测和量化这些粒子，但它们既不便宜也不是开源的。[东润]告诉我们一个旨在改变这种情况的项目，MyPart，它被描述为一个便携式，精确，低成本，开源的空气粒子计数器。这个项目有一个 GitHub 库，还有[一系列详细介绍构建的指令](http://www.instructables.com/id/How-to-Build-a-Portable-Accurate-Low-Cost-Open-Sou/)。它来自美国加州大学柏克莱分校[混合生态实验室](http://www.hybrid-ecologies.org/)的一组成员。

一路上，他们对颗粒传感器的工作原理进行了精彩的描述。一束激光以直角穿过光电二极管，并被带到光电二极管上方的一个焦点上。空气中的任何微粒都会将光散射到光电二极管的方向上，这样光电二极管就可以探测到它们。成功的这种传感器的设计需要精心建造的完全不透光的室，以确保空气层流通过激光器和二极管。为此，他们的腔室有几层，为了内部光滑，是机械加工而不是 3D 打印的。

这些年来，我们在 Hackaday 讨论了相当多的环境传感器。[例如，去年推出的开源挥发性有机化合物(VOC)检测器](http://hackaday.com/2015/08/09/watch-those-vocs-open-source-air-quality-monitor/)，或者使用商用气体传感器的基于 Raspberry Pi 的系统[。](https://hackaday.com/2012/12/11/standalone-air-quality-monitor-based-around-raspberry-pi/)