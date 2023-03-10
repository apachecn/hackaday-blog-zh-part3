# 丰富的高压电源

> 原文：<https://hackaday.com/2016/05/26/a-cornucopia-of-high-voltage-sources/>

多年来我一直在研究高压，结果我使用了大量不同的高压电源。我说来源而不是电源，因为我甚至通过用棉布摩擦 PVC 管，利用摩擦电效应为电晕马达提供动力。但是，尽管电压很高，但电流太低，无法产生必要的离子风来使[升降机飞离桌面](http://hackaday.com/2009/12/08/ionocraft-aka-lifters/)。为此，我使用反激式变压器和插在墙上插座的科克罗夫特-沃顿电压倍增器电源。

所以，是的，我有一套非正统的技能来获得高电压。是时候我坐下来列出我这些年来用过的大多数电源了，包括它们是如何工作的，它们的输出是什么样的，它们可以用来做什么，以及一些成本或制作简易性的想法。顺序是从最弱到最强，所以继续读那些真正有说服力的。

## 摩擦电效应

![Triboelectric series table](img/caeef956734cd96cd5a0e192d94673f3.png)

Triboelectric series table

你肯定遇到过这种情况。这就是当你的脚在地毯上摩擦，然后碰到门把手而受到电击时，你的身体是如何充电的。当你把两种特殊的材料放在一起摩擦时，电子会从一种材料转移到另一种材料。不是任何两种材料都能起作用。要了解哪些材料适合使用，请查看[摩擦电系列表](https://en.wikipedia.org/wiki/Triboelectric_effect#Triboelectric_series)。

当桌子正端的材料与桌子负端的材料摩擦时，会带正电。这些材料将带负电。它们在表中的距离越远，电荷越强。

![Powering corona motor with triboelectricity](img/065731896b23cd9013d1058e9bb1bcaf.png)

Powering corona motor with triboelectricity

我使用它的一个例子是给这里显示的电晕电机供电。我用棉布使劲摩擦一根 PVC 管，当管子从棉布中露出来时，几毫米外的一根尖锐的电线从管子中带走了电荷。你可以在视频中看到这个[电晕电机由其他电源供电](http://hackaday.com/2014/08/09/funky-looking-motor-is-powered-by-static-electricity/)。

这被认为是静电电源，因为电荷在表面上积累。由于是绝缘材料，电荷不能四处移动。

单位时间内在材料之间转移的电荷量很小，这意味着可用的电流很小。你不会用这个来驱动任何重负载，但这种方式驱动的电晕电机每 5 秒钟旋转一周，手指轻轻一碰就可以停止。你已经感受到了触摸门把手时轻微电击的力量。这当然是一种容易制造的能源。

## 威姆斯特机器

![Wimshurst machine - parts and demo](img/04b515e9f06e284a62ae25c7a7843f03.png)

Wimshurst machine – parts and demo

Wimshurst 电机也是高电压/低电流电源。它由两个反向旋转的圆盘组成，通常用手摇曲柄旋转。磁盘上有间隔开的金属扇区。当它们经过时，充电发生在中和器刷接触扇区的地方。这些电荷随后在圆盘左右边缘的收集器处被移除，通常积聚在莱顿瓶(电容器)中，并穿过火花隙，当电压足以击穿间隙中的空气时，火花在火花隙中产生。

![Wimshurst machine and ball cyclotron](img/e580b7e39b79fab8df7706e1bed2fc78.png)

Wimshurst machine and ball cyclotron

但是如果你使用 Wimshurst 机器，你通常不会产生火花。在照片中，你可以看到电线从 Wimshurst 机器连接到[一个球回旋加速器](http://hackaday.com/2015/10/14/hand-cranked-cyclotron/)，使里面的球在碗内旋转。

这个的电压受限于莱顿瓶和火花隙中的损耗以及负载。这就是为什么要努力让一切都变得全面。火花隙也限制了电压，用这个我产生了大约 3 英寸/7 厘米长的火花。

电流间接地由圆盘的直径决定。这是因为较大的选择器会比较小的扇区产生更多的电荷。此外，磁盘转动得越快，每秒经过收集器的扇区就越多，因此可以获得更多的电荷。

一台 Wimshurst 机器不能提供足够的电流使一个升降机飞行。然而，它确实提供了足够的电流[来驱动烟尘净化器](http://hackaday.com/2014/03/13/cleaning-up-smoke-with-an-electrostatic-precipitator/)。

它们并不难制作。我发现最棘手的部分是找到或制造将手摇曲柄旋转传递给圆盘所需的滑轮。光盘可以是丙烯酸的，你可以用线锯或激光切割机切割，通常小型 Wimshurst 机器是用 CD 制作的。

## 范德格拉夫发电机

![Van de Graaff generator parts](img/7294cb8cdaa74731fa58a9dec630c343.png)

Van de Graaff generator parts

从外面看，范德格拉夫发电机看起来像一个大球，或圆顶，在垂直管的顶部，在管的底部有更多的东西。虽然穹顶是中空，但管子内部是一个带滚轮的带子。管子底部的东西包括一个转动滚筒和传送带的马达。带的外表面通过我们上面提到的相同的摩擦电效应和附近的一些尖锐的刷子来充电。该电荷被转移到圆顶的外表面。

圆顶上可积聚的电荷量仅受其直径的限制。直径较小的圆顶可以被认为是比直径较大的圆顶更尖锐的物体。更尖锐的物体周围有更强的电场，更容易分解空气，从物体上带走电荷。图中的大 Van de Graaff 额定电压约为 400kV，小 Van de Graaff 额定电压约为 80kV。

![Big and small Van de Graaff generators](img/803531dd643b7c9e9acee13ba1604fa8.png)

Big and small Van de Graaff generators

它们仍然是低电流源，因为电流是由皮带和辊子的摩擦电效应产生的，并通过皮带的运动进行机械传输。更宽的皮带和滚筒以及更快的转速可提供更高的电流。

它们是中等难度的。由于涉及摩擦电效应，辊子和皮带必须是正确的材料组合。小的圆顶通常是汽水罐，大的圆顶通常是用金属沙拉碗或 T2 大花园球做成的。

## 回扫变压器

![Flyback single transistor schematic](img/ee98b861abbd8177da7618870eb9acf8.png)

Flyback single transistor schematic

转到更高电流的电源，一种常用的类型是使用回扫变压器和一个或多个晶体管的电路。正如所料，反激式变压器的初级绕组会在次级绕组中感应出电流。然而，还有一个反馈绕组，它同时关闭晶体管，阻止电流流向初级线圈。这导致磁场崩溃，并在次级出现一个大的高压尖峰。由于反馈线圈上不再有电流，晶体管再次导通，循环重复。

存在一种类似的使用 MOSFETs 的电路，称为 ZVS 反激式驱动器，但由于我没有制作过，所以我会让你参考[这个电路用于制作 smores](http://hackaday.com/2013/08/26/making-smores-with-50000-volts/) 。

 [![Flyback PSU and arcing corona](img/87e1adf742d370c178a833b511f49dc0.png "Flyback PSU and arcing corona")](https://hackaday.com/2016/05/26/a-cornucopia-of-high-voltage-sources/cube_flyback_and_arcing_corona/) Flyback PSU and arcing corona [![Flyback transformer with built in diodes](img/62e7954f669575d1f8fafa653195017b.png "Flyback transformer with built in diodes")](https://hackaday.com/2016/05/26/a-cornucopia-of-high-voltage-sources/flyback_builtin_diodes_blue_bkgd_an/) Flyback transformer with built in diodes

回扫变压器可以在网上购买，但也可以从旧的 CRT 电视和 CRT 电脑显示器中回收。它们通常在次级绕组输出后内置高压二极管，这意味着输出是 DC。

我把我的放入上面显示的小立方体中。你可以从中看到漂亮的连续弧线。我还为一架[雅各布之梯](http://hackaday.com/2015/03/05/11000-volt-jacobs-ladder-sounds-like-a-lightsaber/)提供动力。矿山产生了约 20kV 的高电流输出。

## 回扫变压器加科克罗夫特-沃顿电压倍增器

如果你足够幸运，找到一个像这里所示的没有内置二极管的反激式变压器，那么在输出端[你可以添加一个科克罗夫特-沃顿电压倍增器电路](http://hackaday.com/2013/09/23/homebuilt-30kv-high-voltage-power-supply/)。该倍增器由电容和二极管组成，可接受反激式交流输出并将其平滑为平坦的 DC，同时在一定数量的级上倍增电压。级数仅仅取决于你增加的电容和二极管的数量。每增加一级都会增加输出电压。

 [![Flyback driver with voltage multiplier](img/9cc13bc45778945d0576198591ac69f7.png "Flyback driver with voltage multiplier")](https://hackaday.com/2016/05/26/a-cornucopia-of-high-voltage-sources/flyback_with_voltage_multiplier/) Flyback driver with voltage multiplier [![Flyback transformer with no built in diodes](img/afc97a7e8dd62d183befc711b2275b6a.png "Flyback transformer with no built in diodes")](https://hackaday.com/2016/05/26/a-cornucopia-of-high-voltage-sources/flyback_transformer_with_just_coil_and_core_cr/) Flyback transformer with no built in diodes

电压将被升高，但是电流将比没有倍增器时低。尽管如此，它仍然很高，高到足以提供足够的电离使升降机飞行。

你可以自己制作倍增板，也可以购买倍增板。你可以买到的通常被称为三倍，因为他们有三个阶段。他们将把 20 千伏的输入电压提高到 30 千伏，也足以让升降机飞行。

![Voltage multiplier PSU flying a lifter](img/790712945a97b6bb2372539cd75301c2.png)

这些类型电源的一个几乎现成的来源是[使用一个旧的 CRT 电脑显示器](http://hackaday.com/2014/06/14/repurpose-an-old-crt-computer-monitor-as-a-high-voltage-science-project-power-supply/)。只需拆除进入阴极射线管的高压电线，并使用该电线。我发现长火花会很容易损坏这些显示器，所以一定要包括大约 240 千欧的至少 2 瓦额定电阻与输出串联。

这些是我有经验的有趣的高电压源。但我很想在下面的评论中听到你自己的高压黑客。我也喜欢听到关于使用或制造高压电源的问题或想法，所以不要害羞。