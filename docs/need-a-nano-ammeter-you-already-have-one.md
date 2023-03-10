# 需要纳米安培计吗？你已经有一个了！

> 原文：<https://hackaday.com/2016/02/01/need-a-nano-ammeter-you-already-have-one/>

【Dannyelectronics】有时需要测量微小电流。非常小，就像通过电容器的漏电流。他建立了一些设置来进行测量，但他也知道当他没有定制的设备时，他有时会想要读取读数。所以他决定看看他能用一个普通的数字仪表做些什么。

![dmm-nano-ammeter](img/f417d18cc1a7cacd3bda9ef38fbfa846.png)如你所料，普通数字仪表的电流量程通常无法测量纳安或皮安。[丹尼]的方法是不使用电流表。相反，他测量电表输入阻抗上的电压(通常很高，如 1 兆欧)。如果您知道电表的输入特性(或者可以根据已知源进行校准)，您可以将电压转换为电流。

例如，在 Fluke 115 米上，[Danny]发现他可以读取高达 60nA 的电流，分辨率为 0.01 na。Viktor 81D 可以解析到 2.5pA，这确实是一个微小的电流。

我们之前已经讨论过[读取小电流](http://hackaday.com/2015/08/26/data-logging-in-the-picoampere-range/)所涉及的困难。如果你不喜欢微弱的电流，也许你会试着用 3 KA 给一部 [iPhone 充电。](http://hackaday.com/2016/01/11/using-over-3000a-to-rapidly-charge-an-iphone/)