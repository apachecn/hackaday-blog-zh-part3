# 在 Hackaday 上开发——HaDge 又回到了绘图板

> 原文：<https://hackaday.com/2015/10/30/developed-on-hackaday-hadge-is-back-to-the-drawing-board/>

几天前，[我们写了关于](http://hackaday.com/2015/10/26/developed-on-hackaday-its-a-badge-no-its-the-hadge/)的[黑客](https://hackaday.io/project/8007-hack)——一个由【Michele Perla】基于 Atmel SAM R21 MCU 设计的原型平台。它是由 ARM Cortex-M0 MCU + IEEE 802.15.4 无线无线电捆绑在一起的新型设备之一。这是令人兴奋的，因为我们可以在 [HaDge](https://hackaday.io/project/3009-the-hackaday-badge) 硬件中装入很多功能。我们计划以后用同样的设计来驱动 HaDge。Building HACK 可以让我们把它交给软件团队，而硬件人员则负责真正的 HaDge 布局。

黑客设计已经准备好接受审查，我们四处询问以验证天线布局，这是我们不太确定的部分。我们请求 Atmel 帮助验证布局。就在那时，我们迎来了 [facepalm](https://duckduckgo.com/?t=lm&q=facepalm&iax=1&ia=images) 时刻。他们问我们——“[FCC 认证](http://library.ul.com/wp-content/uploads/sites/40/2015/02/UL_WP_Draft_FCC-Approval-of-Host-Devices-with-Integrated-Wireless-Modules_v6.pdf)怎么样？”因为我们计划至少生产几百个徽章，很明显我们不能逃避 FCC 的认证。基于 R21 的设计被排除了——获得批准的成本相当高。这意味着我们需要放弃 R21，转而使用已经通过 FCC 认证的现成无线电模块。叹气。

好消息是。从[米歇尔]投入的时间和精力来看，这是一个挫折。但除此之外，我们还可以从头开始。首先，我们决定恢复 Atmel D21 作为主控制器。这是一款相当不错的 MCU，而且有一个相当强大的工具链，很多人都很熟悉。对于无线电，我们正在考虑一些可用的选项:

*   [https://www.anaren.com/air/products/24ghz-solutions](https://www.anaren.com/air/products/24ghz-solutions)
*   [http://www.nordicsemi.com/eng/Products/2.4GHz-RF](http://www.nordicsemi.com/eng/Products/2.4GHz-RF)
*   [https://www.adafruit.com/products/2471](https://www.adafruit.com/products/2471)
*   [http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en535967](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en535967)

微芯片上的最后一个看起来很有希望。但是我们对更好更便宜的建议持开放态度，所以请提出您的意见。