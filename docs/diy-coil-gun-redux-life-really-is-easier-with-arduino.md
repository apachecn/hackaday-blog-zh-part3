# DIY 线圈枪 Redux:有了 Arduino，生活真的更简单了

> 原文：<https://hackaday.com/2016/08/22/diy-coil-gun-redux-life-really-is-easier-with-arduino/>

许多黑客项目评论中常见的抱怨是:他们为什么要使用微控制器？很容易马后炮别人的设计，但很少看到运放回来，并实际证明一个微控制器是最好的选择。因此，当[GreatScott] [用分立逻辑](https://www.youtube.com/watch?v=lzXMImK_wyM)重建他最近的 DIY 线圈枪时，我们只需要把话传出去。

你会从[原始版本](http://hackaday.com/2016/08/19/coil-gun-for-newbies-learning-electromagnetic-propulsion/)中回忆起【GreatScott】并没有试图制造一种砖墙爆破电磁步枪。他的建造更多的是探索概念和为一个小线圈枪设计一个可行的控制机制，因此他选择了一个 Arduino 来快速原型化他的控制电路。但当他接受设计选择的任务时，他接受了挑战，设计了一个使用分立 NAND 和 NOR 门、一些 RS 锁存器和几个比较器的控制器。基本的控制电路很简单，但对安全来说太简单了——一枚弹丸卡在枪管里可能会让线圈无限通电，导致损坏。Arduino 草图中需要一行代码来修复的问题需要一个额外的比较器级和一个 RC 网络来构建一个定时器，以自动断开线圈。最终，试验电路板完成了工作，但实现它需要两倍于 Arduino 的空间，而且没有任何灵活性。

并不是每个项目都配有 Arduino，有时很明显，构建者要么走了捷径，要么使用了他或她书中唯一的技巧。向[GreatScott]脱帽致敬，因为他不仅有勇气证明自己的设计，还证明了他拥有实现这一设计的独立逻辑能力。

 [https://www.youtube.com/embed/lzXMImK_wyM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lzXMImK_wyM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

