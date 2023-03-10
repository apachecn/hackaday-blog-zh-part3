# 爸爸喜欢曼巴蛇:滑行机器人是可重构的

> 原文：<https://hackaday.com/2017/04/25/papa-loves-mamba-slithering-robot-is-reconfigurable/>

考虑到进化是有道理的，但是大自然想出了很多不同的方法来做事情。考虑搬家。陆地动物用四只脚或两只脚行走，有些跳跃，有些利用蠕动或其他方式滑行。然而奇怪的是，大自然母亲从未发明轮子(尽管珍珠母蛾的毛虫会将其整个身体形成一个环，并从攻击者身边滚开)。另一方面，人类开发的机器人通常使用轮子。即使是坦克履带也有轮子。最新的机器人仍然使用轮子，但它模仿了一条蛇的滑行动作，他称之为[伊利湖曼巴](http://www.instructables.com/id/Snake-Robot-1/)。

关于机器人最有趣的事情是它可以重新配置和以几种不同的方式移动。像毛毛虫一样，它甚至可以像大毒蛇一样形成轮子并滚动。你可以在视频的最后看到，在下面。

基本配置滑动并使用 12 段，每段包含一个伺服电机。[Joe]用遥控钥匙驱动蛇，尽管它也能自己移动。大脑是——还有什么——一个 Arduino。在某些配置中，蛇携带自己的大脑和能量。在其他情况下，当蛇变成轮子时，有一个看起来很吓人的线束是必要的，因为它在那个配置中没有多余的空间。

真正的蛇有不同的移动方式，伊利湖曼巴蛇也是如此。在滑行配置中，被动轮将正弦或余弦波运动转换成线性运动。[乔]解释运动背后的数学。如果你卸下被动轮，蛇可以像小虫一样移动。在这种模式下转向很复杂，因为它只能前进或后退，没有任何变化。这些段可以重新配置以将驱动轮置于运行状态，从而引入所需的横向运动。

真正的蛇可以结合这两种运动来“侧风”，曼巴蛇也可以做到这一点。这确实需要重新配置段，并且用正弦波驱动一些段，用余弦波驱动其他段。

这不是我们第一次看到[大毒蛇的把戏](https://hackaday.com/2016/07/20/ourobot-what-happens-when-a-snake-bot-swallows-its-own-tail/)。如果你认为机器蛇不可能有用，[再想想](https://hackaday.com/2012/05/12/pipe-crawling-snake-robot-is-a-masterpiece-of-a-senior-project/)。当然，吸引我们眼球的模块化机器人是 [Dtto，它在去年的黑客日竞赛中获得了大奖](http://hackaday.com/2016/11/05/dtto-explorer-modular-robot-wins-2016-hackaday-prize/)。

 [https://www.youtube.com/embed/3YH25vspiJo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3YH25vspiJo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

