# 只有火腿才能使用的手表

> 原文：<https://hackaday.com/2017/12/19/a-watch-only-a-ham-can-use/>

我们不确定这是怎么回事。随着各种智能手表和健身追踪器的出现，我们不会对如今什么样的硬件最终被绑在手腕上感到惊讶。因此，一个带 RPN 计算器的手表并不太难。但是加个十六进制编辑器？和一个拆卸工？哦，当你在这的时候，一个 70 厘米火腿乐队的收发器？这可不是每天都能看到的。

令人难以置信的不仅是实现[特拉维斯·古斯比(Travis Goodspeed)所谓的 [GoodWatch](https://goodwatch.org/posts/introducing-the-goodwatch/) 所需的技术实力，还有导致所有这些功能都被装进卡西欧计算器手表外壳的思维过程。但是很多黑客行为更多的是关于“为什么不呢？”而不是“为什么？”，当您开始查看[Travis]选择的 CC430F6137 微控制器的特性集时，事情开始变得有意义了。该芯片内置 RF 子系统，无疑旨在实现无线传感器设计。GoodWatch20 使收发器工作在 430 MHz 频段，实现了一个简单的低功耗(QRP)信标。但这里真正的故事是在黑客[特拉维斯]用来实现这一点，如使用便利贴斑点探测液晶显示器的连接，他设法留在原来的情况下。

这里有一些真正的技巧，读起来很有趣。由于 GoodWatch 由硬币电池供电，我们认为这将是我们[硬币电池挑战大赛](https://hackaday.com/2017/11/29/coin-cell-challenge-use-coin-cell-win-prizes/)的绝佳参赛作品。

[通过[无线电/业余无线电](https://www.reddit.com/r/amateurradio/comments/7k7xyd/goodwatcha_casio_watch_modified_to_receive_and/)