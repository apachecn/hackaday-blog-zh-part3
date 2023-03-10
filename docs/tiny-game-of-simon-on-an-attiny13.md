# 西蒙在雅典的小游戏 13

> 原文：<https://hackaday.com/2016/12/31/tiny-game-of-simon-on-an-attiny13/>

只有 1 kB 闪存和(五个或)六个免费 GPIOs 的芯片能玩多少游戏？嗯，你可以让它[玩经典的记忆游戏，西蒙](https://hackaday.io/project/18952-simon-game-with-attiny13)。[Vojtak]正在为 [1 kB 挑战赛](http://hackaday.com/2016/11/21/step-up-to-the-1-kb-challenge/)提交这个项目，但看起来它已经被用于向青少年教授简单的微控制器，所以代码实际上很容易阅读，但充满了美好的特性。

[![3924691481641919444](img/d78214e133881e56885832fa68c665c9.png)](https://hackaday.com/wp-content/uploads/2016/12/3924691481641919444.png) 巧妙的技巧包括在同一个引脚上共享按钮感应和 LED 驱动，这是在这么小的芯片上让一切工作所必需的。一个简单的线性同余伪随机序列提供了变化，它由慢时钟/快时钟时序抖动播种，因此您可能不会看到相同的序列两次。(这不是[有史以来最好的随机数发生器](http://hackaday.com/2014/12/19/nist-randomness-beacon/)，但也可以。)如果这还不够，高分(以及游戏的随机种子)会被保存到 EEPROM 中，这样你就可以向你的朋友炫耀或重现你以前的辉煌时刻。

电路板也很容易焊接在一起。这是一个奇妙的初学者项目，代码中的细节每个人都可以从中学习。这是一个很棒的游戏，也是一个很好的演示，展示了你可以用价值一美元的部件和 1 kB 的代码做什么。

 [https://www.youtube.com/embed/BJ-PwkigoB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BJ-PwkigoB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



![1kb-thumb](img/c25ee8590ee29cc76bd2ada5afb927dd.png)

如果你心中有一个很酷的项目，还有足够的时间[参加 1 kB 挑战](https://hackaday.io/contest/18215-the-1kb-challenge)！截止日期是 1 月 5 日！