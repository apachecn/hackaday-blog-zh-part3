# 本周失败:我的 3D 打印机升级

> 原文：<https://hackaday.com/2016/04/29/fail-of-the-week-my-3d-printer-upgrade/>

在我的 Prusa Mendel i2 暴露的螺纹上切了几年之后，是时候进行一次早该进行的升级了。我不想只买一台新打印机，因为它一点也不好玩。所以，我决定为我的打印机买一个新的框架。我选定了 P3Steel，这是 Prusa i3 的激光切割钢版本。它没有 vanilla i3 潜在的方形问题，钢使得它比类似设计的丙烯酸或木框打印机更不稳定。

[![My trusty i2\. Very sharp. It... uh.. grew organically. ](img/f00ef1b660855e3c2ebae67a58d653b5.png)](https://hackaday.com/wp-content/uploads/2016/04/2016-04-10-12-00-04.jpg)

My trusty i2\. Very sharp. It… uh.. grew organically.

我期望我的新框架在可靠性和打印质量方面有巨大的提高。我希望花更少的时间摆弄它，花更多的时间打印。我最大的希望是切换到 M5 螺纹螺丝，而不是 i2 使用的 M8 将提高我的 z 层精度。我让我的旧打印机工作了足够长的时间来打印新打印机的零件，然后兴高采烈地组装我的新打印机。

我没有等到所有的电子设备都安装好了。不。是时候了。我点燃了它。我期待着最方正、最安静、最准确的印刷，以及惊人的 z 层对齐。我什么都没得到。我的指纹上有清晰可见的波纹。我的第一个倾向是，我过于突出。当然，我闪亮的新机械师不会有错。另外，我造了这台打印机，我是一个很好的打印机制造者，知道自己在做什么。过度挤压看起来很像 Z 轴的问题。所以，我调整我的挤压，直到它是完美的。

 [![Aww yea. First print on the new machine. This is going to be good. My mind is about to be blown at the quality of this print.](img/242b02e9eeafcc1f1801bc1a7b919c31.png "Aww yea. First print on the new machine. This is going to be good. My mind is about to be blown at the quality of this print.")](https://hackaday.com/2016/04/29/fail-of-the-week-my-3d-printer-upgrade/2016-04-10-23-00-27/) Aww yea. First print on the new machine. This is going to be good. My mind is about to be blown at the quality of this print. [![Nope. It sucks.](img/f09ea3f3cd0f85117f52365b20921675.png "2016-04-11 10.21.53")](https://hackaday.com/2016/04/29/fail-of-the-week-my-3d-printer-upgrade/2016-04-11-10-21-53/) Nope. It sucks.

没用。我的下一个目标是螺杆。我怀疑他们，因为我购买工具的供应商给了我非常光滑的棒。它们是未硬化的、未打磨的、不直的、普通的旧钢棒。对轴承来说毫无用处。最后，我不得不把旧打印机上的棒切断，取消了我为它们准备的一个项目。所以，从逻辑上讲，他们寄给我的螺杆也是垃圾。

[![Precision rod on the top, the rods I got on the bottom. I guess the pits in the surface are for holding oil?](img/0ca3c625496ad40b362a2f5ccc7e84ab.png)](https://hackaday.com/wp-content/uploads/2016/04/precision-rod.jpg)

Precision rod on the top, the rods I got on the bottom. Maybe they thought the surface pitting would help with lubrication?

我跑到五金店，买了一个全新的 M5 棒，一些新的 M5 坚果(这次有真正的等级评定)，然后回家。我花了一个小时拉直杆子，直到它们在我的桌子表面滚动，没有明显的高点。我安装了新的杆来代替打印机附带的杆。没有结果。事实上，新的燃料棒比旧的更不稳定。

在这一点上，我变得有点沮丧。我开始打印，尽可能仔细地观察打印机，注意任何明显的偏差。我用了一点橡胶管作为我的 z 螺纹杆和步进电机的耦合器。当我观察打印机运行时，我注意到偶尔螺纹杆会在连接器中滑动半圈，然后在下一次电机反转时返回到原来的方向。啊哈！我拆开了另一个项目，从他们那里抢走了一些螺旋切割的弹性联轴器。我更换了橡胶管。

[![You were the chosen one! You were supposed to bring balance to the printer!](img/e93721e839e4944c2f1d37872029e02c.png)](https://hackaday.com/wp-content/uploads/2016/04/coupler.jpg)

You were the chosen one! You were supposed to bring balance to the printer!

我大吃一惊。印刷质量几乎没有改善。怎么会？我修复了打印机上一个明显可见的缺陷。很明显，这种滑动是可重复的，以至于它自己解决了这个问题。好吧。嗯，我注意到，由于我的连接器的内径不完全匹配螺纹杆，杆没有完全对准步进机的轴。这可能会导致一些抖动。因此，我花了一些时间与 kapton 磁带，并得到螺纹杆运行作为中心，我可以不跑出去使用车床在黑客空间。

肯定就是这样。我已经更换了 Z 上的几乎所有组件至少一次。唉，还是摇摆不定。我正准备放弃任何对技术人员、工程师、黑客等的要求，去学习唱摇篮曲或考虑流浪。我决定再仔细看看打印机，看看是否能发现 z 有什么问题。

这时，我注意到，当仔细看时，Z 杆似乎以一个角度进入螺母。如果丝杠螺母以一个角度进入，这意味着它每次转动都必须弯曲。这 100%是抖动的原因，但是这个理论有问题。一个刚性固定的杆和一个精确放置的螺纹杆怎么会不对齐呢？

[![The culprit at last!](img/88e5f7d6b21549d07d656d3f801c7dbd.png)](https://hackaday.com/wp-content/uploads/2016/04/aha.jpg)

The culprit at last!

我的第一个想法是责怪我的旧打印机，因为这部分是在上面打印的。i2 打印正方形有问题。事情往往是平行四边形，尤其是在 Z 轴上(完全是我的错)。所以也许固定螺母和轴承的部分不是方形的。如果它向某个方向倾斜，肯定会导致这个问题。所以我小心翼翼地打印出新的零件，并完全按照以前的方式重新组装我的打印机。我知道我的新打印机是方形的。我量过了。所以这些新零件必须解决问题。他们必须这么做。

[![My precision mechanism adjuster. NSFW. As in if you use one of these to adjust a precision mechanism at work you'll get fired. Home use is fine tho;)](img/90062ba84e5857812290ecc3d85d02e4.png)](https://hackaday.com/wp-content/uploads/2016/04/precision-adjuster.jpg)

My precision mechanism adjuster. NSFW. As in if you use one of these to adjust a precision mechanism at work you’ll get fired. Home use is fine tho;)

流浪，对吧？我的意思是，新鲜的空气，不用洗衣服，偶尔免费的食物，只是散步。日复一日地生活着……尽管有了新的部件，它仍然摇摇晃晃。我还能修什么？所以我坐下来，第 50 次左右认真思考这个问题，令我惊讶的是，我想通了。是时候拿出我的精密机械调节器了。

我的逻辑是这样。机械装置的一边固定着 X 的光滑杆。另一侧有贯穿零件的孔。当你组装打印机时，你应该把杆从一部分滑过，然后把它们放在另一部分。嗯，我很聪明，我把两个部分的孔都铰了出来，使它们紧密地贴合。(对于塑料，你可以将光滑的杆夹在钻子里，穿过孔，它实际上会切割出一个很好的压配合。)

[![Here we can see all the parts( and my messy wiring job. Still waiting on that drag chain, China.) The left side holds the rods in place. The right side slides on the rods.](img/74da366d9d58c9c36bc066bd9ba7c139.png)](https://hackaday.com/wp-content/uploads/2016/04/2016-04-22-17-42-09.jpg)

Here we can see all the parts, as well as my messy wiring job. The left side holds the rods in place. The right side slides on the rods.

这使得双方能够非常安全地握住钓竿。P3 工具的设计非常巧妙。一边保持杆的稳定。另一边可以滑动。看起来，如果杆可以滑动，机器会不精确，但事实并非如此。杆仅将喷嘴保持在其 Z 位置。它们可以滑动的方向是 X。但是，喷嘴的 X 位置由皮带决定。燃料棒与此完全无关。皮带通过杆张紧到固定步进器的部分。所以，右滑架的 X 位置根本不影响喷嘴的 X 位置。

[![Old on the left. New on the right. Still not perfect, but a huge improvement.](img/e80c1daef1e0c1c84f7b64258b2bb26c.png)](https://hackaday.com/wp-content/uploads/2016/04/a-big.jpg)

Old on the left. New on the right. Still not perfect, but a huge improvement.

这是很多，但在理论上，这意味着如果一方可以滑动，它应该自我调整到 Z 杆。如果棒被适当地保持在适当的位置，理论上应该不可能使 Z-棒不对齐。也就是说，除非你故意把通孔做成压配合——这是我失败的地方。因此，部件不会沿着轴滑动，直到舒适地处于平衡状态。我可以在轴上选一个位置放它。我有强迫症，所以我确保我的轴与塑料部分的末端完全对齐，向内弯曲两根杆。这造成了我看到的角度。

我用我的精密机械调节器轻敲它，这给了它足够的力来克服静摩擦力，并使其接近平衡。我启动了打印机。你瞧，我的 Z 显著提高了。题图有个前后。

我仍然有一些问题(可能是因为我试图修复它时弄坏了很多东西)。我的 Z 不完美。我的下一步是从麦克马斯特订购螺纹杆的长度，因为他们的杆在螺纹上有公差，希望会更直。我还想把不锈钢螺母换成黄铜的，这样更合适。

我还想重印通孔部分，并铰出一个很好的滑动配合。理论上这将解决我的 Z 问题，但嘿，它可能只是别的东西。还有人有类似的调试经历吗？

* * *

《一周失败》是一个黑客专栏，它把庆祝失败作为一种学习工具。通过写下你自己的失败和[给我们发送一个故事的链接](mailto:tips@hackaday.com?Subject=[Fail of the Week])——或者发送你在互联网旅行中发现的失败报道的链接，帮助保持乐趣。