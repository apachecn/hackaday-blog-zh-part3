# 刮刮乐跨越了物理和数字领域

> 原文：<https://hackaday.com/2015/12/21/scratching-vinyl-straddles-physical-and-digital-realms/>

现代 DJ 的生活很艰难。[Gergely]喜欢他的应用程序，但当他抓挠时，与应用程序配合工作的 MIDI 控制器会感觉不对，并且用于抓挠的最佳物理接口只能与他们的专用机器配合工作。[Gergely]的博客记录了他在构建一个界面以从物理转盘上驱动他的 iPad 应用程序的冒险经历。但是要注意，这里有很多，你最好的选择是从博客的开头开始(向下滚动),然后一路向上。或者让我们来引导你。

在他最早的一篇文章中，他展示了他的理想解决方案:一个解释时间码黑胶唱片并模拟标准 MIDI 控制器的 MIDI 输出的黑匣子。听起来很简单，对吧？【Gergely】[在](https://turntablecontrol.wordpress.com/2014/11/30/emulating-reloop-beatpad-to-algoriddim-djay/)上很早就让 MIDI 端工作，因为嗅探 USB 流量并模拟它相对简单。因此，现在他已经控制了 MIDI 驱动的应用程序，与现实世界交互的艰难部分开始了。

在[用时间码乙烯基做了很多](https://turntablecontrol.wordpress.com/2014/12/10/the-input-stage/)实验后，【Gergely】放弃了它，寻找一个更容易的替代品。他还[考虑使用光电鼠标](https://turntablecontrol.wordpress.com/2014/12/21/reverse-engineering-an-optical-mouse/)，但这也是一个死胡同。最后，[Gergely]决定使用 Tascam TT-M1，[，它基本上是一个光学编码器，位于唱片的顶部，](https://turntablecontrol.wordpress.com/2014/12/14/reverse-engineering-tascam-tt-m1-unit/)，这使得微控制器的工作容易得多。你可以在休息时间下面的视频中看到结果。

然后，在一个令人惊讶的值得一看的结局中(《我看见死人》)希亚马兰他[从坟墓中取出时间码乙烯基，建造了一个小型硬件翻译器，并让他最初的计划开始工作](https://turntablecontrol.wordpress.com/2015/03/04/latest-developments/)。但是我们感觉他还没有完成:他还做了一个 3D 打印的光学鼠标支架。

 [https://www.youtube.com/embed/_xLBSqPOOmI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_xLBSqPOOmI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们迫不及待地想从[Gergely]那里看到更多，也不介意看到这个项目背后的一些代码。与此同时，如果这一切让你觉得有灵感完全从零开始制作自己的 DJ 控制，[看看这个完全 DIY 的转盘项目](http://hackaday.com/2015/11/09/two-turntables-and-no-microphone/)。