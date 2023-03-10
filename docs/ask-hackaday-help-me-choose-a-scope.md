# 问黑客日:帮我选择一个范围

> 原文：<https://hackaday.com/2016/09/20/ask-hackaday-help-me-choose-a-scope/>

如果有一种仪器可以作为电子工程师的工作台，那就是示波器。在时域中跟踪电压并测量其周期和幅度的能力类似于黑暗中的一盏灯，它将一个仅仅修补电路的人变成了一个控制电路的人。简单的附加电路可以将基本示波器转变为曲线跟踪器、频率响应显示器等，现代示波器提供了一系列令人眼花缭乱的有用测量功能，仅在几年前工程师还无法想象。我需要你帮我选一个新的。

[![They don't make 'em like they used to! My Cossor portable oscillograph.](img/a436bdc4c5ca6f42ef9177d9e9dcdc67.png)](https://hackaday.com/wp-content/uploads/2016/09/cossor-front-panel.jpg)

They don’t make ’em like they used to! My Cossor portable oscillograph.

## 现状

我的第一台示波器是在 20 世纪 80 年代初我的学校清理实验室时得到的。这是一个双光束 Cossor，可能来自 20 世纪 50 年代，它自豪地拥有 2MHz 或者我应该说“2 Mc/s”！–带宽。制造商的盘子称它为“便携式示波器”，因为它的顶部有一个手柄，如果你是一名举重运动员，你可以带着它走一段距离。为了这篇文章，从车库的角落里掸去灰尘，让我想起了所有那些由旧电视零件拼凑而成的电路，想起了亲眼目睹 PAL 彩色脉冲的奥秘，想起了我自制的光谱分析仪。

Cossor 显然不适合电子工程专业的学生，所以大约在 1990 年的某个时候，我去了雷丁书店的阿拉丁洞穴，买了一个 70 年代中期的廉价古尔德双扫描望远镜。它有 20 兆赫兹的带宽，从那以后一直是我的忠实伙伴。这是那个时代的典型日常观测仪器，因为像它这样的观测仪器现在比啤酒钱多一点就能找到，我会毫不犹豫地向任何寻找基本测试设备的人推荐一台。

四分之一世纪后，我有了一个“范围问题”。作为一个业余无线电爱好者，我总是与古尔德的低带宽搏斗。它也不是最小的仪器，现在新的望远镜能做的事情的数量是我不能忽视的。我该买一个新的望远镜了，这就是你的用武之地。

## 选择，选择

[![If I held my finger over the badge, would you be able to distinguish it from its competition? Image: SIGLENT TECHNOLOGIES CO.,LTD [PD], via Wikimedia Commons](img/cb8582ec96b68c7a2367f60c2923fa31.png)](https://hackaday.com/wp-content/uploads/2016/09/siglent_sds1304cfl.jpg) 

如果我把手指放在徽章上，你能把它和它的竞争对手区分开来吗？Image: SIGLENT TECHNOLOGIES CO .，LTD [PD]，via[Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Siglent_SDS1304CFL.jpg)

把选择范围缩小一点，考虑到我不能在我真正喜欢的范围上花费数千英镑。在市场顶端卖望远镜的人将不得不等待我的船进来。我不喜欢 USB 示波器，我更喜欢独立的仪器。

相反，我将着眼于我猜想你们很多人也会关注的低端中国数码产品，如 Rigol、Owon、Siglent、Hantek 等品牌。我非常熟悉它们中的不止一个，因为它们在合同、hackspaces 和其他人的长椅上使用。它们都是紧凑型仪器，不同品牌之间的规格相当相似，事实上，许多型号看起来非常相似，足以在相同的生产线上制造。当涉及到噪声甚至灵敏度的极限时，它们可能没有几千磅范围的规格，但它们以这个价格提供的性能对我来说已经足够了。

[![Why buy a DS1074 when a DS1054 will do. Image: Alex P. Kok (Own work) [CC BY-SA 4.0], via Wikimedia Commons.](img/695dff25fde2b9d6ed64e45f0c7f81a2.png)](https://hackaday.com/wp-content/uploads/2016/09/rigol_ds1074z_oscilloscope.jpg) 

有 DS1054 就行了为什么要买 DS1074。图片:Alex P. Kok(自己的作品)[CC BY-SA 4.0]，via [维基共享资源](https://commons.wikimedia.org/wiki/File:Rigol_DS1074Z_Oscilloscope.jpg)。

因此，给定一系列表面上相似但价格仍超出市场预算的望远镜，我该如何选择？一旦我决定只需要 2 个通道而不是 4 个，我的基本需求首先是带宽，所以这似乎是一个很好的开始。但即使在那里，画面是混乱的，这似乎是这些仪器的规范，有一个报价的带宽，可以通过软件黑客扩展。最著名的是 Rigol 1050 系列，50 兆赫的示波器[，它可以达到 100 兆赫的带宽](http://hackaday.com/2014/11/12/how-to-get-50-more-zed-from-your-rigol-ds1054z/)，但它们绝不是唯一的。也许制造商允许这种非法升级，因为它们是一种有价值的销售工具。虽然我的直觉是购买我能负担得起的最高带宽范围，并将以后的升级视为奖金，但不一定要立即这样做，因为我更喜欢我的仪器没有品牌和保修。

即使在带宽上归航也不能给我应有的清晰图像。当所有的税都付清后，我可以花 200 到 300 英镑(约 260 到 400 美元)买任何一款类似规格的中国双通道 100MHz 示波器。一些型号甚至承诺通过软件破解获得 200MHz 的额外升级，但这与价格无关。我只能看着样本记忆长度的差异，甚至怀疑我有时是否只是被期望支付一点额外的费用来支持一个新兴的品牌层级。

黑客时代的读者是一个多样化的群体，除了感兴趣的读者之外，他们还是我们所涉及的几乎任何主题的真正的专家，而不是纸上谈兵。你们中的一些人会像我一样看待新的“范围”,你们中的许多人自己也会经历这个过程，并有好的和坏的故事来讲述你们的选择。所以，如果你站在我的位置，看着预算数字示波器，你的选择会受到什么影响？

标题图片:Binarysequence(自己的作品)[CC BY-SA 3.0]，通过 [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Rigol_DS2000_Series_Digital_Oscilloscope.png)