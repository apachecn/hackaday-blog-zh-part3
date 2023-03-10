# 建筑设置限制导致了 Z 高度的愚蠢

> 原文：<https://hackaday.com/2017/09/01/building-set-limitations-make-for-z-height-follies/>

我在一个小型数控工厂工作，这个工厂以机器人建筑为起点。我不知道该从过程中期待什么。也许连接会太不稳定，让这台机器除了好奇什么都不是。也许我将能够做钢笔绘图和巴尔萨雕刻，但没有比这更难的了。我的目标是让它雕刻 PCB，但最终重要的是我有一个工具，它的惊人之处证明了我在这个项目上投入的费用。

到目前为止，这个过程很有趣。但最近 Z 轴的建设尤其如此。这提出了一个非常有趣的问题:未知的成品设计和已知的材料参数之间的平衡在哪里？

### 设计 Z

我是这方面的初学者，但人们可以凭直觉知道所需的基本尺寸。总行程要求是工具的长度、工件和/或滑板的厚度，加上安装夹具所需的间隙。我预计使用的大多数切割工具是两英寸或更小，包括夹头。轴承也是一个因素。轨道的长度减去两个块的距离决定了 Z 移动的距离

但是最小并不意味着我想要最小。我也想要一点空间，这样我可以快速地移走工件。更高的 z 肯定有优点和缺点。首先，稳定性是一个因素。长度越短，结构越坚硬。但是更短的 Z 也限制了你可以用它做什么，工具方面。例如，第 4 轴转动工具头，从一个角度撞击工件。也许我需要一把有微型步进器转动刀片的拖油刀。我绝对不会考虑的一件事是磨厚的材料。我真的不想在 z 上雕刻太多，即使一英寸也比我对这个项目感兴趣。

我选择了一个相当标准的机架设置，其中 Z 轴(目前)由 NEMA-17 步进器驱动，步进器转动丝杠。该产品系列包括两种不同的螺母，它们设计得非常好，仅重力就能让它们转动——抓住螺母，丝杠就会旋转出来。现在，12 英寸的丝杠让我觉得门架非常高。Z 电机的顶部离工作台约 17 英寸。完成后工具柄会有多大的提升力很难猜测，因为我没有合适的滑板，也没有主轴。

到目前为止，我在“构建集合”方法中遇到的最大问题之一是，我发现自己受到了使集合成为一个集合而不是一个随机的碎片的限制。必须有某种制度，现在这个制度正在挑战我。

### 明智地破解它

[![](img/7463d2a9d5274a2f5930b613d823b4db.png)](https://hackaday.com/wp-content/uploads/2017/08/img_1343.jpg) 从一个构建集合中构建一个项目迫使你根据那个集合的系统来构建它——要么这样，要么在某个时候你必须有意识地决定放弃这个系统。如果横梁只有这么大，你不能神奇地让它们变大。如果一根横梁有 100 毫米长，你不能拿出钢锯把它锯短。

```
::record scratch noise::
```

你当然可以。在 Hackaday 上，我们遵循这样一种风气:如果我买了它，我可能、能够并且应该黑掉它，如果那是我想做的。也就是说，如果要花钱，而我又买不起，我肯定会加倍确保我做的是对的。

我正在使用的产品 Actobotics 的特点是金属通道布满了两种不同的孔模式，允许各种各样的部件连接。该方案有足够的迭代，理论上你可以做一个轻型数控铣床，是我的想法。与定制的加工部件相比，构建集的优势在于我可以随意改变我的项目。如果我不喜欢项目中的 9”梁，我可以删除它们并添加 6”梁。集合使迭代成为一个梦想。根据设置，你也可以放心，像电机安装和轴承的附件将是兼容的。

但是集合也会限制你。当我建造我的高屁股 Z 并且决定它太大的时候，我的预期变化被产品提供给我的限制了。我应该砍掉一些部分使它达到完美的高度吗？也许吧，但还不是时候。

我必须承认，并拒绝这种心理成分——零件有内在的价值，因此布景的纯度比我用它做的项目更重要。最合理的决定是使用 hackerspace 的切割带锯将丝杠切割成我想要的任何尺寸。要么这样，要么出去找我自己的该死的部分，而不依赖于什么是可用的一套。

然而，我还没有这样做，原因很可能是:我仍然不知道我的 z 应该达到什么高度。你对我目前的身材有什么建议吗？你有没有经历过同样的“砍它还是保存它？”难题？请在下面的评论中告诉我们。