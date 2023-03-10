# 印刷磁场

> 原文：<https://hackaday.com/2016/04/25/printing-magnetic-fields/>

不久前我们告诉过你这些“可打印”的磁铁。当你有能力将许多更小的磁铁挤到一个小点上，并随意调整它们的北/南方向时，你不仅可以控制整体磁场的强度，还可以构建新的看似违反物理的小部件。本文将不会关注磁铁本身，而是我们将剥去隐藏他们的漂亮的小打印机的内部工作的封闭的源护罩。关于这些可打印的磁铁已经有了很多讨论，但是关于它们是如何制造的却很少。今天这种情况发生了变化。我们将向你展示这种磁场打印机是如何工作的，这样你就可以忙着自己制作了。

## 历史

几年前，一家名为 Correlated Magnetic Research 的公司向世界介绍了一种带有微型磁打印机的磁场打印机的想法。它的售价高达 45，000 美元，这使得它仅限于企业和资金充足的大学。他们最终将公司更名为 [Polymagnet](http://www.polymagnet.com/) ，现在专注于自己制造磁铁。然而，他们似乎已经改进了他们的打印机，以获得更高的分辨率。在这个视频[中跳到 2:45](https://www.youtube.com/watch?v=SWuVzhTd6Fc)来看迷你磁打印机的运行。现在，在此视频[跳到 7.25](https://www.youtube.com/watch?v=IANBoybVApQ)看他们的下一代打印机。现在让我们弄清楚它们是如何工作的。

## 我们所知道的

![magnet_06](img/64abe5733008aa38eee420e9663b165d.png)

Original Mini MagPrinter

首先，你可以把你的 Kickstarter 创意扔进回收站，因为他们为他们的 [打印机](https://www.google.com/patents/US20140035707?dq=ininventor:%22Larry+W.+Fullerton%22&hl=en&sa=X&ved=0ahUKEwj3qqXhsprMAhUBjSwKHc8rBZ04FBDoAQhMMAc)持有[几个](http://www.google.com/patents/US20140062241)[专利。但这并不意味着你不能在你的车库或你的黑客空间里做一个。他们的机器可能价值 45000 美元，但我们愿意赌上一打 Raspberry Pi，赌你能以低两个数量级的价格制造一个。但首先我们需要知道它是如何工作的。先来看科学。](https://www.google.com/patents/US9105384?dq=ininventor:%22Larry+W.+Fullerton%22&hl=en&sa=X&ved=0ahUKEwiYwfv_sprMAhWCXCwKHUSjBQU4KBDoAQgiMAE)

### 居里点

[居里点](https://en.wikipedia.org/wiki/Curie_temperature)是磁铁失去磁场的温度。从理论上讲，磁性来自电子的自旋和角动量。如果你把它们排列正确，你会得到一个磁铁。当你把金属加热到超过居里点时，这种排列就会被打乱，你就会失去磁性。当然，你可以通过将金属引入强磁场来重新排列原子。

### Halbach Array

当较小的磁体排列成使它们的磁场集中在一个特定方向并在另一个方向抵消时，就产生了一个[哈尔巴赫阵列](https://en.wikipedia.org/wiki/Halbach_array)。磁场打印机制造的磁体可以被认为是哈尔巴赫阵列。

## 它是如何工作的

一切从一块空白的钕磁铁开始。我们都熟悉数控技术，所以我们将重点放在磁场打印头本身。通读原始文章的评论，许多人认为它使用了超过居里点的加热和高强度电磁体的组合来将磁场“写入”空白。然而，在仔细研究了[这个专利](https://www.google.com/patents/US20140035707?dq=ininventor:%22Larry+W.+Fullerton%22&hl=en&sa=X&ved=0ahUKEwj3qqXhsprMAhUBjSwKHc8rBZ04FBDoAQhMMAc)之后，情况似乎并非如此。不涉及加热。打印头由“具有多层和贯穿多层的孔的感应线圈”组成，其工作原理是“从感应线圈发射磁场，该磁场磁化可磁化材料表面上的区域……”。简而言之，它只是一个强大的局部磁场。

![magnet_07](img/0c2256c351589eeff3159c15d2d52d28.png)

Left – Magnetic field print head. Right – Drawing of internal structure of the print head.

## 自己做

现在你对如何打印磁场有了一个基本的想法，你可以开始自己的设计了。你已经知道如何制造 3d 打印机和激光切割机。只需采用其中一种设计，用您定制的磁性打印头替换打印头，开发一些软件，并将这项技术引入开源社区。[空白钕磁铁](http://www.ebay.com/itm/10PCS-Super-Strong-Round-Disc-Magnets-Rare-Earth-Neodymium-Magnet-N52-12x3mm-/131701749679?hash=item1eaa0937af:g:Cd0AAOSwoydWmMZT)和[磁场观片](http://www.amazon.com/Magnetic-Viewing-Film-Field-Display/dp/B00129CCGS)相当便宜。第一个印上骷髅头和扳手标志的人可以得到一件免费的 t 恤！