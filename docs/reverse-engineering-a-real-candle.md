# 对真正的蜡烛进行逆向工程

> 原文：<https://hackaday.com/2016/01/06/reverse-engineering-a-real-candle/>

【cpldcpu】就是[离不开蜡烛的奥秘](https://cpldcpu.wordpress.com/2016/01/05/reverse-engineering-a-real-candle/)。在之前，我们已经报道过他对蜡烛闪烁发光二极管[的](http://hackaday.com/2014/03/02/reverse-engineering-candle-flicker-leds-again/)[探索](https://cpldcpu.wordpress.com/2013/12/08/hacking-a-candleflicker-led/)，但是这次他把他的传感器放在了真实的东西上。[cpldcpu]将一个光电二极管连接到他的示波器上，对准蜡烛火焰，记录结果。

第一个有趣的观察是蜡烛慢慢地改变亮度，不管它是否被交互作用。接下来，他测量了火焰被小股气流扰动时的效果。这产生了一种明亮的闪烁，在返回稳态之前以 5Hz 的频率振荡，正如黑客新闻评论 中提到的【冥河声波】[，这是火焰探测器中使用的一种已知现象。整洁！甚至还有一个等式:](https://news.ycombinator.com/item?id=10852383)

> 在正常重力条件下，火焰具有明确的振荡频率，该频率与燃烧器直径 D 的平方根成反比，并且可以很好地近似为 f 1.5/D，其中 D 以米为单位给出。

[cpldcpu]然后将他的测量结果汇编成一系列图表，最终形成一个动画 gif，比较蜡烛的稳态、真实蜡烛的闪烁和他从蜡烛 flickr LED 记录的闪烁。赝品和真品的差别之大令人吃惊。你可以在[他的 github](https://github.com/cpldcpu/RealCandle) 上看他的度量和代码。

【via *[黑客新闻](https://news.ycombinator.com/item?id=10851743)*