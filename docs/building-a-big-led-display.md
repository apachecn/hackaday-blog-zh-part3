# 在一个大的 LED 显示屏上加倍

> 原文：<https://hackaday.com/2015/10/04/building-a-big-led-display/>

去年在 2014 年 NC 制造商大会上，Manical Labs 带来了一个大型 LED 显示屏。闪烁的 led 和像素动画总是受欢迎的，但在 24 英寸见方的情况下，这种构建令人印象深刻，但不够令人印象深刻。今年，Manacal 实验室的[Adam]想要更大的规模。*比*大得多。这个建筑被称为巨像，占地两平方米，有 1250 个独立的 led，[这个 LED 显示屏是一个巨大的建筑](http://maniacallabs.com/2015/09/22/building-the-colossus-led-display/)。

当建造一个大的 LED 显示屏时，大量的规划会带来回报。这个项目的支柱是一张 3/8″的胶合板，被拆成 1 米乘 2 米的尺寸。1250 个半英寸的洞是在四五个漫长而乏味的晚上钻出来的。led 安装在大约一千个孔中，泡沫芯板网格包裹着每个单独的 LED。

大型 led 阵列的最大问题之一是其庞大的规模。如果一个 LED 像素消耗 60mA，那么 1250 个像素意味着消耗 75 安培。这种电流会熔化大多数电线，所以电力是通过定制的铜母线输送的。以合理的刷新率驱动该显示器是另一个重要的考虑因素；WS2812 灯在一根电线上有 800kHz 的信号，对于一个巨大的显示器来说太慢了。除了 2812，Adam 还配备了时钟频率为 30MHz 的 LPD8806 LEDs。这是由两个全像素控制的[，有效地使这两个显示器作为一个。所有这些都集中在一个非常大的 LED 显示屏上。你可以看看下面的视频。](http://maniacallabs.com/AllPixel/)

 [https://www.youtube.com/embed/6qzRQ0Hsj3Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6qzRQ0Hsj3Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

