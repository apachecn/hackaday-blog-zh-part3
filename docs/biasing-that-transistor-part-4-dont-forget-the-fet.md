# 偏置晶体管第 4 部分:不要忘记场效应晶体管

> 原文：<https://hackaday.com/2018/06/08/biasing-that-transistor-part-4-dont-forget-the-fet/>

[![The 2N3819 is the archetypal general-purpose N-channel FET. (ON Semiconductor)](img/5e17be2fe24c6a8092d1478ccda69b24.png)](https://hackaday.com/wp-content/uploads/2018/06/2n3819-datasheet.jpg)

The 2N3819 is the archetypal general-purpose N-channel FET. ([ON Semiconductor](https://www.onsemi.com/pub/Collateral/2N3819-D.PDF))

最近几周，在 Hackaday，我们一直在观察不起眼的晶体管。这个系列的动力来自于一位朋友，他的学生带着高度发达的微控制器知识，却对基本的电子电路知之甚少，在这个系列中，我们研究了双极晶体管的所有配置。然而，如果不承认双极晶体管只是故事的一部分，就不应该结束这个系列。还有另一类晶体管，其电路结构与双极晶体管相似，但工作方式完全不同:场效应晶体管，简称 fet。

从某种意义上说，用我们研究双极晶体管的方式来研究场效应晶体管不太合适，因为虽然它们是非常有趣的器件，可以为电子器件的许多功能供电，但作为分立器件的情况却少之又少。你所接触的每一个 CMOS 器件的工作都依赖于场效应晶体管，你随意抛出信号的每一个高质量运算放大器都是通过场效应晶体管输入端来实现的，但这些场效应晶体管都埋在芯片内部，如果我们没有告诉你，你很难知道它们的存在。如果需要高阻抗音频前置放大器或低噪声 RF 放大器，您可以使用 FET，FET 是高电流开关应用的良好选择，但遗憾的是，您可能永远不会像双极性等效电路那样拥有大量通用 FET。

也就是说，FET 是一种迷人的器件。请加入我们，让我们深入了解他们的操作，以及如何和在哪里使用他们。

## FET basics

[![A diagram of an n-channel JFET. As the negative gate voltage on the p-type silicon decreases in the lower diagram, its electric field restricts the area through which electrons can flow in the n-type channel. Chtaube,(CC BY-SA 2.0 DE)](img/ae2c91cce600401b98c689958f16d669.png)](https://hackaday.com/wp-content/uploads/2018/04/jfet-chtaube0504131.png)

A diagram of an n-channel JFET. As the negative gate voltage on the p-type silicon decreases in the lower diagram, its electric field restricts the area through which electrons can flow in the n-type channel. Chtaube,([CC BY-SA 2.0 DE](https://commons.wikimedia.org/wiki/File:Jfet-chtaube050413.png))

基本 FET 有三个端子，源极(电子源)、栅极(控制端子)和漏极(电子离开器件的地方)。它们类似于双极晶体管的端子，因为源极相当于发射极，栅极相当于基极，漏极相当于集电极。因此，三种基本的双极晶体管电路配置与 FET 具有等效性；共发射极变成共源极，共基极变成共栅极，射极跟随器变成源极跟随器。然而，将双极晶体管和场效应晶体管之间的类比延伸得太远是危险的，因为它们的工作模式不同。如果有帮助的话，场效应管和三极管之间有更相似的地方。

用于演示目的的最简单的 FET 有一块 N 型半导体，在相对的两端有源极和漏极连接，在中间淀积一个 P 型半导体区。这被称为 N 沟道结 FET 或 JFET，因为电流流经的沟道是 N 型半导体，并且因为在栅极和沟道之间存在二极管结。有等效的 P 沟道器件，就像有 PNP 和 NPN 双极晶体管一样。

如果像对栅极施加正偏压的双极晶体管一样对 n 沟道 JFET 施加偏压，则栅极和源极之间的二极管将导通，晶体管将仍然是具有两个阴极端子的二极管。然而，如果你给栅极一个相对于源极的负偏置，二极管就会反向偏置，没有电流流入栅极。

反向偏置二极管的一个特点是在阳极和阴极之间有一个耗尽区，在这个区域中没有电子。这就是导致二极管不再导通的原因，耗尽区的大小取决于存在于其上的电场的大小。如果你曾经使用过变容二极管，这个可变宽度区域两边的电容就是你正在利用的特性。

在 FET 中，耗尽区从栅极区延伸到沟道中，并且由于它的尺寸可以通过栅极电压来调节，所以它可以用于“收缩”沟道内的剩余导电区。因此，电子可以流过的面积由栅极电压控制，因此在漏极和源极之间流动的电流与栅极电压成比例。我们有一个放大器。

[![A simple FET radio receiver circuit showing FET biasing. The gate is biased at ground potential through the inductor, and the source is held above ground by the current in the 5K resistor. Herbertweidner [Public domain].](img/c1b3a13515bb736dc82f8977e1b1f463.png)](https://hackaday.com/wp-content/uploads/2018/06/1kreiser_mit_fet.png) 

显示 FET 偏置的简单 FET 无线电接收机电路。栅极通过电感偏置在地电位，源极通过 5K 电阻中的电流保持在地电位以上。Herbertweidner [ [公共领域](https://commons.wikimedia.org/wiki/File:1kreiser_mit_FET.png) ]。

在上面的 JFET 图中，负的栅极偏置用电池来表示。电子管发烧友可能遇到过从电源获得负栅极偏置的设备，您会发现电子管电源单元包括用于此目的的-150 V 电源轨。一般来说，即使电压较低，这在 FET 电路中也是不方便的，因为负调节器的额外成本..取而代之的是，通过仔细选择源电阻，使得流经源电阻的电流将源极带到地电位以上，并且通过栅极偏置电路将栅极保持在接近地电位，从而将栅极保持在比源极低的电位。由于这个原因，双极电路的基极电阻链通常用单个接地电阻或具有极低 DC 接地电阻的门电路(如电感)来代替。

## MOSFETs，FET 变得更加有用

[![Internal structure of an N-channel MOSFET. Fred the Oyster [Public domain].](img/cc7512e29add3c3856a05de695ef0430.png)](https://hackaday.com/wp-content/uploads/2018/04/n-channel_mosfet-svg1.png)

N 沟道 MOSFET 的内部结构。牡蛎弗雷德[ [公有领域](https://commons.wikimedia.org/wiki/File:N-channel_mosfet.svg) ]。我们所描述的 JFET 是最简单的场效应器件，但它不是你最常遇到的。MOSFETs 是金属氧化物半导体 fet 的缩写，具有类似的源极、栅极和漏极，但它们不依赖于反向偏置二极管中的耗尽区，而是具有一层薄薄的绝缘层。来自栅极的电场作用在绝缘层上，通过电子的排斥来挤压沟道中的导电区域，其效果与在 JFET 中的效果相同。深入探讨它们的机制超出了本文的范围，但是您会遇到两种类型的 MOSFET: *耗尽型*器件，它们需要与 JFET 相同的负偏置，以及*增强型*MOSFET，它们需要正偏置。

## 为什么要使用 FET？

我们已经描述了 FET，并注意到虽然它的工作模式与双极晶体管不同，但它的工作方式基本相似。那么，我们为什么要使用 FET 呢？它能给我们带来什么好处呢？答案来自于栅极被 JFET 中的耗尽区或 MOSFET 中的绝缘层所绝缘。FET 是电压放大器，而不是电流放大器，其输入阻抗比双极性晶体管高许多数量级，因此您会发现 FET 用于许多需要高阻抗小信号放大器的应用中。例如，高性能运算放大器的输入几乎肯定是 FET。

[![This half-bridge power MOSFET driver circuit uses a specialist gate driver IC with a pair of Schmidt buffers to deliver the initial surge required for a fast-turn-on time. Wdwd (CC BY 3.0).](img/0076b028a64b40f12a72eacc1035aa55.png)](https://hackaday.com/wp-content/uploads/2018/06/bootstrap_half-bridge-svg.png)

This half-bridge power MOSFET driver circuit uses a specialist gate driver IC with a pair of Schmidt buffers to deliver the initial surge required for a fast-turn-on time. Wdwd ([CC BY 3.0](https://commons.wikimedia.org/wiki/File:Bootstrap_Half-Bridge.svg)).

高输入阻抗的另一个影响与小信号工作的耦合度较低。双极晶体管需要很大的基极电流来导通，而相应的 FET 几乎不需要基极电流。因此，几乎所有复杂的集成电路逻辑器件都是基于 FET 的，而不是双极的，因为不需要提供数千个双极晶体管的基极电流需求就可以节省大量的功率。

同样的效应也会影响用于功率开关的 FET 的选择，而双极性晶体管的基极电流与其集电极电流成比例，因此需要一个有效的驱动器，相比之下，功率 MOSFET 在初始浪涌之后几乎不需要稳定的栅极电流。因此，与相应的双极性开关相比，MOSFET 功率开关所需的驱动电子器件更少，效率更高，并使一些可能用于驱动 3D 打印机或多转子电机的微型驱动板成为可能。

通过本系列课程，您应该已经掌握了基本双极晶体管原理的坚实基础，现在您应该能够将 fet 添加到该知识库中。在之前的一篇文章中，我们建议您购买一袋 2N3904s 进行实验，现在我们可以建议您购买一袋 2N3819s 吗？