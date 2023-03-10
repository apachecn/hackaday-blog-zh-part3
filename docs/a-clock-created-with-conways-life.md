# 用康威的一生创造的时钟

> 原文：<https://hackaday.com/2017/03/11/a-clock-created-with-conways-life/>

康威的生活必须是历史上最持久的零玩家电脑游戏。自 20 世纪 70 年代以来，四种简单的细胞自动机规则已被用于创建令人惊叹的模拟。最新的是在生活中实现的[全数字时钟](http://codegolf.stackexchange.com/questions/88783/build-a-digital-clock-in-conways-game-of-life/111932#111932)。StackExchange 用户[dim]创建了此模拟，以回应来自[Joe Z]的挑战。我们不得不承认，一开始我们并不相信，但是你可以通过[导入【dim’s】要旨](https://gist.githubusercontent.com/anonymous/f3413564b1fa9c69f2bad4b0400b8090/raw/f5c77c999a8e11f0ec6ba504d383774eb3b88e5c/Conway%2520life%2520clock%2520PM%2520only)到线上 [Javascript 康威人生模拟器](https://copy.sh/life/)自己运行一下。说这令人印象深刻是一种保守的说法。我们不知道[dim]建造这座钟到底花了多长时间，但挑战从 2016 年 8 月就开始了。

[Dim]很好地描述了时钟是如何工作的。时基在顶部。下面是时钟分配和计数器。之后是计数器、锁存器和查找表。数据以滑翔机的形式昼夜不停地移动。确切地说是 P30(又名蜂后)滑翔机。把滑翔机路径想象成电路轨迹，把滑翔机本身想象成时钟脉冲，可能会让事情变得简单一些。

我们无法忽略这个设计中的所有小细节。如果放大，可以看到所有的查找表模式都被注释了，就像原理图一样。对于[迪姆]的下一个壮举，我们希望他接受[乔 Z 的] [俄罗斯方块挑战](http://codegolf.stackexchange.com/questions/11880/build-a-working-game-of-tetris-in-conways-game-of-life)！

康威的生活对黑客来说就像蜂蜜。我们已经看到它运行在我们自己的 Hackaday 徽章上。我们甚至在他们的显示器上看到了运行游戏的[时钟](http://hackaday.com/2014/01/11/extremely-slick-game-of-life-based-clock/)。有人需要实现一个时钟来运行运行这个时钟的游戏。有人同意吗？