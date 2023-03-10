# 3D 集成电路的新时代

> 原文：<https://hackaday.com/2016/02/08/the-coming-age-of-3d-integrated-circuits/>

集成电路的教学模型大致是这样的:取一块硅晶片，蚀刻出几个井，用磷掺杂一些硅，去掉一些芯片的掩膜，用硼掺杂更多的硅，并在其间放置一些金属。这是现代半导体工厂如何工作的一个非常基本的模型，但它并不是非常不准确。任何人在了解这一点后都会得出的结论是，芯片天生就是三维设备。但是这些层非常小，芯片有源层的总厚度比人的头发还薄。稍加研究和思考，你就会意识到集成电路的结构实际上并不是三维的。

最近，来自硅业内部人士的谣言和有根据的猜测都指向真正的三维芯片是该行业的未来。这些芯片不像上面的例子那样只有几层厚。不是只有几十层，而是 100 层或更多的晶体管将被塞进一片硅片里。这种转变的原因包括缩短信号必须传输的距离、降低电阻(从而减少热量)以及在单一设计中优化性能和功耗。

影响当代三维芯片的想法并不新鲜；这些概念自从半导体工业开始以来就一直存在。新的是这些设备最终将如何进入市场，英特尔和其他半导体公司目前面临的挑战，以及它对未来几年的一代芯片意味着什么。

### 3D 芯片的历史

![Many different circuits on the same die, tied together with three dimensional interconnects. Image source: Pavlidis & Friedman, Three-dimensional Integrated Circuit Design (2010)](img/f514e54bea27cd7dee4fbfa6dfef8c60.png)

Many different circuits on the same die, tied together with three-dimensional interconnects. Image source: Pavlidis & Friedman, Three-dimensional Integrated Circuit Design (2010)

20 世纪 60 年代末和 70 年代初，芯片变得越来越复杂。半导体技术的前沿从运算放大器和小型数字封装转移到具有数千个晶体管的半导体，随之而来的是越来越依赖这些芯片不同部分之间的互连。

在过去 50 年的技术进步中，晶体管已经从肉眼可见的东西变成只有几个原子宽的微小颗粒。互连成为主要的设计选择，尤其是随着设计复杂度不断增加、总线宽度不断增加以及输入和输出越来越多。

因为除了最基本的集成电路之外，所有的集成电路都是三维的，所以在任何杂乱无章的大都市，放置这些互连的明显选择都是相同的解决方案；如果你不能让*成长，就让*让*成长。*

这条研究路线作为一种学术追求贯穿了 20 世纪 70 年代、80 年代和 90 年代，为新问题提供了解决方案。你如何冷却立方体的内部？你可以在整个芯片上设置冷却通道。虽然这些问题很容易定义，解决方案也很容易解释，但将整个想法从制造到成品却很难。增加晶体管密度的一个更简单的方法是将单个封装堆叠在一起。

![The main chip on the Raspberry Pi Zero is actually two ICs. The bottom is the ARM processor, while the top is the DRAM. This is known as a Package on Package (POP) assembly.](img/379fab4e107e4186ef277ba47f910a40.png)

The main chip on the Raspberry Pi Zero is actually two ICs. The bottom is the ARM processor, while the top is the DRAM. This is known as a Package on Package (POP) assembly.

这些[封装器件](https://en.wikipedia.org/wiki/Package_on_package)可以在几十个器件上看到——尽管是以倾斜的角度。Raspberry Pi Zero、Model A 和 Model B 上的大芯片是 POP 设备，顶部芯片上的 RAM 直接连接到 Broadcom CPU。最新、最大容量的 RAM 模块也使用这种技术。[内存的 JEDEC 标准](http://www.jedec.org/standards-documents/results/taxonomy%3A3193)不占 16GB DDR3 模块，但这并不意味着你不能买。在这里，PoP 设备再次成为公司解决互连问题的方法。

### 3D 芯片的现状

![Samsung's V-NAND image source](img/d93bbab864240e1cf0f32b4af4177b18.png)

三星的 V-NAND [ [图片来源](http://www.chipworks.com/about-chipworks/overview/blog/second-shoe-drops-%E2%80%93-samsung-v-nand-flash)

虽然由多层硅构建 3D 芯片的想法是一个古老的想法，但直到最近我们才看到这种技术进入消费设备。2013 年，三星凭借 V-NAND 进军 3D 闪存市场，这被视为第一项真正的生产级 3D 晶体管技术。

Chipworks 对三星 850 Pro 固态硬盘中的 V-NAND 进行了彻底的拆解。无论用什么标准来衡量，这都是一项不可思议的工程壮举。这些固态硬盘中的 V-NAND 堆栈是一个 38 层的晶体管三明治，每个晶体管存储一位信息。

这一创新显然允许三星将更多晶体管放入一个小区域，从而实现更高的容量。如果你相信三星的营销材料，一个芯片上可以塞进多达 100 层晶体管，为非常非常高容量的驱动器铺平了道路。这种能力不是唯一的好处；由于 V-NAND 的结构，存储单元之间的干扰减少，使驱动器更节能。与普通的 2D NAND 闪存相比，写入耐久性——一个存储单元可以被写入而不会损坏的次数——得到了提高。

![VoltaGPU](img/b59622b12231f1ffde0c3862326095ac.png)即使大部分关于三星的 V-NAND 3D 闪存技术的说法都是营销 wank，你也不能否认它是一款非常优秀的 SSD。在任何基于 PC 的社区的论坛上查看任何“构建建议”帖子，你会在零件列表中的某个地方找到三星 850 Pro SSD。3D Flash 是技术的胜利，也是市场的成功。每个人心中的问题都变成了“什么时候不仅仅是固态硬盘了？”

下一代 Nvidia GPU Volta 将在 2018 年发布时采用堆叠式 DRAM。虽然这与堆叠式 NAND 闪存的复杂程度大致相同，但它确实告诉我们，3D 芯片正在成为主流，我们将 CPU 视为真正的 3D 设备只是时间问题，而不是几层叠加在一起。

### 3D CPUs

如果你追溯半导体中有趣的技术成就的起源，通常的进展是从大学开始，随着存储器进入生产，最后成为将 CPU 结合在一起的胶水的一部分。曾经，英特尔最出名的是他们的超高容量 DRAM 芯片(数百字节！)，在他们的制造过程中获得的知识转移到 CPU 之前。

![Intel's EMIB. Image source](img/d4a9f26c26d0e75d5e2dd1baef929756.png)

英特尔的 EMIB。【[图片来源](http://www.intel.com/content/www/us/en/foundry/emib.html)

这必然意味着设计了几十层的 CPU。对于英特尔来说，下一个重大进步是嵌入式多芯片互连桥(EMIB)，它采用了 PoP 概念，去除了环氧树脂，并在更低的级别上完成所有工作。EMIB 实际上是芯片之间的背板。通过在一片硅片上放置多个芯片，通孔以之字形方式隧穿，英特尔可以在一片硅片上放置许多不同的电路。

虽然在一块硅片上放置多个芯片对英特尔来说是一个福音——特别是在他们的产品组合中有 Altera IP 的情况下——但它并不是真正的三维芯片。那要等一会儿了；我们现在只有几年的 3D Flash，3D RAM 还要两年才会公开。制造 3D CPU 是一项复杂得多的工程挑战，为此我们可能要等上十年。

不过，三维芯片将会发布。这只是时间问题。除了进入硅的第三个维度，没有其他方法可以增加互连的密度、芯片上的器件数量或速度。