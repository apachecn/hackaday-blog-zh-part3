# 本周失败:Arachno 失败 ia

> 原文：<https://hackaday.com/2016/06/23/fail-of-the-week-arachno-fail-ia/>

从名单上往下看(FCC、CE、UL 等。)我们想不出一个监管机构来测试这种故障模式。据报道，一个价值 100 万美元的灌溉系统被一只蜘蛛偷走了。还有一只小蜘蛛。

这次失败在/r/mildlyinteries 上以快速图片的形式出现，但我并不是唯一一个像飞蛾扑火一样被吸引的电子人。我们的朋友[Sprite_TM]蹦出来回答了一个关于保形涂层的问题。似乎这块板被密封在一个防水的外壳中，但显然没有被均匀地覆盖。

![fotw-spider-short-relay-diagram](img/a706598e54f44a270715ce30d85c411a.png)[Sprite _ TM]也帮助一些工程师猜测发生了什么。不难看出，电路板上的足迹看起来像一组排成一行的机械继电器。他查找了接力赛最可能的引出线。

我们在电路板上叠加了引脚，以帮助说明故障。高电压从红色走线所示的引脚进入。该引脚的两侧是低压线圈的连接，该线圈从常闭(右上角的引脚，不与任何东西连接)切换到常开引脚(具有从其引出的最宽走线)。

所以当一只蜘蛛出现时，高压针就在线圈针之间。它短路了引脚，可能一直短路到低压轨的电源。[Fugly _ Turnip](OP)分享一些关于系统的[额外细节和这个故障](https://www.reddit.com/r/mildlyinteresting/comments/4o4qes/this_little_spider_knocked_out_a_million_dollar/d49prcy)；除了这张卡，它还烧坏了控制模块。

同一帖子的另一个评论分享了两个相邻安装的电路板的不同故事，其中一个 bug 导致两个电路板之间的 1/4”空气间隙短路，并导致类似的大屠杀。你遇到过自己的蜘蛛吗？下面让我们了解一下。

* * *

《一周失败》是一个黑客专栏，它把庆祝失败作为一种学习工具。通过写下你自己的失败和[给我们发送一个故事的链接](mailto:tips@hackaday.com?Subject=[Fail of the Week])——或者发送你在互联网旅行中发现的失败报道的链接，帮助保持乐趣。