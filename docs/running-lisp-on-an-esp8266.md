# 在 ESP8266 上运行 LISP

> 原文：<https://hackaday.com/2016/10/14/running-lisp-on-an-esp8266/>

LISP 是一种两极分化的语言。你要么喜欢它，要么讨厌它。但是我们会抛开个人喜好，给你带来一个好的 hack。在这种情况下[运行在 ESP8266](http://dmitryfrank.com/articles/lisp_on_mcu) 上的 LISP 环境。[Dmitry]站在“热爱它”的一边——他一直在等待编写 LISP 解释程序的借口，他在 ESP8266 中找到了一个。

[![there-is-always-a-way-2](img/49ce796b346e3c917f92ab405724ea43.png)](https://hackaday.com/wp-content/uploads/2016/10/there-is-always-a-way-2.jpg) 实际上，[Dmitry]在 JavaScript 内部运行 LISP，而 JavaScript 本身在被组装到 ESP8266 上运行之前，可能是用 C 语言编写的。(一路向下都是乌龟！)这意味着他可以搭载 JavaScript 的垃圾收集和控制台处理等等。在挑选了一个合适的小型 LISP 实现(实际上是一种 Scheme 方言，适合那些知道区别的人)之后，他开始工作。

一个周末过去了，但他让系统运行起来，连接到网络上，并让 led 灯闪烁！最后，他甚至设法为了内存的缘故进行了一些优化。非常酷，因为它利用了一个已经完整的系统，它甚至可以变得非常有用。对于几个周末的工作来说还不错！

最后，如果大量恼人的愚蠢括号是你的好时光，但 ESP8266 上可用的大量计算资源似乎有些多余，那么看看运行在 AVR 上的 [Microlisp。或者走向另一个极端，](http://hackaday.com/2016/09/13/microlisp-lisp-for-the-avr/)[在树莓派](http://hackaday.com/2015/09/23/old-lisp-languaged-used-for-new-raspberry-pi-os/)上运行 LISP 操作系统。无论你做什么，不要忘记关闭你的括号！(我们被告知这是传统的口齿不清的告别。)