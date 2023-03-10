# 利用 Stellaris/Tiva 实时时钟

> 原文：<https://hackaday.com/2017/02/19/making-use-of-stellaristiva-real-time-clock/>

如果你和我们一样，或者和[Vadim]一样，你会在壁橱里的鞋盒里藏了一些开发板。如果你比我们组织得更好，它甚至可以被称为“开发板”。(好吧，这个项目改天再说。)不管怎样，把手伸进你的盒子里拿出一个来，用起来吧。如果需要，做一些琐碎的事情，但是一个开着愚蠢信号灯的开发板比一个坐在黑暗中的开发板要好。

[Vadim]的[给我们所有人树立了一个好榜样](https://shortn0tes.blogspot.de/2017/02/stellaris-launchpad-rtc-usage-in.html)将成为自动植物浇水系统的大脑。这是一个低需求的应用，微控制器可以花大部分时间睡觉。[Vadim]的第一步是获得一个与休眠模式一起工作的实时时钟。他的博客里有工作代码。

[![royale-with-cheese-pulp-fiction-2_12-movie-clip-1994-hd-6pkq_ebhxj4mkv-shot0001](img/af1656c6376d9103757b522285a27e02.png)](https://hackaday.com/wp-content/uploads/2017/02/royale-with-cheese-pulp-fiction-2_12-movie-clip-1994-hd-6pkq_ebhxj4mkv-shot0001.jpg)

“I don’t know, I didn’t go into Burger King.”

如果你使用 Arduino，你会在 Energia 生态系统中有宾至如归的感觉。但这就像在巴黎点四分之一磅奶酪:Energia 是皇家奶酪(YouTube)——这是一点点区别。也许这就是这个练习的重点。尝试新事物总是一件好事，即使它只是最小的不同。

因此，从架子上拿走那块[未使用的开发板](http://hackaday.com/2011/02/01/what-development-board-to-use/),在不熟悉的开发环境和/或工具链中奋斗，但是记得留意可爱的小差异。当你着手下一个项目时，你熟悉的工具越多，你脑海中浮现的解决方案就越多。