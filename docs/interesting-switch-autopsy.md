# 有趣的转换尸检

> 原文：<https://hackaday.com/2016/09/03/interesting-switch-autopsy/>

我们对一些极其廉价的组件寄予了极大的信任，但有时这种信任是非常不值得的。每个电子元件都是构造精美的精密实验室仪器的日子已经一去不复返了。正如[鲁珀特·赫斯特]所展示的，即使对最大的公司来说，这也可能是一个很难学习的课程。

[Rupert]的 Nexus 5 遇到了一个众所周知的重启问题。他追踪到了手机的电源开关。它总是对地短路，即使它像预期的那样发出咔哒声。

他拆下开关，撬开脆弱的金属片外壳。里面有四个组件。底部有一个硬瘤的软膜，可能是为了给开关带来高质量的感觉。接下来是两个金属扣，它们产生咔哒声并与电路板接触，电路板是最后一个组件。

他注意到了一些奇怪的事情，拿出了他的 USB 显微镜。该公司在底部带扣上放了一滴焊料。我们认为这是因为钢与铜的接触会导致基板过早损坏，尤其是在每次开关事件中的高冲击下。

错误在于焊料滴的位置不精确。如果它完全在中间，并且很可能许多从未显示问题的手机都有它，那么问题就永远不会出现。由于它偏离了中心，每次开关事件的冲击都会慢慢地在铜和玻璃纤维上沉积薄薄的焊料层。最后，它积累到足以完全短路开关。

有趣的是，这个确切的问题出现在不同的手机制造商身上，某个地方有一家拥有杀手级销售团队的交换机公司。