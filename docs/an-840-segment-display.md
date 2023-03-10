# 840°分段显示器

> 原文：<https://hackaday.com/2017/02/17/an-840-segment-display/>

不久前，[limpfish]从易贝的一个卖家那里买了一些四位数的七段显示器。一两个月后，30 台显示器出现在[limpfish]的邮箱里。[limpfish]决定用这些七段显示器做一些非常酷的事情，而不是使用他认为他订购的一两个显示器。他同时控制了他们所有人。

[limpfish]控制大量 LED 的常用方法是 MAX7219 LED 驱动器。这种芯片可以很容易地——也很便宜地——控制八个共阴极七段显示器。然而，这个计划有一个问题:从易贝接收的 led 是公共阳极。这实际上不是问题，因为通过一点努力和更多的思考[limpfish] [让这些显示器与 MAX7219 驱动芯片一起工作](http://www.plingboot.com/2017/01/max7219-and-common-anode-displays/)。

有了芯片，[limpfish]为 MAX7219 和两个公共阳极 4×7 分段显示器设计了一个小型分线板。这些显示器可以用菊花链连接起来，将它们连接在一起会产生一种非常奇怪但非常酷的视觉效果。

[limpfish]将此显示视为位图显示，这意味着现在是演示时间。您可以在下面的视频中查看在这款 840 段显示器上播放的 1337 01d skool 演示。

 [https://www.youtube.com/embed/heHaCssSs2Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/heHaCssSs2Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

