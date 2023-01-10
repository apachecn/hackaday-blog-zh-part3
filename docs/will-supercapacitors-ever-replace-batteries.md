# 超级电容器会取代电池吗？

> 原文：<https://hackaday.com/2017/01/19/will-supercapacitors-ever-replace-batteries/>

在几分钟内给你的手机或电动车充电听起来确实很吸引人。超级电容器技术有潜力提供电池目前无法提供的那种性能，尽管电池在不断改进，但发展速度并不是很快。请记住，你的旧诺基亚手机装有镍镉电池，使用几天后就需要充电了。今天我们有锂离子电池，我们必须每天给手机充电。显然需要更好的储能选择，超级电容器似乎是唯一接近取代电池的技术。

## 超级电容如何工作

电池以电化学形式储存能量，电池内部的反应释放电载体，形成可用的电流。超级电容器的工作原理非常不同，当相反符号的电荷彼此分开时，就会产生一个电场来储存能量。

![](img/1be17ad157ad034ad4e962eb89108db5.png)

Operation of a normal capacitor, image from [physics-and-radio-electronics.com](http://www.physics-and-radio-electronics.com/electronic-devices-and-circuits/passive-components/capacitors/supercapacitor.html).

左图显示了普通电容器的工作原理。两个导电板被电介质彼此分开。当电压施加到板上时，电子在一个板上积累，并从另一个板上耗尽(形成正空穴)。电荷的这种分离在电介质中产生了一个电场，这个电场就是能量储存的地方。一旦磁场达到最大强度，电容器就会充满电。电子被吸引到空穴中，因此，如果我们给它们一条流动的路径，就会产生电流，电容器开始放电。

![](img/7dc7f9c99eefc78ebac464feb9bb61b1.png)

Operation of a supercapacitor, image from [physics-and-radio-electronics.com](http://www.physics-and-radio-electronics.com/electronic-devices-and-circuits/passive-components/capacitors/supercapacitor.html).

超级电容器有不同的设计，如右图所示。我们还有两个通常由碳制成的电极，一个电解质和一个允许电解质中离子转移的隔板。当向电极施加电压时，正离子扩散到负极，负离子扩散到正极。电荷在每个电极表面积累，形成一个[双电层](https://en.wikipedia.org/wiki/Double_layer_(surface_science))(因此得名双电层电容器)。每个双电层都像我们之前解释过的简单电容器一样工作，但我们在每个电极上都有一个。因此，通过设计，超级电容器实际上是两个串联的电容器。

但是为什么超级电容器的电容比普通电容器的电容大呢？电容(与可储存的能量成正比)与极板面积成正比，与极板间距成反比。在普通电容器中，极板间距是电介质的厚度——大约几十微米，而在超级电容器中，该距离大约是纳米(千分之一微米)。此外，用于超级电容器电极的碳技术允许更大的表面积。其海绵状的性质使得有效面积比电极本身的面积大 100，000 倍。

## 比较电池和超级电容器

现在，电池和超级电容是一种互补，一个的优势是另一个的弱点。让我们回顾一下超级电容器和锂离子电池的关键参数:

*   充电时间:超级电容在这方面表现出色，充电时间为 1 至 10 秒，而电池充满电需要 10 至 60 分钟。
*   寿命:典型的电池有 500-1000 次充放电循环，而超级电容器可以达到一百万次循环。在车辆服务中，电池的预期寿命为 5 至 10 年，而超级电容可持续 10 至 15 年。
*   比能量:这是每单位质量的总储存能量，是超级电容器的主要弱点，平均为 10 瓦时/千克，而电池为 100-200 瓦时/千克。作为参考，我们有 3700 Wh/kg 的汽油燃料(考虑到内燃机 30%的效率)。关于单位体积的能量，超级电容器也远远落后于 15 Wh/L，电池为 1200 Wh/L。这意味着超级电容器供电的 Iphone 5 将有 2 英寸厚。
*   比功率:由于超级电容器可以快速充电，也可以快速放电，因此它们可以提供高达 10，000 W/kg 的功率。锂离子电池在 2000-3000 W/kg 的范围内。
*   成本:作为一项相对较新的技术，超级电容器仍然很昂贵，每瓦成本约为 20 美元，而电池则便宜得多，每瓦约为 0.5-1 美元。

![](img/988259abacc40c733c4d1b1e04cef2dc.png)

Charge-discharge voltage curves, by Elcap, via [wikimedia commons](https://en.wikipedia.org/wiki/Supercapacitor#/media/File:Charge-Discharge-Supercap-vs-Battery.png).

与电池相比，超级电容器还有一个额外的缺点:它们的电压随着存储的电荷近似线性地降低，而电池保持近似恒定的电压，直到它们几乎耗尽。这意味着使用超级电容时，需要额外的电路来将电压保持在可用水平，在此过程中会消耗一些能量。超级电容器的典型电压为 2.5V-2.7V，与电池一样，您可以将它们串联起来以获得更高的电压。然而，单个超级电容器之间的电容和 ESR(等效串联电阻)存在小的变化，这导致不均匀的电压分布。超级电容器过压会很快导致故障，因此需要平衡电路来确保每个超级电容器上的电压大致相同。

## 安全问题

锂离子技术有其安全问题，我们都听说过，[最近三星 Galaxy Note 7](http://hackaday.com/2016/10/14/li-ion-tech-staring-into-the-abyss-with-note-7-failure/) 的事故和[波音 s 787 梦想飞机在电池着火后于 2013 年](http://www.nytimes.com/2013/04/19/business/faa-expected-to-approve-787-dreamliner-fix.html)停飞只是两个例子。当然，鉴于市场上有数百万块电池，实际故障率非常低，因此这不是一项不安全的技术。关于超级电容器，它们的内阻比电池低得多，因此在短路的情况下，它们不会发热。当然，这项技术仍在发展中，可以带来更高容量的新材料和方法也可能增加风险，但截至今天，我们可以说超级电容器比锂离子电池更安全。

## 我们什么时候能有超级盖头的 iPhone？

超级电容器已经有几个利基应用，估计有 4 亿美元的世界市场。内存备份和保护是最早的应用之一，也是为电子玩具供电。它们也用于太阳能电池阵列和微型能量收集系统。在储能领域的高端，超级电容用于混合动力电动汽车的再生制动和提供启动电源。电网也可以从中受益，使用超级电容器组作为电涌的缓冲，输电线路可以接近 100%的容量运行，从而提高效率。

所有这些都是好消息，超级电容器已经开始承担一些传统上分配给电池的角色。但超级电容在存储方面仍落后于电池。新的技术进步，如石墨烯和其他化合物的使用，可能会在不久的将来增加容量，使超级电容器成为取代电池的真正选择。就目前而言，制造成本仍然很高，物理尺寸意味着即使你愿意在价格上挥霍，你仍然无法找到一个合理的替代品来取代今天的锂离子电池手机。也许智能手机的下一个趋势将是回归砖块设计，为超级电容器利用其快速充电和长使用寿命腾出空间。在那之前，我们要等待制造技术的进步，让更大的盘子能装进更小的空间。