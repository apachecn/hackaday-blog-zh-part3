# Hackaday 奖参赛作品:开源静电纺纱机

> 原文：<https://hackaday.com/2016/05/21/hackaday-prize-entry-open-source-electrospinning-machine/>

静电纺丝是一个迷人的过程，其中在导电发射器喷嘴和收集器筛网之间施加高电压电势。然后聚合物溶液从喷嘴中缓慢分配。溶液中负电荷的排斥迫使细纤维从液体中散发出来。然后，这些纤维在电场的作用下迅速加速向收集屏移动，同时被拉伸并变细到直径只有几百纳米。细小纤维的大表面积使它们在飞向收集器筛网的过程中变干，在那里它们形成细小的织物状材料。我们注意到，静电纺丝有望在未来实现可穿戴纺织品的全自动制造。

[道格拉斯·米勒]已经有了烹饪小批量微小纤维的经验。他已经在他的微波炉里制造了碳纳米管。下一步是在 [低成本、开源的静电纺纱机](https://hackaday.io/project/10599-electrospinning-machine)中将这些纳米管转化为材料和织物，这是他的 Hackaday 奖参赛作品。

和基础研究项目一样，很多参数都必须调整到合适的程度。为了加快寻找合适的电势值、定量给料速率、发射器到收集板的距离、温度和湿度值的过程，[Douglas]用 CNC 控制的垂直轴和注射泵建造了他的机器，该机器甚至可以精确地分配最小量的给定溶液。随着项目的进展，将增加温度和湿度控制。主机软件和图形用户界面允许轻松控制所有参数，并且一旦一切都拨入，还将保存和调用不同纺丝解决方案的预设。[Douglas]已经进行了一些测试，从一个旧的 3D 打印机喷嘴喷射盐溶液，我们很快就可以期待从他安装的更合适的注射器喷嘴中使用聚合物溶液进行第一次测试。

[![Electrospun fabric, image source](img/fa8f5c0e05b830b5978534f060efb337.png)](https://hackaday.com/wp-content/uploads/2016/05/electrospun_pcl.png)

Electrospun fabric, [image source](https://en.wikipedia.org/wiki/Electrospinning#/media/File:Electrospun_pcl.png)

为了让其他制造商能够负担得起，并易于复制，[道格拉斯]利用现有的材料，想出了一些也可以应用于其他项目的设计技巧。皮带驱动的垂直轴基于 PVC 管，3D 打印的衬套块在其上上下滑动，调整喷嘴和收集器板之间的距离。带有安全开关的丙烯酸门防止聚合物喷雾从纺丝室中逸出。在机器的中心有一个带 gShield 的 Arduino Uno，它控制步进电机并与主机通信。3D 打印注射泵是一种定制设计，从机器的侧面向外摆动，便于重新灌装。浸没在矿物油中的半波串联电压倍增器可以将交流电源的电压提升到最大 30 千伏 DC，矿物油可能是为了降低过热和电弧的风险而选择的。

 [https://www.youtube.com/embed/6z_SGMO6fVU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6z_SGMO6fVU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)