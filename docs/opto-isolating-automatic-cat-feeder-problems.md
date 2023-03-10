# 光隔离自动猫喂食器问题

> 原文：<https://hackaday.com/2017/10/07/opto-isolating-automatic-cat-feeder-problems/>

当你购买现成的自动喂猫器时，你可能会期望它做它应该做的一件事。喂猫。好吧，至少只要你做好自己的工作，让它装满食物块。[[Stephen]暗自怀疑他的喂食器偶尔会偷懒，并着手证明这一理论。](https://github.com/stephen--/CatFeederAlerts)

他对调查有一些想法。一个是安装一个网络摄像头，但这被证明是不可靠的。另一个想法是记录食物碗的重量变化。这似乎是一种可能性，因为无论何时装满，读数都会发生显著变化。他选定的方法也很好——监控马达的活动，寻找漏洞。毕竟马达只有在喂食的时候才会运转。

该设计基于一个智能门/窗报警器，它比一个具有网络功能的簧片开关好不了多少。[Stephen]连接了一个光隔离器，这样当马达运行时，簧片开关被触发但不会烧坏，事件会记录在 Google Sheets 中。任何错过的食物都被一个脚本剔除，这个脚本通过电子邮件和短信提醒[斯蒂芬]他可怜的小猫饿了。

如果[斯蒂芬]曾经想要建造自己的猫喂食器，[我们](https://hackaday.com/2016/12/30/cheap-cat-feeder-enhances-sleep/) [有](https://hackaday.com/2015/05/12/super-simple-cat-feeder/) [充足的](https://hackaday.com/2012/05/06/automatic-cat-feeder-made-with-recycled-laminator-parts/)[设计](https://hackaday.com/2013/05/20/automated-cat-feeder-and-large-plastic-screws/) [用于](https://hackaday.com/2015/08/08/hack-your-cats-brain-to-hunt-for-food/) [灵感](https://hackaday.com/2016/09/01/cat-operated-cat-food-dispenser/)。