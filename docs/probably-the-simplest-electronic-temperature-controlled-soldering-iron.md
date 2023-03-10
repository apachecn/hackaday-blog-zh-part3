# 可能是最简单的电子温控烙铁

> 原文：<https://hackaday.com/2016/11/04/probably-the-simplest-electronic-temperature-controlled-soldering-iron/>

我们都习惯了温控烙铁，我们大多数人都会有一个这样或那样的烙铁作为我们的焊接工具。在许多情况下，我们的熨斗将由微处理器控制，配有热电偶、液晶显示器和其他技术魔法，从而成为完美的焊接工具。

所有这些技术都令人印象深刻，但是如何简单地制造温控熨斗呢？如果你是老一辈的人，你可能会指出带有双金属或磁性温度调节的熨斗，所以让我们重新表述一下这个问题。一个*电子*温控烙铁能做多简单？[Bestonic lab]可能会有答案，因为他的[在 YouTube 上发布了一个视频](https://www.youtube.com/watch?v=FAfb948tZgU)，展示了一个极其简单的温控熨斗。这不是最优雅的解决方案，但它完成了要求它完成的工作，而且只需要很少的零件。

他从一个多余的保险丝座中取出一个陶瓷外壳，并将其安装在一个金属框架上，制成一个基本的烙铁座，他的未调节烙铁的尖端可以插入其中。他在陶瓷上安装了一个热敏电阻，它位于 MOSFET 的栅极偏置电路中。MOSFET 反过来操作继电器，为熨斗提供主电源。

当熨斗将陶瓷加热到热敏电阻改变 MOSFET 和继电器状态的点时，温度调节开始，在该点(熨斗断电)它冷却，直到 MOSFET 再次翻转并重新开始该过程。你可能已经发现了一个缺陷，因为它需要熨斗在支架中才能工作，尽管我们怀疑在实践中，只要熨斗回到接头之间的支架中，陶瓷的热惯性就足以合理地保持调节。没有人声称这种温控熨斗与其昂贵的商业同类产品不相上下，相反，它代表了一种非常简洁的黑客技术，可以用很少的组件变出一种有用的工具。我们喜欢这样。看看休息下面的完整视频。

 [https://www.youtube.com/embed/FAfb948tZgU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FAfb948tZgU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在 Hackaday 之前，我们已经处理了许多温控烙铁项目，包括这种[使用 Weller RT tips](http://hackaday.com/2016/05/07/a-cheaper-soldering-solution/) 的廉价方式，无需支付整个焊接站的费用，由工业 PID 控制器控制的烙铁[，以及由 PIC](http://hackaday.com/2015/04/28/adding-pid-control-to-a-non-adjustable-iron/) 供电的[烙铁。然而，这种熨斗将温度控制的简单性提升到了一个新的水平。](http://hackaday.com/2010/05/19/solder-station-hack-adds-temperature-control/)