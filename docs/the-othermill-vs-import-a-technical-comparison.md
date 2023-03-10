# 另一个磨坊是另一回事

> 原文：<https://hackaday.com/2016/08/02/the-othermill-vs-import-a-technical-comparison/>

我承认。当我第一次看到另一家工厂时，我以为它只是另一家内部装有廉价中国硬件的工厂。我很惭愧地说，我甚至垃圾谈论它一点点。这给了我另一个机会重新认识到，我应该在成为一个混蛋之前做我的研究，彻底检查我的假设，即使这样也不建议。另一家机器公司很友好，让我去了加州伯克利的办公室。首席执行官[Danielle]带领我了解了工厂的设计以及运营过程中面临的挑战。

Othermill 是一台严肃的机器，随着最近 Othermill Pro 的发布，它只会变得更好。这些零件并不便宜。这一点可能更明显，但它几乎完全由美国采购的零件制成，包括定制的步进电机。没有任何滚珠轴承会在一年内开始发出奇怪的声音。它现在可以全天在 PCB 上切割 6 密耳的迹线。要正确看待它。Othermill Pro 的价格是 LPKF 的三分之一，但功能相同。

## 历史:

[![IMG_0347](img/91d76277eb6b8d13ac1e52a3ce3bf42e.png)](https://hackaday.com/wp-content/uploads/2016/05/img_0347.jpg)other mill 最初是由 [DARPA 拨款](https://theblueprint.com/stories/othermill/)在 Otherlab 研究的。他们希望每个教室都有一台便宜、耐用、易于理解的 CNC，拥有与激光切割机相同的功能，但没有有毒气体或火灾危险。它导致了一个相当奇怪的机器。这台机器工作起来就像是一台带有转轴而不是刀片的乙烯基切割机。片状原料被送入滚筒，它来回移动材料，直到完成。我对这个设计有些怀疑，但是[Danielle]向我保证它运行得很好。因为她有博士学位，并且是一家数控机床公司的首席执行官，所以我倾向于相信她。

但是，这个机器不是我们今天看到的机器。一如既往反复无常的政府，在地板上看到一个更新、更亮的按钮，摇摇摆摆地走过去，边跑边从粘糊糊的手指上扔下另一个磨坊研究项目。随着几乎所有资金的消失，其他机器公司应该已经放弃了，相反，他们重组，接受一些工作只是为了保持运转，并朝着 Kickstarter 的方向努力。

[![The first version of the othermill was fastenerless. ](img/c898c8b5b4481e547f5537814519d3e6.png)](https://hackaday.com/wp-content/uploads/2016/05/fastnerless.jpg)

The first version of the Othermill was fastenerless.

他们机器的下一次迭代，也就是在 [Kickstarter 视频](https://www.kickstarter.com/projects/otherfab/the-othermill-custom-circuits-at-your-fingertips/description)中展示的机器，开始向我们今天看到的另一个磨坊转变。有趣的是，这台机器一开始是没有紧固件的[。](http://mtm.cba.mit.edu/machines/mtm_snap-lock/)这是一个很酷的设计选择，有一些优点，但不足以取代紧固件的使用。机加工成本更高，机器也更难维修。

在 Kickstarter 最终发布的整个开发过程中，该机器进行了大量升级。它长出了把手。它有一个封闭的建筑体量。电线管理得很好。除此之外，他们还添加了一个非常好的软件堆栈。波兰人的水平令人印象深刻。

最终，这一招奏效了。其他机器公司没有倒闭。它努力获得足够的财务独立，从其他实验室分离出来，在伯克利拥有自己的设施。

## 有什么区别？低端 vs 高端？

对于一个跌跌撞撞地走进另一家工厂的业余爱好者来说，很难理解为什么要花这么多钱。Ebay 以三分之一的价格拥有来自中国的 3020 台数控铣床。为什么有人要花额外的钱买一台纸上规格非常相似的机器呢？这些规格很好，但是所有的规格都是在星星都排成一行，首席工程师刚刚花了三天时间调整设备，营销有点醉了，首席执行官很烦躁的时候写的。

纸上规格会给你一个预期的指示，但评估现实世界的性能会给你真相。即使是规格完全相同的顶级数控机床，在切割、噪音、振动、表面光洁度、速度等方面也会有所不同。如果不是这样，他们就不会花无数的时间用推销员来纠缠公司。他们只要贴出最低价格，人们就会购买。

### 振动:

![http://www.thingiverse.com/thing:277394](img/9f5b11394d095b788e84d20e48d3bae1.png)

[http://www.thingiverse.com/thing:277394](http://www.thingiverse.com/thing:277394)

振动在数控机床中是一件很微妙的事情。就其本质而言，这种机器会发出很大的噪音，到处扔芯片，而且通常会弄得一团糟。如果你把一个好的 CNC 放在一个相当差的 CNC 旁边，用相同的设置并排运行它们，你通常很难马上发现真正明显的差异。然而，当需要将两个零件装配在一起或检查零件的表面光洁度时，真相就变得显而易见了。振动很重要。

在姊妹机 3D 打印机中，真的很容易看到震动的效果，如右图所示。框架上的动态力加起来会在塑料中产生可重复的振动。你可以在版画的墙上看到[节点和](http://www.physicsclassroom.com/class/waves/Lesson-4/Nodes-and-Anti-nodes)波腹。通过改变速度和加速度设置，用户可以减少打印机上的这些力，直到打印出来平滑。

现在，考虑到从材料类型到月相等一系列变量，旋转立铣刀的间歇性负载大小不一，数控铣床的振动问题就变得显而易见了。

再次提到 3020 轧机，这里有一个很棒的主轴偶尔偏转和振动回零的慢动作视频。用肉眼很难发现这种行为。请记住，这种设备实际上有望达到与其他轧机相同的位置精度，但是，它经常偏离主轴上的负载超过 0.01 英寸。

 [https://www.youtube.com/embed/To9Q5pwiUXs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/To9Q5pwiUXs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



3020 上的主轴是一个铸造和轻加工的轴承箱，压配合到无刷电机外壳的前面。电机内部产生的任何振动都会直接传到零件上。此外，轧制金属板外壳没有足够的金属来提供足够的抗力。这个视频解释了这些锭子中的一些严重设计缺陷如何导致大的跳动。它还提到，有可能在大约 4 小时内破坏这些主轴，这是铣床应该预期的切割。有一个原因，大多数，但不是全部，卖方市场这些是数控雕刻机，而不是工厂。

 [https://www.youtube.com/embed/7P5THNNjafU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7P5THNNjafU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



另一台磨机有一个定制的机加工主轴箱，带有一个夹持钻头的顶尖夹头。主轴有一套适当匹配的精密滚珠轴承，这些轴承都经过适当的预加载。

通过使用皮带驱动代替直接驱动，马达与端铣刀的动作分离。这些皮带必须经过精心挑选，最终会因日常操作的热量和机械应力而磨损。这个小小的权衡(皮带便宜，容易更换)是值得的。Othermill 最近还为他们定制了一个主轴电机，比他们以前使用的 R/C 电机性能更高，噪音更小。我听说他们的新马达符合和硬盘驱动器一样的动平衡标准。

所有这些加起来就是一个安静、精确、持久的主轴，并且对于这样一个小机器来说，可以承受惊人的负荷量。这种锭子的实际跳动明显低于中国锭子的跳动。

[![Othermill Spindle Up-Close](img/3cd05c8f45f6928e12130dee1b9daaa2.png)](https://hackaday.com/wp-content/uploads/2016/05/othermill-spindle-up-close.jpg)

The bottom of the Othermill’s spindle assembly showing quite a bit more metal than the chinese spindle uses as well as the first of its paired and properly pre-loaded bearings.

## 基本框架

好吧，但是中国的工厂是铝的，另一个工厂只是一些蹩脚的塑料。铝无疑是制造工厂的优质材料。这不是真的。

Othermill 的框架由加工的 HDPE 制成。根据与它比较的铝合金，HDPE 可以比铝更坚固，同时提供许多独特的优点。

HDPE 比铝阻尼更大。所有这些微小的振动在机器中累积起来。HDPE 能够将这些振动转化为热能。相反，铝像弹簧一样刚性地传递大部分振动。这意味着机器的切割和运动的力和振荡必须去某个地方。通常这是进入机器的接头；那是端铣刀和轴承。如果处理不当，这可能导致从表面光洁度差到机器过早故障的任何事情。对于另一台轧机来说，这导致了更安静和更精确的操作。

[![A section of the precision milled HDPE frame for the othermill. ](img/4e53b30cd4c913a911471bfe5393d831.png)](https://hackaday.com/wp-content/uploads/2016/05/hdpe-frame-section.jpg)

A section of the precision milled HDPE frame for the othermill.

他们还巧妙地利用塑料的更大弹性，通过一个柔性接头来对齐光滑的杆。一根杆固定在框架中，另一根可以左右移动，但另一端不能上下移动。与机器将承受的负载相比，这实际上是一种非常坚硬的结构，可防止线性导向轴承设置可能发生的任何失准[静摩擦](http://machinedesign.com/technologies/journal-bearing-stiction)问题或过早磨损

高密度聚乙烯比铝轻得多。对于主轴托架和轧机中的其他移动部件以及轧机的便携性来说，这是一件好事。车厢越重，作用在车架上的动力就越强。对于这样一台小机器来说，中国工厂的龙门式设计正在搬运相当巨大的重量。当机器快速运行时，这将导致大量振动、噪音和更多偏转。

当然，正如在上面的主轴组件中所看到的，这里需要更坚硬的铝，其他机器公司选择了它作为材料。高密度聚乙烯会成为一个可怕的主轴外壳。它受热时膨胀过度。它偏转太多，无法准确保持方位。

HDPE 比同等的铝合金便宜。这降低了机器的成本。因为塑料更便宜，他们可以多使用一些。单就体积而言，othermill 比 3020 mill 在机架上使用了更多的材料。这使得机器的框架非常坚固、轻便且封闭。

[![A ton of complex cuts, including the flexural alignment joint, are visible in this photo. This would be prohibitively expensive to do in a metal.](img/145ff49d31a853506d8f83cd8ff16bc7.png)](https://hackaday.com/wp-content/uploads/2016/05/img_0410-2.jpg)

A ton of complex cuts, including the flexural alignment joint, are visible in this photo. This would be prohibitively expensive to do in a metal.

HDPE 不仅便宜，而且在正确设置的机器上切割起来像黄油一样。这使得他们可以进行非常复杂的切割，而这对于金属来说太昂贵了。我们稍后会看到。他们甚至可以负担得起在机器壁上切槽，以获得非常整齐的布线。

## 线性运动:

对于坚固的框架和主轴，留下来进行比较的唯一显著贡献的机械元件是各个 CNC 机器的线性运动机构。3020 轧机以偶尔在其价格范围内提供滚珠丝杠和线性导轨而闻名。然而，滚珠丝杠是一个众所周知的难以制造的物体，正如许多人所经历的那样，如果它不转动，就不值钱。

[![Othermill's linear movements from http://mikeshouts.com/othermill-pro-desktop-cnc-milling-machine/](img/7e23846b6d705e59a3a2698c512d0326.png)](https://hackaday.com/wp-content/uploads/2016/05/othermill-pro-desktop-cnc-milling-machine-image-4.jpg)

Othermill’s linear movements from [http://mikeshouts.com/othermill-pro-desktop-cnc-milling-machine/](http://mikeshouts.com/othermill-pro-desktop-cnc-milling-machine/)

3020 轧机因卖方而异。一些公司提供 ACME 丝杠，其他公司通常提供 C7 精密滚动或研磨滚珠丝杠。在如此小的轧机上增加滚珠丝杠的复杂性不一定是卖点。滚珠丝杠的一个优点，尤其是在较大的机器中，是在负载下较低的摩擦。然而，这些较大的机器具有如此大的驱动装置，并且移动的重量如此之大，以至于像螺杆的惯性以及由此产生的振动和噪音变得可以忽略不计。通常，滚珠丝杠也比 3020 研磨机更能屏蔽研磨产生的颗粒。

另一台轧机使用美国公司 [Koco motion](http://kocomotionus.com/linear-actuators/) 生产的特氟隆涂层精密轧制丝杠。与适当匹配的反游隙导向螺母配对，它们可以匹配 C7 滚珠丝杠的性能，而没有滚珠丝杠的任何复杂性缺点。特氟隆涂层消除了两者之间的大部分驱动力差异。

虽然 Othermill 和 3020 都使用圆形线性导轨，但 3020 通常使用滚柱轴承，而 Othermill 使用更昂贵的聚四氟乙烯浸渍[乙缩醛](http://hackaday.com/2016/03/03/materials-to-know-acetal-and-delrin/)衬套。当正确预加载时，这些衬套不仅一样或更精确。同样，与滚子元件相比，它们的噪音问题、磨损问题、维护和振动问题要少得多。这在下面的对比视频中可以看到。

 [https://www.youtube.com/embed/AbSU_rI82-4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AbSU_rI82-4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 电子产品:

可以很容易地假设，一个 600 美元的工厂将会有非常便宜的电子产品。所有这些工厂的电子设备都设计成在并行端口计算机上运行。因此，随着你的购买，你必须找到一个合适的旧电脑，实际运行软件，马赫 3，为这个工厂。(LinuxCNC 也是可以的。)

除了较高的功耗，较低的 PWM 频率带来的较高的噪声，Mach 3 和 Linux CNC 目前都不支持 S 曲线加速，除非进行一些严重的黑客攻击。正如[这段视频中的](https://www.youtube.com/watch?v=C0XjXqO6Ji8)所示，这对运转中的机器会有很大的影响。不仅工具上的负载更均匀，而且机器振动更小。

[![An othermill on its side. It's electronics is being assembled. Not the properly terminated wires. Also the torroids for noise. Not standard on cheaper mills.](img/b061f729f9343772db0c116352c51643.png)](https://hackaday.com/wp-content/uploads/2016/05/img_0407-3.jpg)

An Othermill on its side. It’s electronics is being assembled. Note the properly terminated wires. Also the toroids for noise. Not standard on cheaper mills.

TinyG 也是一款得到广泛支持的成熟主板。中国工厂将配备电子设备，这些电子设备已经过最严格的计数，只有最粗略的测试。在正常使用下，它们很可能会破裂。我们已经介绍了一位用户使用 3020 mill 电子设备的体验。他要做的第一件事就是彻底更换电源。它还需要一些挖掘和黑客来启用功能，如主轴转速控制，这应该已经启用。

最后，其他工厂的电气连接更可靠。3020 mills 通常需要在他们能找到的最便宜的 d in 连接器中布线和端接电线。对于铣床来说，这些都不是可靠的连接。

[![Inset wire routing with the proper bend radius for the wire ensures the long life of the Othermill's electrical connections.](img/e85725401684f2f2f0a6c33fd1d57c94.png)](https://hackaday.com/wp-content/uploads/2016/07/img_0389-2.jpg)

Inset wire routing with the proper bend radius for the wire ensures the long life of the Othermill’s electrical connections.

由于 Othermill 的目标是成为便携式机器，因此在正确布线和端接方面做了大量工作。这方面有很多工作要做。例如，如果你刚刚尝试使用标准的 Belkin 电信电缆或带状电缆用于数控机床，你会很快发现电线断断续续地断开连接([看看你的 Makerbot！](http://hackaday.com/2016/04/28/the-makerbot-obituary/))无论移动到哪里。布线必须为柔性应用而设计，否则会断裂。这需要钱，公司做了各种事情，从特殊的塑料结构和复杂的金属丝编织到在导体之间放聚四氟乙烯粉末以实现柔性电缆。

## 最后润色:

[最后一个差异是 QC](http://makezine.com/2014/09/12/meticulous-machines/) 之一。进口工厂肯定需要最终用户做一些工作，才能接近承诺的规格。我们已经看到用户做任何事情，从[替换所有的电子设备](https://hackaday.io/project/6776-3040-cnc-milling-machine-mods)到用更贵的替换[主轴。](https://www.reddit.com/r/CNC/comments/3muxkc/xpost_rhobbycnc_newbie_looking_to_buy_a_3020/)机器很可能不平整，调整其中一台机器可能相当困难。

与大多数高端/国产产品一样，Othermill 在出厂前要经过更多的测试和校准。磨机是有轨道的，床身被磨得与机器的行进方向完全一致。电子设备都检查过了，所有东西都被追踪。其他机器公司提供了中国制造商无法提供的另一种支持。

 [![Othermills waiting for testing before leaving the factory.](img/d14f12ad412937d6ad53e7e3b931bf3a.png "IMG_0376")](https://hackaday.com/2016/08/02/the-othermill-vs-import-a-technical-comparison/img_0376/) Othermills waiting for testing before leaving the factory. [![This bed did not meet the specifications and will be reworked until it is as advertised.](img/9c83007db42ad455ec6082264252d1f3.png "IMG_0391")](https://hackaday.com/2016/08/02/the-othermill-vs-import-a-technical-comparison/img_0391/) This bed did not meet the specifications and will be reworked until it is as advertised.

### 软件:

Othermill 的软件堆栈值得一提，尤其是 PCB。这是他们吹捧得最多的卖点之一。看过它的运行。它肯定能起到广告的作用，尤其是如果有人在制作电路板，它会让他们的生活变得更轻松。

 [https://www.youtube.com/embed/SuPlmSrdD6I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SuPlmSrdD6I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



然而，在常规机器工作的情况下，LinuxCNC 或 Mach3 并不*难以掌握。归根结底，拥有任何种类的 CNC 仍然需要一些技术知识和阅读文档的能力。一旦设置好了，基本上两者都很容易实现。*

## 这一切意味着什么:

[![A circle diamond square test piece off the Othermill. It is 1cm x 1cm. ](img/737c5a9fed3b3fa540b62ce237ed9da3.png)](https://hackaday.com/wp-content/uploads/2016/05/img_0425.jpg)

A tiny circle diamond square test piece in aluminum off the Othermill. It is 1cm x 1cm.

一天下来，所有这些加起来就是一台每次都以同样方式切割的机器。作为一个额外的奖励，它也将明显比其他选项更安静。当我在没有听力保护的情况下进行电路板布线操作时，我可以坐在其中一个旁边。一台制造良好的机器是耐用的；到目前为止，我在野外看到了另外四个磨坊，它们都被大量使用。他们可以精确地碾磨各种各样的材料，偶尔维护一下，在出现重大故障之前，他们应该可以使用很长时间

另一方面，进口工厂理论上可以达到与其他工厂相同的规格(从而符合他们承诺的规格)。然而，这需要大量的时间和金钱投入。

[![Othermills completely covered in dust at Maker Faire. They ran the whole time.](img/d402e25107ef2d742f08496261f994eb.png)](https://hackaday.com/wp-content/uploads/2016/05/othermillinuse.jpg)

Othermills completely covered in dust at Maker Faire. They ran non-stop the whole show.

机械工程是一个[完全不同的野兽](http://hackaday.com/2016/04/11/continuing-the-dialog-its-time-the-software-people-and-mechanical-people-sat-down-and-had-a-talk/)。有趣的是，在为这篇文章进行研究的时候，我发现我在写这篇文章之前的一些假设并没有我想象的那么正确。例如，我认为任何级别的滚珠丝杠都会比 ACME 螺纹更出色。我敢肯定，你们当中有许多人的经验和教育程度超过了我。期待评论。

* * *

免责声明:在寻找可写的东西时，我问了其他机器公司是否可以去他们的办公室。我现在没有其他工厂，也没有其他工厂给过我写这篇文章的任何好处。作为一名碰巧为 Hackaday 撰稿的在职工程师，本文中的所有观点，无论主观还是客观，都是我自己的观点。Hackaday 的商店里确实有卖 Othermill，在供应框架设计实验室里也有一个，但这与我的写作无关。我确实认为，没有人想过至少给我一袋滑稽大小的现金(当然是拒绝)以获得正面评价，这是非常无礼的。只是出于礼貌。