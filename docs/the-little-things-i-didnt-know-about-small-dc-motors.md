# 我不知道的关于小 DC 汽车的小事情

> 原文：<https://hackaday.com/2016/10/17/the-little-things-i-didnt-know-about-small-dc-motors/>

我们都拆开了一个小玩具，拿出了一个小马达。“用这个！我什么都能做！”我们高举着它宣告。十分钟后，我们让它转了几圈后，它就进了抽屉，再也看不见了。

[![](img/6a0d4e72e40c5e6367a99df000dcc08f.png)](https://hackaday.com/wp-content/uploads/2016/10/mark_o1.png)

It’s all their fault

看起来它们似乎无处不在，但是让它们在项目中发挥作用却是徒劳的。它们到底是干什么用的？人们从哪里学到让他们发挥作用所需的黑魔法？为他们拉出规格表是很容易的。它们中的大部分是由日本 Mabuchi Motor Corporation 制造或仿制的。仅该公司一年就生产超过 15 亿台微型发动机。

## 不仅仅是规格

在规格中，您会发现运行速度、电压、失速电流和失速扭矩等内容。但是他们没有提供令人信服的应用指南，或者工程师在使用之前应该做的基本假设。这绝不是一个完整的列表，几乎完全跳过了电气，因为这方面的 DC 汽车公司是不合理的良好记录。

[![The paint mixers high running speed and infrequent use make it a decent candidate for hooking directly to the motor.](img/3fd89768e579cbdf32bb205ce1d46305.png)](https://hackaday.com/wp-content/uploads/2016/09/2016-02-01-11-15-56-hdr-2.jpg)

The paint mixers high running speed and infrequent use make it a decent candidate for hooking directly to the motor.

首先要注意的是，它们真的不是用来直接驱动任何东西的。它们通过齿轮系与实际驾驶隔离开来。这有很多原因。首先，它们通常旋转非常快，即使是最小的电机，6000–15000 rpm 也不是不正常的。因此，尽管数据手册可能会抛出一些令人印象深刻的东西，比如 3 瓦电机，但事实并非如此。确切地说，是每分钟 15000 转电机的 3 N*m/s。或者仅仅 1.2 毫瓦每转，这是一种奇怪的单位，我只是用来演示，但它给你的感觉是没有一吨的“活力”。然而，如果你开始用一个齿轮系将许多旋转组合在一起，你可以开始从中获得一些真正的动力，即使有摩擦损失。

我能想到的唯一经常打破这一规则的消费品是非常便宜的儿童玩具，它们的设计寿命都不长，还有那些电动橡皮和咖啡搅拌器。这两者都想当然地认为他们的扭矩需求很低，速度需求很高，或者电机烧毁对世界来说没有真正的损失(至少在短期内)。

这是因为马达几乎立即减额。这些电机中的大多数是数百圈非常细的漆包线，缠绕在一些硅钢板上，点焊或以其他方式压在一起。这意味着，即使几毫秒的小热量事件也足以烧穿 10 微米厚的线圈绝缘涂层。实际上，如果你连续几次让一个小马达停转，你还不如把它扔掉，因为再也无法猜测它的实际性能等级了。同样，持续的启动困难、过电压、过电流和其他滥用会很快损坏电机。因为它产生的能量意味着分散在许多旋转中，所以马达根本不是设计成(也不可能合理地建造成)在一次戏剧性的推动中产生全部能量。

## 进行接触

[![Pololu has the clearest picture of the different kind of brushes inside these small motors.](img/74ded0eda0a4be3f950fb45cbf9ad99b.png)](https://hackaday.com/wp-content/uploads/2016/09/0j6412-1200.jpg)

Pololu has the clearest picture of the different kind of brushes inside these small motors.

这让我想到了关于这些微型马达的另一个小问题。他们中的大多数没有碳刷，人们开始期望从更强大的电机。大多数情况下，他们有一个铜条，冲压有几个手指压在换向器上。这些金属触点有很多优点，并不都是削减成本，但除非你设法阅读了 Ragnar Holm 的“电触点”并真正理解它，否则很难解释它们。有各种各样的魔法。例如，仅仅在换向器表面形成合适的氧化膜本身就是一场战斗。

这是一个奇怪的交易。首先，你可以用金属触点使马达更便宜。金属触点的摩擦也比碳刷或石墨刷低得多。它们更安静，传输的电流也更少，这似乎是一件坏事，但如果你有一个像头发一样的电机在传输小精灵，你最不想做的事情就是通过它们传输尽可能多的电流。然而，一张薄薄的铜片也不会持续很长时间。

所以它归结为这一点，至少我的理解是:如果爆发非常快，低能量，高效率的运动是所有的电机在其工作寿命的要求，那么金属条刷是完美的。如果你需要运行电机一段时间，噪音不是一个问题，那么碳刷版本将工作，只是不要停止它。会多花一点钱。

## 照顾好你的小马达

[![Here is one of these can motors being restrained properly. Only torque on the case itself is restrained. The motor is otherwise free to move.](img/861575658a25b1f8363f61ba5eacd8a9.png)](https://hackaday.com/wp-content/uploads/2016/09/held_loose.jpg)

Here is one of these motors being restrained properly. Only torque on the case is restrained. The motor is otherwise free to move.

去触碰另一个小小的机械装置。它们的设计根本不能承受任何轴向载荷，甚至不能承受任何径向载荷。大多数都有一个塑料或铝青铜衬套，压入一个简单的冲压钢体。因此，如果你为其中一个设计齿轮箱，一定要在轴承表面施加尽可能小的力。如果你曾经拆开过一个小玩具，你可能会注意到马达可以在它的底座上来回滑动。这就是为什么。

最后，因为大多数这些电机只是不打算运行在他们的书面最大规格附近，所以最好假设他们的规格是善意的，但完全是谎言。大多数设计使用电子表格上最大数字的底部 25%。随着时间的推移，在接近顶部的任何地方运行电机通常都会损坏。

这些都是有用且无处不在的马达，但与它们更强大的表亲不同，它们有自己的一系列挑战。然而，考虑到你可以以比糖果更便宜的价格买到它们，有一个很好的理由去熟悉它们。