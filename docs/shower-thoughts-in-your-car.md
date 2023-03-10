# 在你的车里沐浴思绪

> 原文：<https://hackaday.com/2016/05/24/shower-thoughts-in-your-car/>

淋浴思想的子编辑提供了从深奥到平凡的智慧。例如:“每次你剪一个角，你就会多剪两个。”显然，[哈林]对 subreddit 有点上瘾。他一直在嗅他的 2012 现代 Genesis 上的 CAN 总线，并决定在他的收音机屏幕上显示顶级淋浴想法。

为了实现这一壮举，他同时使用了树莓派和 Arduino。两款器件都有一个 MCP2515 与两条不同的 CAN 总线接口(一条用于 LCD 显示，另一条用于承载大量流量的控制消息)。

该代码可在 [GitHub](https://github.com/hdemel/Genesis-Canbus) 上获得。例如，要让消息滚动，还有很多工作要做。[哈林]有其他关于嗅探巴士的帖子，像[这个](http://solderandflux.com/2016/04/27/canbus-sniffing-the-2012-hyundai-genesis-coupe/)。

我们已经[涵盖了 CAN 总线](http://hackaday.com/2012/04/17/tinkering-with-odb-ii-and-the-can-bus/)相当多，包括一些[非汽车用途](http://hackaday.com/2012/03/07/can-bus-for-home-automation/)。我们甚至看到了用于铁路模型的 [CAN 总线](http://hackaday.com/2012/06/17/router-controlling-choo-choos-over-the-can-bus/)。