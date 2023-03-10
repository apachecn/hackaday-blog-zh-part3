# 俄罗斯黑客倍增升压转换器的价值

> 原文：<https://hackaday.com/2016/09/04/russian-hacker-multiplies-value-of-boost-converter/>

我们对锂离子电池又爱又恨。他们把所有的能量都装在一个又小又轻的包里。但对于运行 3.3 V 设备来说，它们很笨重。当它们以 4.2 V 充满电时，需要降低一点，但在充电结束时，需要升高 3.0 V 左右。

简单的升压或降压转换器无法同时完成这两项工作，尽管你可能会被诱惑，因为它们可以在网上以极低的价格购买。所以[Kirich] [将廉价的升压转换器改造成更强大的 SEPIC 拓扑结构](http://mysku.ru/blog/aliexpress/36199.html)，其售价几乎是前者的 10 倍。(谷歌翻译版[此处](https://translate.google.com/translate?depth=1&nv=1&rurl=translate.google.com&sl=auto&tl=en&u=http://mysku.ru/blog/aliexpress/36199.html)。)底线？稍加脱焊，在这里切割一条走线，在那里增加一个电感，[Kirich]拥有一个非常强大的电路，当输入在 1 V 至 5 V 之间摆动时，它可以保持恒定的 3.3 V 输出。

[![95aa17](img/de367757053842cd1cbf46d3b9dc3389.png)](https://hackaday.com/wp-content/uploads/2016/09/95aa17.jpg) 如果你对 SEPIC 电力变换器不熟悉，请通读一下 [Maxim 的白皮书](https://www.maximintegrated.com/en/app-notes/index.mvp/id/1051)。基本上，它是一个升压转换器，中间有一个电容，让输出电压降至输入电压以下。一个额外的电感将该电容的输出端保持在地电位(平均)。

如果你想要更多的细节，[基里希]不会让人失望。他在两种不同型号的升压转换器上以多种配置测试了他的修改。正如你所料，电源电路、布局和走线长度很重要，[Kirich]做了很好的笔记。对于节俭的黑客或任何对升压/降压转换器感兴趣的人来说，这是一本很好的读物。

说到升压/降压电路，我们为您提供了更多链接。来自 Sparkfun 的[Pete Dokter]的这个视频价值 15 分钟，如果你想亲自动手建造这样的电路，[这个基于 ATtiny 的升压转换器](https://hackaday.com/2014/12/07/an-attiny-boost-converter/)电路玩起来很有趣。

感谢[kirillre4]的伟大提示！