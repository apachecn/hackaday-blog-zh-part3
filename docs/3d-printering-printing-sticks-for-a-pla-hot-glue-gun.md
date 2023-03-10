# 3D 打印:PLA 热胶枪的打印棒

> 原文：<https://hackaday.com/2018/02/05/3d-printering-printing-sticks-for-a-pla-hot-glue-gun/>

什么时候热胶棒不是热胶棒？当然是解放军的时候！一旦我知道如何用 PLA 打印出我自己的“胶水”棒，一个可以分配熔化的 PLA 而不是热胶水的胶枪变成了一个将 3D 打印物体连接在一起的便捷工具。结果有点像加大尺寸的 3D 打印笔，但更简单，能够承受更大的挤压。但是这并不像把 PLA 碎片塞进一把热胶枪，然后猛扣扳机那么简单；一些小故障需要解决。

### PLA 为什么要用胶枪？

一些解决方案来自于以正确的心态看待两个不同的事物，并意识到它们可以融合在一起。在这种情况下，我最近将一个大的、中空的 3D 模型分割成更小的 3D 打印机大小的部分，并将其全部打印出来，但我发现自己遇到了一个问题。我现在有大量弯曲的薄壁零件需要彼此平齐连接。这些基本上都是对接接头，是最弱的一种接头，几乎没有粘合的表面。最重要的是，弯曲的表面意味着夹紧是不切实际的，而且在粘合时，任何碎片的移动都会导致其他碎片无法对齐。

