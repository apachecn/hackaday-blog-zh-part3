# 一个疯狂科学家的自制电容器

> 原文：<https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/>

从前我是一个真正的疯狂科学家。我对非常规推进很感兴趣，我的想法是以某种方式与量子真空波动，零点能量场相互作用。尽管我对那是什么只有模糊的理解，也没有考虑到任何人所说的在宏观尺度上与它互动是多么不太可能或不可能，我还是投入了进去。但我们都必须来自某个地方，这就是我对高压和自制电容器世界的介绍。

在此过程中，我制作了一些非常有趣或与众不同的电容器，我将在这里讨论。

## 大型蜡制圆柱电容器

正如照片所示，这个电容器相当大，看起来像是夹在两个木盘之间的厚厚的一大块石蜡。在内部，导线连接到两个铝制防水盘，这是间隔 2.5 厘米(1 英寸)的电容器极板。但在它们之间，电介质由七个以上的铝制防水盘组成，由浸在更多石蜡中的普通棉片隔开。看，我告诉过你这些电容器是不同的。

 [![Big wax cylindrical capacitor](img/090e701217027b4616759e5b3233f1b5.png "Big wax cylindrical capacitor")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/big_wax_cylinder_capacitor_01_top_view_cr/) Big wax cylindrical capacitor [![Exposed wax of the capacitor](img/05d2eab64d9231c7cad965d362ed484c.png "Exposed wax of the capacitor")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/big_wax_cylinder_capacitor_03_showing_wax_cr/) Exposed wax of the capacitor [![The experiment and the capacitor's interior](img/9c113c0a85c53c1702e1bc29994e90de.png "The experiment and the capacitor's interior")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/8_inch_cylindrical_capacitor/) The experiment and the capacitor’s interior

我不会去探究建造背后的推理——这都是瞎猜的想法，有希望、独角兽毛做后盾，实际上没有任何理论。有趣的是实验本身。成功了！

我把电容器放在一根直径为 4 英寸的高 ABS 管上，这根管又放在地板上的电子秤上。几十千伏的高压通过厚厚的绝缘导线加在电容器上。电源在高压侧包含一个回扫变压器和[科克罗夫特-沃顿电压倍增器](http://hackaday.com/2012/02/10/cockroft-walton-multiplier-can-output-positive-or-negative-voltage/)。当我调高电压时，磅秤显示重量在减少。我减肥了！

但是经过几个小时的极性反转和电容器翻转，并做了大量的笔记，我找到了原因。重量损失仅发生在如图所示顶部一根向下输送的情况下，但是当顶部一根水平输送时，重量没有变化。我以前见过高压线移动，现在它又出现了，在秤上产生了看起来像体重减轻的效果。

但这只是我制作的有趣电容器之一。休息后，我们进入引力子，多硫化物，甚至钛酸钡。

## 引力子

重力电容器是由 T . Townsend Brown 发明的，用于控制重力，并在英国专利 GB300，311 中有所描述。我的实现是一个 30 厘米(12 英寸)长的 Bondo 树脂块，中间有两个铝电极板和 29 个均匀间隔的隔离板。在其中一张照片中，你可以看到它正在建设中。它由两部分组成，每一部分都有一个白色的塑料模具，模具中加入了一个盘子和树脂。然后树脂硬化，模具升起，然后加入更多的板和树脂，如此循环，直到每块板的长度是最终电容器的一半。然后用更多的树脂将它们粘在一起，制成你在测试装置的照片中看到的一个长条。

 [![Gravitator as a pendulum](img/a149ba87a5dac92648a92c79708769b5.png "Gravitator as a pendulum")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/grmk2_pendbigpic_an/) Gravitator as a pendulum [![The two gravitator molds](img/043104d3d945b1648d195d457929908d.png "The two gravitator molds")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/grmk2_startingclose_an/) The two gravitator molds [![Gravitator internals](img/e51a255e17e7120cf4a9870dd6b330cc.png "Gravitator internals")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/gravitator_internals/) Gravitator internals

这次测试是水平的，重力仪像钟摆一样悬挂着。没有检测到任何移动。然而，通常在进行该测试时，一根或两根馈线是具有薄搪瓷涂层的小直径线，即电磁线。在这些电压下，珐琅质很容易分解，电离到空气中，就像一股喷射流，产生某种形式的推进力。当我们谈到被称为升降机的自制飞行器时，我们以前见过这种类型的离子推进。

这种运动通常很小，但实验者通常会根据运动的时间开关电源，就像一个荡秋千的人拉绳子并在合适的时间摆动双腿一样，产生共振。结果是一个大的运动，但与重力控制无关。在我的例子中，你可以看到我使用绝缘足够厚的馈线来避免击穿，所以我没有移动。

## 多硫化物

在这些非常规推进实验中，一个被认为是有益的特征是具有高 K 电介质，即具有高相对介电常数的电介质。当时有人发现多硫化物的 K 值为 2260，非常高。对于大多数材料，K 值低于 10。我设法找到了一种名为 Deck-O-Seal 的聚硫密封剂，这是一种用于游泳池周围水泥接缝的液体塑料填料。图表和照片显示了我的想法。

 [![Polysulfide high K capacitor - Front view](img/16e2b96d3f126d4b70867ea57f0b4684.png "Polysulfide high K capacitor - Front view")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/hk1bfrnt/) Polysulfide high K capacitor – Front view [![Polysulfide high K capacitor - Top view](img/f0d537981c1b72f2300c96ef7960b3b5.png "Polysulfide high K capacitor - Top view")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/hk1btop/) Polysulfide high K capacitor – Top view [![Polysulfide high K capacitor interior](img/4a568d80e93ad7d2cc547fb5667c390d.png "Polysulfide high K capacitor interior")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/polysulfide_dielectric_capacitor/) Polysulfide high K capacitor interior

最初，黄铜丝浸在聚硫化物中，整个东西悬挂在转子臂的末端。但是在施加高电压的情况下，没有运动。通过进一步的研究，我发现聚硫化物产品可能含有导电材料，所以我将黄铜丝从聚硫化物中取出，希望空气可以充当绝缘体。这一次，我在电线的两端得到了电离，其形式是蓝色的电晕和嘶嘶声。和上面引力子的馈电线一样，这产生了一个喷射，导致了一点点运动。但同样，我是在运动之后，由于与量子真空波动的相互作用，所以我放弃了那个。

## 钛酸钡

然而，我坚持寻找高 K 电介质，并设法从大西洋设备工程师公司找到了纯度为 99.9%的钛酸钡粉末(如果你想要的话，产品编号为 BA-901)。如果温度合适，电场强度合适，电场方向正确，钛酸钡的 K 值可以达到数千。

 [![Barium titanate powder](img/2570c8d890e9acb4c36067ee1253b1df.png "Barium titanate powder")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/batio3_aee_can/) Barium titanate powder [![Barium titanate and wax in a mold](img/23be1683e820829ebf7188656c31463e.png "Barium titanate and wax in a mold")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/batio3wax1_inmold/) Barium titanate and wax in a mold [![Measuring the capacitance](img/9f5561f8e502a26108cc430ec551b42f.png "Measuring the capacitance")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/batio3wax1_measuring_c_10/) Measuring the capacitance

但是问题是把白色粉末变成没有空气的固体电介质。一种方法是在高温下压缩它，或者烧结它，但是我没有办法做到这一点。取而代之的是，我尝试混合石蜡作为粘合剂，因为我知道这样得到的介电常数会比纯钛酸钡低。我得到的最好结果是 12.5 到 18.6 的相对介电常数。

 [![Barium titanate/epoxy capacitor making setup](img/7f37621027153ec331cc59c756a289e7.png "Barium titanate/epoxy capacitor making setup")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/s_100415_batio3_eagerepoxy_k15_setup/) Barium titanate/epoxy capacitor making setup [![The mix with small balls](img/749afc983654f8d48a549d68a81e68bd.png "The mix with small balls")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/100612_batio3_epoxy_mix/) The mix with small balls [![Barium titanate/epoxy capacitor](img/615bcf2784c6a4cd6ea4961647fdec4c.png "Barium titanate/epoxy capacitor")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/diy_barium_titanate_capacitor/) Barium titanate/epoxy capacitor

然后我试着用环氧树脂作为粘合剂。通过大量的实验，我得到了最好的结果，将树脂和钛酸钡以这样的比例混合，我得到的球大部分直径为 1 毫米或更小，如图所示。我当时追求的电容器是圆柱形的。我用了 1/4 英寸直径的铜棒作为中心电极，铝网作为外部电极。我用两片纵向切开的塑料管做了一个模子，铜棒穿过中心。我一次倒入一点钛酸钡和环氧树脂的混合物到模具中，当它还很软的时候，轻轻敲打它。对于 86 重量%的钛酸钡，我得到 27 的 K 值。这是我用这种方法所能做到的最好的结果，但并没有像我希望的那样达到数百或数千个。然而，与 K 值通常约为 2 或 3 的普通树脂或蜡制电容相比，它仍然令人印象深刻。

## 双介质电容器

但是钛酸钡并不是我最有野心的一个。这个荣誉属于一个圆柱形电容器，它的电介质实际上是两个分开的部分，沿着中心延伸。一块由环氧树脂制成，另一块由石蜡制成。我们对尺寸和材料进行了全面的计算，以符合一个理论产生的假设，当然这意味着我不能只使用我手头的任何东西。正如你所看到的，我不仅用蜡填充了电容器内部的一半，还把整个电容器外部都包了起来。

 [![The capacitor with epoxy only](img/21fe2a890ff98ab414223f90c559420e.png "The capacitor with epoxy only")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/cons5_bare_thruster_3_an/) The capacitor with epoxy only [![Two-dielectric capacitor test setup](img/1f7385757b2ad996dcf73ab7e8b5bacf.png "Two-dielectric capacitor test setup")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/cons5_bad_exp_foil_1_an/) Two-dielectric capacitor test setup [![Two-dielectric capacitor with card on top](img/a4c34a3e5ecc4acb7ed78c5df9f57f48.png "Two-dielectric capacitor with card on top")](https://hackaday.com/2016/10/03/homemade-capacitors-of-a-mad-scientist/cons5_bad_exp_foil_3/) Two-dielectric capacitor with card on top

当电容器的蜡片朝上时，应该会有一个向上的净推力。测试是在数字秤和三重天平上进行的，但重量没有变化，然而轻轻放一张扑克牌在上面会产生重量变化。如您所见，为了屏蔽目的，秤完全被接地铝箔覆盖。在电容器内部出现火花之前，电压仅为 8kV，但这足以检验假设。这个理论被发现是错误的。

## 结论

因此，虽然我没有得到我所追求的推进类型，但我确实对高压、电容器、新的施工技术有了很好的了解，并在这一过程中获得了很多乐趣。你自己有没有做过任何新奇的电容器或者非常规的推进实验？让我们在下面的评论中了解他们。如果你倾向于坚持更传统的观点，从我们关于[关于商用电容器](http://hackaday.com/2016/06/21/capacitors-made-easy-the-hackaday-way/)的文章中可以学到很多东西。