# 逆向工程调试线

> 原文：<https://hackaday.com/2016/04/07/reverse-engineering-debugwire/>

你遇到过这种情况吗？你开始一个逆向工程项目，开始钻研，然后被难住了。然后你在网上寻求帮助，偶然发现某人已经做了你正在尝试做的事情？

[Geekabit]给我们写了这个悲惨故事的一个版本。在他的案例中，要逆转的协议是 Atmel 的 debugWire 协议，用于在低引脚数的器件上进行调试。有很多网站声称这是“秘密”或什么的，但它实际上看起来只是记录很差。无论如何，[RikusW]似乎早在 2011 年就捕捉到了所有的信号。干得好！

[geekabit]的故事中最精彩的部分是，他自己*在 debug wire 上创建了[维基百科页面](https://en.wikipedia.org/wiki/DebugWIRE)*，以激励在逆向工程协议上的合作，有人参与了[RiskusW]的工作。过了一会儿，当[geekabit]再次发现这个问题时，他做了一些网络调查，发现问题已经解决了——就在他开始的页面上。

也许这终究不是一个悲哀的故事，而是一个无意合作的故事。无论如何，它提醒我们，如果你对目的地的兴趣超过了探索之旅，那么事先做些研究也无妨。现在我们都知道了 debugWire 协议的底层细节。有人写了一个司机吗？

感谢[geekabit]的提示和故事！图片来自 ATmega32-AVR，其中[很好地解释了如何在 debugWire 模式下使用 Dragon](http://atmega32-avr.com/avr-dragon-manual-user-guide-in-pdf/)。