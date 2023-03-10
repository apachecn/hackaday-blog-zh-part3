# 最小可行一维乒乓

> 原文：<https://hackaday.com/2018/06/08/minimum-viable-1-d-pong/>

是什么让游戏成为游戏？比如，当我们面对一个 PONG 时，我们怎么知道我们看到的是它的一个变种呢？我们怎么知道怎么玩呢？[Bertho]试图回答这个问题，他设计了可能是有史以来最小的一维乒乓游戏。他的答案涉及到 charlieplexing LEDs，使用分压器来节省 I/O 引脚，以及几个应该可以持续很长很长时间的 AAA。

[Bertho]的最小 1-D PONG，简称 m1dp，随着游戏从“我得到了这个”到“没有人可能保持这个”的快速发展，使 ATTiny85 通过它的步伐。该状态机休眠，直到按下两个按钮中的一个，此时等待动画开始。动作从下一次按钮按下开始。

在只有五个 led 灯的情况下玩游戏也能产生一些相当激烈的动作。幸运的是，蜂鸣器是体验的一大部分。当球在运行时，它为每个 LED 发出一种声音，并发出不同的声音来确认按钮的按下。[Bertho]用 charlieplexing 节省了这么多 I/O 引脚，以至于他增加了一个绿色 LED，当可以回球时它就会亮起。如果我们在玩，我们会盯着这个 LED，而不是试图看球。我们在断点之后提供演示，所以不要让它错过你。

对于极简主义的研究来说，这里确实有很多不同的色调和动画。如果你喜欢最大列表一维 PONG，[总有 LED 条](https://hackaday.com/2012/08/22/one-dimensional-pong-is-a-great-use-for-led-strips/)。如果你更喜欢硬件令人满意的地牢爬虫，你真的需要看看[的鼻音](https://hackaday.com/2018/01/24/diy-dungeon-crawler-game-plays-on-single-led-strip/)。

 <http://www.vagrearg.org/m1dp/min1dp_vid.webm?_=1>

[http://www.vagrearg.org/m1dp/min1dp_vid.webm](http://www.vagrearg.org/m1dp/min1dp_vid.webm)

Via [ [危险原型](http://dangerousprototypes.com/blog/2018/06/05/minimalistic-1d-pong/)