# 硬币电池挑战:启动汽车

> 原文：<https://hackaday.com/2017/12/08/coin-cell-challenge-jump-starting-a-car/>

显然，作为“不成功便成仁”这句老话的信奉者，[Ted Yapo]决定做一件乍看之下似乎不可能的事情:[用 CR2477 电池启动他的汽车](https://hackaday.io/project/28432-coin-cell-jump-starter)。他已经做了数学计算，看起来很有希望，尽管现实世界是否能适应还有待观察。至少，【Ted】[找到了一个【electro boom】](https://www.youtube.com/watch?v=tKki89sq0XY)的视频，声称用超级电容启动了一辆汽车，所以也不是完全没有先例。

在做一些研究时，[Ted]发现在 14 V 电压下，启动普通汽车发动机大约需要 2,000 W 到 3,000 W。这显然远远超过了一个硬币电池所能瞬间释放的能量，但关键在于这些电池中存储的惊人的潜在能量。如果电池在 3 V 时的额定容量为 1000 mAh，[Ted]显示了计算储存能量(焦耳)的数学公式:

[![](img/a262d36814fcd5f5325f4c2e9c08d2cb.png)](https://hackaday.com/wp-content/uploads/2017/12/cellstart_detail.png)

根据[ElectroBOOM]的视频，他只能用 6527 焦耳启动他的汽车，而[Ted]根据他的研究计算出应该只需要大约 9000 焦耳。所以只要他能拿出一个升压转换器，能以足够高的效率给电容充电，这个应该是十拿九稳了。

[Ted]已经开始组装一些早期硬件，甚至公布了他在 PIC12LF1571 上用来驱动转换器的源代码。他指出，根据他的计算，目前的充电效率大约是所需的一半，但他确实提到这是一个早期测试，可以进行改进。会开始吗？如果是的话，这将是一件令人敬畏的重任。

Coin Cell ChallengeBuild something cool powered
by a coin cell, win prizes![Enter now](https://hackaday.io/contest/28283-coin-cell-challenge)[See all entries](https://hackaday.io/submissions/coin-cell-challenge/list)