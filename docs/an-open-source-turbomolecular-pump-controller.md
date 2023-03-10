# 一种开源的涡轮分子泵控制器

> 原文：<https://hackaday.com/2018/04/28/an-open-source-turbomolecular-pump-controller/>

并不是每个项目报道都以“我有这个 TURBOVAC 50 涡轮分子泵……”这样的句子开头，但也不是每个报道都来自像[Niklas Fauth]那样有一个装满好东西的实验室的人。他的泵有一个过期的控制器板，[所以他创造了一个自己的开源控制器](https://hackaday.io/project/156682-open-source-turbomolecular-pump-controller)以 STM32 为中心。有趣的是，他提到了它的潜在用途，比如“*我想在未来做更多关于溅射和离子注入的东西*”，当然这也是人之常情。

因此，鉴于可能没有多少黑客读者有涡轮分子泵，但你们中的相当一部分人会发现这个主题很有趣，这个项目是做什么的？遗憾的是，它比泵本身更普通，因为涡轮分子泵是一种高度专业化的多级涡轮，这是一种三相电机控制器，具有模拟速度反馈，来自电机两相的电压。出于这个原因，他指出这是他的悬浮滑板电机控制器软件的一个分支，[我们过去已经向你展示过它的成果](https://hackaday.com/2017/12/03/boxes-form-an-orderly-queue-behind-the-armchair/)。如果电机没有在安全时间内达到全速，没有中断计时器，但他提供了建议，如有必要，可以在[代码](https://github.com/NiklasFauth/stm32-turbotronik)中查找。

这绝不是第一个到达这些页面的涡轮分子泵，2016 年我们给你带来了一个从特斯拉涡轮机获得灵感的涡轮分子泵。