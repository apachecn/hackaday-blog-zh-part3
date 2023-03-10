# 纸板电脑

> 原文：<https://hackaday.com/2017/01/18/the-cardboard-computer/>

每当我们说“我们都看过了”的时候，就会有一个项目让我们大吃一惊。60 岁的[Mark Nesselhaus]喜欢学习新的东西，他从来没有在门级的硬件上工作过。因此，他正在为自己建造一台 4 位计算机，仅使用二极管晶体管逻辑。他用黄铜大头钉做衬垫，在“纸板”上组装整个东西。为什么——因为他是一个节俭的人，想要利用他周围的一切。显然，他有无穷无尽的纸板、图钉和耐心。这个故事听起来很熟悉。它开始是一个简单的 4 位全加器项目，然后事情失去了控制。当他称他的万用表为“模拟 VOM”时，你就知道他是老派了！

这项工作仍在进行中，但他在过去的一年里已经做了很多。[Mark]开始模仿 Simon Inns 的[等待星期五博客](http://www.waitingforfriday.com/?p=529)中的 4 位全加器。这是 ALU，他的项目的其余部分就是围绕着它构建的。ALU 完成后，他决定继续前进，下一步构建一个 4 到 16 行的解码器——查看缩略图，看看乱糟糟的电线组成的老鼠窝。他的清单上的下一个是几个触发器——R-S 型、J-K 型和 D 型，它们作为程序计数器很有用。这时，他碰到了信号电平、定时和触发的问题。他决定给自己增加一个集成电路——一个基于 555 的时钟发生器。但是他仍然需要一些脉冲整形电路来使它持续工作。

![from right, Input, +5V, nc, gnd](img/293d92a6801d6029619f119e4407d3ca.png)

LED Driver : from left, Gnd, NC, +5V, Input

[Mark]还基于 Rory Mangles [TinyTim 项目](http://www.northdownfarm.co.uk/rory/tim/)所做的工作构建了一个有限状态机序列发生器。他完成了一些多路复用器和多路分解器的制造，看起来他可能使用了一整排 14 个墙壁开关来实现地址、输入和控制功能。对于输出显示，他用从 1 美元的圣诞灯串中回收的 led 组装了一个面板。不过，他的 LED 驱动器似乎有些问题——LED 开启时为 2mA，LED 关闭时>为 2.5mA。LED 似乎连接在 PNP 晶体管的集电极和发射极之间。加入你的评论。

这种构建似乎正在沿着我们在过去迷恋过几次的[巨型处理器](https://hackaday.com/?s=megaprocessor)的路线成形。坚持下去，[马克]！

 [https://www.youtube.com/embed/deJ7I13KFLY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/deJ7I13KFLY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

