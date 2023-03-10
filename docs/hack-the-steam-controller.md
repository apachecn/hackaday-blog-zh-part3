# 黑掉蒸汽控制器？

> 原文：<https://hackaday.com/2015/11/02/hack-the-steam-controller/>

[willrandship]从 Reddit [发来一个对话，讨论 Steam 控制器](https://www.reddit.com/r/SteamControllerMods/comments/3p6d26/some_details_on_the_chips_in_the_controller_and/)内部的编程端口及其被黑客攻击的可能性。从帖子和图片来看，似乎无线电/SoC 和 MCU 可以在板上编程，或者至少它们都有 JTAG 接头。JTAG 接头是电路板上的“标签连接”焊盘形式，因此需要专用电缆或将一些硬件临时焊接到电路板上。

从图片中，我们可以看到一款恩智浦 LPC11U37F ARM Cortex-M0 和一款 Nordic nRF51822 ARM Cortex-M0 SoC，集成了低功耗蓝牙技术。目前在野外只有有限数量的 Steam 控制器，所以到目前为止，我们并不指望能破解它们。有一个 [Steam Controller hackaday.io 项目](https://hackaday.io/project/8296-controlsteam)刚刚开始，面向任何愿意为 Steam Controller hacking 做出贡献的人。

 [![Image by [Coloredcontrollers] via Reddit](img/2fe030f11f37fbc8b2461765da5350c4.png "parts")](https://hackaday.com/2015/11/02/hack-the-steam-controller/l1bwo2n/) Image by [Coloredcontrollers] via Reddit [![Image by [willrandship] via Reddit](img/ac4cf002283b9178bc9794009e20b7a2.png "radio")](https://hackaday.com/2015/11/02/hack-the-steam-controller/radio-28/) Image by [willrandship] via Reddit [![Image by [willrandship] via Reddit](img/b368b0076bdf57d52a52d6d0ffdd464c.png "tag_header_valve_logo")](https://hackaday.com/2015/11/02/hack-the-steam-controller/tag_header_valve_logo/) Image by [willrandship] via Reddit [![Image by [willrandship] via Reddit](img/c8888137963568642b8c78b61d6afc17.png "back")](https://hackaday.com/2015/11/02/hack-the-steam-controller/back-9/) Image by [willrandship] via Reddit

该控制器可在 Steam 网站上以 49.99 美元的价格[预购，但唉，这只是预购，我们今天不能玩它。半好消息是，如果你今天愿意](http://store.steampowered.com/app/353370/)[为一个汉堡买单的话，圣诞节前还是有可能吃到的。](https://en.wikipedia.org/wiki/J._Wellington_Wimpy)

如果你错过了，我们在 2013 年报道了 [Steam 关于控制器是开放和可攻击的](http://hackaday.com/2013/10/01/steam-controller-open-and-hackable/)的声明。不久前，我们[还讨论了 JTAT 的“标签连接器”](http://hackaday.com/2014/04/27/a-small-replacement-for-large-programming-headers/)。