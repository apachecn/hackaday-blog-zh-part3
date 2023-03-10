# 被动，但并非无害

> 原文：<https://hackaday.com/2015/10/12/passive-but-not-innocuous/>

Maxim Integrated 最近发布了一系列应用笔记，记录了即使是最简单的“无源”器件也比你想象的要复杂得多。没有什么是安全的:[电容](https://www.maximintegrated.com/en/app-notes/index.mvp/id/5663)、[电阻](https://www.maximintegrated.com/en/app-notes/index.mvp/id/5686)，甚至[印刷电路板](https://www.maximintegrated.com/en/app-notes/index.mvp/id/5800)都可能以非理想的方式运行，如果你没有意识到它们，这可能会在回流炉中咬你一口。

你可能已经知道，电容器有一个[等效串联电阻](https://en.wikipedia.org/wiki/Equivalent_series_resistance)来限制它们放电的速度，还有一个等效电感来模拟较高频率下的理想行为偏差。但是你知道吗，陶瓷电容器也可以像电压源一样工作，在物理压力下以压电方式[工作](https://en.wikipedia.org/wiki/Piezoelectricity)？

对于电阻，你还必须考虑温度依赖性，以及电容显示的压电和电感特性。更糟糕的是，电阻器可以在更高的电压下显示可变电阻，实际上会产生少量随机噪声:[约翰逊噪声](https://en.wikipedia.org/wiki/Thermal_noise)这取决于电阻值。

最后，本系列的第三篇文章讨论 PCB，总结了许多需要注意的潜在制造缺陷，并讨论了实际玻璃纤维层本身可能引入电路的寄生电容、漏电流和频率相关性。

如果你有一种似曾相识的感觉，[2013 年在《电子设计》杂志上发表了相同系列的文章](http://electronicdesign.com/power/passive-components-aren-t-really-so-passive-part-1-capacitors)，但它们足够好，我们希望你不要介意再次重复。如果你已经在和[争论他们所谓的“被动”](https://www.maximintegrated.com/en/app-notes/index.mvp/id/5800#sidebar)到底是什么意思，我们能感受到你的痛苦:他们实际上是在谈论[寄生效应](https://en.wikipedia.org/wiki/Parasitic_element_%28electrical_networks%29)，但是我们也不去管它。我们今天有一种奉献的心情。

[via [危险原型](http://dangerousprototypes.com/2015/10/11/app-note-passives-arent-really-so-passive-pcb/)