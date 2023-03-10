# 本周失败:我的毛衣呢？

> 原文：<https://hackaday.com/2016/06/17/fail-of-the-week-wheres-me-jumper/>

如果你认为我们这些为 Hackaday 写文章的人是工程天才中的精英，他们从不犯错，他们的长凳上可以看到一系列完美执行的构建和惊人的黑客，让我用我自己的一个不光彩的失败来纠正你的这种想法。

几周前，我在制作一个电子工具包。这是一种模块化设计，背板上有多个卡，不过由于在适当的时候您将在这里看到对它的回顾，所以我将把它的细节保存到那时。在我几十年的电子工作中，我已经制作了许多套件，所以这一个作为标准 0.1 英寸间距的通孔设计应该不会给我带来任何问题。遗憾的是，事情并没有这样发展。

在制作快结束的时候，事情开始变得不对劲，[我注意到我的烙铁上的温度调节器在制作过程中的某个时候出了故障](http://hackaday.com/2016/06/01/long-term-review-weller-magnastat-soldering-iron/)。因此，它的大部分是在令人担忧的高温下焊接的，所以我面临着大量的焊接点，以检查和返工，以防它们中的任何一个因过热而变干。

在适当的时候，当我给我的全套设备加电时，没有任何东西工作。我想，这一定是额外的热量，所以脱去了脱去的辫子，我又重新制作了整套工具。还是没有欢乐。打开我的示波器，我可以看到它的时钟和数据线上发生的事情，所以有希望，但这不是一个对治疗有反应的套件。与(非常耐心的)药盒制造商的一次长谈让我追踪了一系列途径，但都无济于事。这时，几周断断续续的诊断来了又去，我开始绝望了。不知何故，我用我有缺陷的熨斗煮了这个东西，没有办法找到罪魁祸首。

在我们的 hackspace 开放之夜，我坐在那里，将工具包放在面前，再次查看它的各种信号。我拿出万用表，开始艰难地追踪我返工的每一个关节的连续性，确信这样我就能找到干燥的关节。我并没有失望，因为在外部背板插座上的一条线和它的邻居上的一条线之间，我没有发现电路。我的罪犯终于来了！然后我找到了另一个，又一个。一整条总线，与其余的插座断开。一种恐怖的怀疑开始形成，我仔细看了看背板。

该背板在该套件的早期版本中是作为一片条形板出现的。您购买了子板，并提供了自己的条形板。我曾天真地认为背板仅仅相当于一块奇特的条板，但我错了。我原本以为是一个插座将总线连接到另一块电路板的空间，结果却是一组跳线的空间，这些跳线将总线隔离在最后一个插座上。在某些应用中，它们可以填充电阻，我只需要一组跳线，我的最终电路板就可以与其邻居通话。我安装了双排插销和跳线，就像变魔术一样，套件工作了。

那么我能从这一切中得到什么呢？首先，跳线在套件说明的原理图中有，它们的作用很清楚。所以我没能发现这一点，因为我看到了以前的带板版本的套件。其次，我抓住我的有缺陷的铁作为明显的罪魁祸首，而没有努力去寻找其他任何东西。[确认偏差](https://en.wikipedia.org/wiki/Confirmation_bias)，你又认领了一个受害者！

如果我可以给你留下任何东西带走，那就是当我们遇到失败时，我们在 Hackaday 不得不吃自己的狗粮，正如我刚刚发现的那样，在没有真正阅读的情况下阅读说明太容易了。下一次，我们中的任何人有了看似无法解决的错误，而我们确信已经找到了原因，我们都应该试着后退一步，想想我们是否做对了，或者我们是不是找错了对象。毕竟，它可以让我们避免像这里描述的那种公开失败的尴尬，这种努力是值得的！

跳线图片:By Anthrax11 [CC BY-SA 4.0]，via [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:IO_Expansion_Board_Jumpers.jpg) 。

当然，我为这篇文章的标题向 Ping FC 的苏丹们道歉。

* * *

《一周失败》是一个黑客专栏，它把庆祝失败作为一种学习工具。通过写下你自己的失败和[给我们发送一个故事的链接](mailto:tips@hackaday.com?Subject=[Fail of the Week])——或者发送你在互联网旅行中发现的失败报道的链接，帮助保持乐趣。