# 辐射 4 有逻辑门，功能齐全

> 原文：<https://hackaday.com/2016/06/22/fallout-4-gets-logic-gates-is-functionally-complete/>

[![Fallout logic. This is literally called Fallout logic. This is far more confusing than it should be.](img/b32e1b4d787889fedc07f5bbd427cbd4.png)](https://hackaday.com/wp-content/uploads/2016/06/fallout-logic.png)

Fallout logic. This is literally called Fallout logic. This is far more confusing than it should be.

《辐射 4》,后末日时代荒原流浪者的最新故事，昨天在[拿到了最新的 DLC](https://bethesda.net/#en/events/game/fallout-4-contraptions-workshop-available-now/2016/06/21/149) 。这个附加项目，*精巧装置车间，*给*辐射 4* 的定居建筑车间机械师增加了新的物品和零件。这个附加物带来了更多的建筑构件、电梯，以及最重要的*逻辑门*到英联邦定居点。

*辐射*逻辑门与发电机、灯和自动哨兵一起用于建造定居点。虽然一个简单的与非门就可以了，但还有几种逻辑门，包括与、或、异或、非、与非、或非和 XNOR。

游戏中对这些门的解释是非常非常奇怪。 AND、OR 和 XOR“根据输入功率的组合来决定是否传输功率”。“非”、“与非”、“或非”和“XNOR”显然是不同的，“只有当它们的输入直接连接到其他逻辑门的输出时才传输功率”。除了 Bethesda 的少数程序员和项目负责人之外，目前还不知道不同门集之间这种任意区别的原因。应该注意的是,{AND，OR，XOR}在功能上并不完整。

随着视频游戏中逻辑门的实现，出现了一些非常有趣但无用的应用。辐射 4 已经有了灯箱，T2 允许巨大的动画广告牌。*余波*音箱，废土的*相当于《我的世界》的* s 音块，[可以用来演奏简单的旋律](https://www.youtube.com/watch?v=rGtLhejkDhk)。你可以用 NAND 做任何事情，所以我们希望动画广告牌和单音合成器的自动化、有序版本会很快出现。

功能的完备可以为一款游戏加分不少。自从《我的世界》在游戏中加入了红石逻辑，我们已经看到了一些非常非常令人印象深刻的基于方块的构建。《我的世界》CPU [通常被认为是第一个，最完整的 CPU](http://hackaday.com/2010/09/29/16-bit-alu-in-minecraft/) 花了大约三个月的时间来设计和制造。这个版本没有使用后来添加到 redstone 工具箱中的东西，比如中继器、活塞和现在的 cheaty 命令块。