一个优点是只有我的空心模型的外部是一个展示表面；里面可能很丑。像这样的工作，热胶枪是值得考虑的。这个想法是将两块拼在一起，展示面彼此对齐，然后在接缝的内侧(非展示面)涂上熔化的胶水将接缝固定在一起。让热胶冷却变硬，重复。这是一个可行的过程，但我觉得在这种情况下用热熔胶并不合适。热熔胶完全冷却的速度很慢，并且总是有一点弹性。我想快速工作，我希望关节坚硬僵硬。我真正想要的是融化的聚乳酸而不是胶水，但我没有办法做到这一点。[摩擦焊接 3D 打印件](https://hackaday.com/2014/12/30/3d-printing-technique-friction-welding/)是一种可能性，但我怀疑我的旋转工具在尴尬的方位会有多灵活。当我看到我的廉价桌面胶枪时，我正考虑订购一只 3D 打印笔作为小型 PLA 点焊机使用。

一支胶枪拥有我需要的一切:良好的人体工程学、良好的尖端可视性和战术触觉反馈，以及简单的机械操作。如果它能挤出熔化的 PLA 而不是热熔胶，它将是这项工作的理想工具。经过一些初步的测试和与同事的讨论，很明显，尝试实现这一点是值得的，可能会破坏一个廉价的胶枪。

### 胶枪会融化 PLA 吗？

根据 PLA 的 [RepRap Wiki 条目，它在 60°C 到 65°C 左右软化，在 180°C 到 220°C 左右熔化。胶枪可以完成这项工作吗？为了找到这个问题的答案，我手动将一捆废弃的 PLA 细丝推过一个我不介意毁掉的小型桌面胶枪。胶枪是为低温胶棒制造的业余爱好装置。小爱好单位最终融化了解放军，但只是勉强；解放军出来更像软化油灰。基于](http://reprap.org/wiki/PLA)[这种廉价的业余爱好胶枪](https://hackaday.com/2017/11/22/teardown-of-a-cheap-glue-gun/)的拆卸，工作温度预计在 150℃左右，这不足以真正适当地熔化 PLA。

在这个过程中，另一件变得清晰的事情是，胶枪对挤出和进料有特殊的需求。为了正确地输送，触发机制需要能够抓住并推动一个实心圆柱体，而不是一束细丝。此外，适当的挤出需要完全填满熔化室开口的固体形状，以防止回流。否则，熔化的塑料宁愿从后面溢出，而不是被迫通过喷嘴。换句话说，我需要:

*   高温胶枪，还有
*   由 PLA 而不是热熔胶制成的正确大小和形状的“胶棒”

经过一番研究，我购买了一把经济型高温胶枪，据称功率为 80 瓦，工作温度高达 208 摄氏度。

### 测试解放军“胶棒”

![](img/6365a5a2a70b423a11b9b8680f932e93.png)

Test with straight-walled plain cylinder of PLA. The back of the stick was printed with black so I could get an idea of where the stick ended when extruding.

为了给我的新胶枪供料，我需要一个直径 11 毫米、至少 5 英寸长的圆筒。令人高兴的是，3D 打印机存在的唯一目的是将 1.75 毫米的细丝变成其他形状和大小。使用 3D 打印机简单地将 1.75 毫米直径的塑料变成 11 毫米直径的塑料感觉有点奇怪，但在大约一个小时内，我打印了一个高(75%)填充 11 毫米 x 150 毫米的 PLA 圆柱体用于测试。

PLA 的第一棒足以表明 80 W 胶枪能够可接受地熔化和挤出 PLA；唯一的问题是在我的冷车间里需要 10 到 15 分钟的预热，相比之下，热胶水只需要 5 分钟甚至更少。

但是，暴露了一个问题。胶枪的进给机构有一个小杠杆臂，当扳机被拉动时，它咬入胶棒并向前推动胶棒。然而，解放军“胶棒”光滑而坚硬，进给系统无法正确地咬入其中。事实上，解放军圆柱的脊状表面很快就磨损了小臂上的牙齿，因为它徒劳地试图找到可以抓住的东西。

### 通过在 PLA 棒上增加凹槽解决了进料问题

解决方案是对胶棒的 3D 模型做一个小小的改变。在圆柱体模型上添加一系列成角度的槽口，可以让抬起的臂完美地锁定和推动。

[![](img/bc8dd715f3670a29e803f307fc97ea71.png)](https://hackaday.com/2018/02/05/3d-printering-printing-sticks-for-a-pla-hot-glue-gun/makersdate2017-9-23ver6lenskan03actlar02e-ve-2/)

This little lever rises when the trigger is pulled.

[![](img/a58a796370abbedf3a5ba9d941918ea3.png)](https://hackaday.com/2018/02/05/3d-printering-printing-sticks-for-a-pla-hot-glue-gun/makersdate2017-9-23ver6lenskan03actlar02e-ve-3/)

Showing wear on arm that rises to grip the glue stick. Teeth are notched from rubbing on PLA.

[![](img/e8e5a3c60d3a4a7096955daf4216830e.png)](https://hackaday.com/2018/02/05/3d-printering-printing-sticks-for-a-pla-hot-glue-gun/makersdate2017-9-23ver6lenskan03actlar02e-ve-9/)

Notched PLA “glue stick” engages properly to the feed system.

### 测试债券

使用 80 W 胶枪进行熔化，当扣动扳机时，PLA 圆柱体上的凹槽允许进料系统完成其工作，熔化的 PLA 容易流动并具有良好的控制。我做了一些简单的测试:

1.  像胶水一样使用 PLA，沉积一滴熔化的液体，然后在上面捣碎一部分。结果很好，但 PLA 团增加了一些体积，因为它在开始冷却和硬化之前没有完全涂抹。
2.  接合缝:熔化的 PLA 仅稍微熔化到被接合的表面，但是仍然惊人地坚固。我能够把接缝拉开，但在这个过程中总是会弄破一个或另一个表面，或者把接缝本身分成两半(剩下的部分粘在我连接的部分上)。

[![](img/ae0447d79f8632eae5abc229c5c86d16.png)](https://hackaday.com/2018/02/05/3d-printering-printing-sticks-for-a-pla-hot-glue-gun/makersdate2017-9-23ver6lenskan03actlar02e-ve-4/)

Left and center: using PLA as if it were a blob of glue. Right: applying along a seam between parts.

[![](img/6dcdb423a1f5a40001ee35958b6e46e6.png)](https://hackaday.com/2018/02/05/3d-printering-printing-sticks-for-a-pla-hot-glue-gun/makersdate2017-9-23ver6lenskan03actlar02e-ve-5/)

The bottom surface is a scrap raft. Slight melting visible around seam on the right.

[![](img/f63c74b63079110c068336e7e7f2c56a.png)](https://hackaday.com/2018/02/05/3d-printering-printing-sticks-for-a-pla-hot-glue-gun/makersdate2017-9-23ver6lenskan03actlar02e-ve-6/)

Results of pulling the pieces apart until they failed. The two on the left had lots of leverage. The small piece on the right could not be broken off without destroying it.

[![](img/c4436e3b1c9b7c2881977d16df7cf6b1.png)](https://hackaday.com/2018/02/05/3d-printering-printing-sticks-for-a-pla-hot-glue-gun/makersdate2017-9-23ver6lenskan03actlar02e-ve-7/)

This part has been cut in two to see how much actual melting together between the parts has occurred. Not much, and superficial only.

[![](img/77150f9cd2764e4df1e45ef5124ca335.png)](https://hackaday.com/2018/02/05/3d-printering-printing-sticks-for-a-pla-hot-glue-gun/makersdate2017-9-23ver6lenskan03actlar02e-ve-8/)

Pulling the pieces apart until failure still took effort and resulted in the bead splitting in two instead of simply popping apart.

### 真的有焊接吗？

当接头和两部分的材料融为一体时，就形成了真正的焊接。事实显然并非如此。有一些融合在一起的事情发生，但充其量只是表面的。尽管如此，结果很容易通过“拖船测试”。剖开的测试接头显示红色 PLA 已经流入并充满了每个角落和缝隙，这可能是大部分强度的原因。

### 经验教训

*   一个小爱好胶枪可靠地软化，但没有融化解放军。为高温热熔胶而设计的胶枪，可以很好地熔化 PLA。
*   测试胶枪是一个经济的双加热器 80 W 装置，但需要 10 分钟或更长时间来加热和熔化填充腔室的塑料(相比之下，热胶只需 5 分钟或更短时间)。)
*   除了热量之外，阻止 PLA 用于胶枪的最大问题是胶枪的进料机构不能夹紧和推动光滑、坚硬的 PLA。他们期待更柔软的热胶棒。测试枪与侧面有凹口的 PLA 棒一起工作良好，但这将根据所使用的特定胶枪的设计而变化。
*   我的简单开槽胶棒的 STL 文件在 GitHub 上有[。它可能与其他喷胶枪进料系统兼容，也可能不兼容。](https://github.com/DPHAD/PLA-Glue-Stick)
*   这不是一个很大的焊接，因为它只是表面的，但它仍然需要更多的努力来拉开碎片。
*   实验很有趣。

### 解放军胶枪管用吗？

我的大型多件式 3D 打印件是一个大的中空物体，薄件像拼图一样装配在一起，使用 PLA 胶枪快速有效地将这些 3D 打印件粘在一起，无需夹紧，这比预期的要好。

对于 PLA 胶枪可能无法完成工作的情况，在 OpenSCAD 的帮助下，使用[这种方法来简化多部分模型的打印和组装](https://hackaday.com/2017/12/29/3d-printing-without-support-2/)。但对于我的大空心模型，手动对齐表面和粘合内部接缝快速、简单、坚固，绝对值得重新使用 30 美元的胶枪，并在工具抽屉中给它一个位置。