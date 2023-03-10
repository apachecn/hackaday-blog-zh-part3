# 机制:轴承

> 原文：<https://hackaday.com/2018/02/14/mechanisms-bearings/>

从 3D 打印机的步进器到每个汽车引擎的数百个步进器，它们位于每个坐立不安的旋转器和运行我们生活的每个马达的核心。它们可以像润滑衬套一样简单，也可以像车轴上的滚柱轴承一样复杂。轴承每天都在为我们工作，引导力量和减少摩擦，了解它们对完成旋转机构的工作很重要。

### 滚动轴承

[![](img/ad4fc685a43b6921d3f858e92a8a0baf.png)](https://hackaday.com/wp-content/uploads/2018/01/ball-bearings_0.png)

Roller bearing. Source: [Machine Design](http://www.machinedesign.com/whats-difference-between/what-s-difference-between-bearings-1)

当使用术语“轴承”时，首先想到的可能是广义的*滚动元件轴承*中的一些东西，如滚柱轴承或滚珠轴承。我们以前都见过它们——困在两个凹槽轨道之间的坚韧钢球或圆柱体。传说莱昂纳多·达·芬奇在 16 世纪发明了滚珠轴承，但就像他的许多画作一样，数百年来都没有尝试过实际实施，直到材料科学和工程的进步赶上了他最初的设想。

滚动元件轴承依靠限制在内外圈之间的滚动元件来减少摩擦和管理负载。轴承有两种主要载荷:径向载荷和轴向载荷。轴承上的径向载荷垂直于轴的长轴。巨型电机转子轴施加在外壳上的力就是径向载荷的一个例子。滚珠轴承在处理径向载荷方面非常出色，但是滚柱轴承，由于其沿着滚柱的表面积比滚珠的点接触面积更大，所以甚至更好。

 [https://www.youtube.com/embed/b6svVy1lYOA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/b6svVy1lYOA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



但是，这两种方法都不擅长处理轴向载荷，或者平行于轴长轴的载荷。轴向载荷可能是在用端铣刀过度切入切削时，CNC 刳刨机的主轴被压入电机。因为这些轴承的内圈和外圈上的凹槽不能很深，所以滚动元件在轴向上没有太多压力，导致该尺寸的性能很差。

[![](img/1154f934bb23e1bfe56de5fb9ed2fcc3.png)](https://hackaday.com/wp-content/uploads/2018/02/tapered-roller-bearing_din720_120_bright.png)

Tapered roller bearing by [Silberwolf](https://commons.wikimedia.org/wiki/File:Tapered-roller-bearing_din720_120.png), CC BY 2.5

圆锥滚子轴承更擅长处理轴向载荷，但代价是一些径向载荷的处理。圆锥滚子轴承顾名思义，就是内圈形状像一个浅圆锥的滚子轴承，与外圈的锥度相匹配。圆锥滚子轴承可以承受高轴向载荷，但只能承受将内圈压入外圈锥度的方向的载荷。如果需要处理两个方向的轴向载荷，圆锥轴承通常成对使用。

当然，关于滚动轴承的主题有很多变化。有时，单个轴承内有两个平行的座圈，以便更好地处理负载，甚至有相对的锥形元件，因此单个轴承可以更好地处理轴向负载。额外的零件，如防护罩和密封件，可以防止砂砾或润滑剂进入。虽然大多数滚柱轴承和滚珠轴承由钢制成，但也使用了从木材到塑料甚至陶瓷的其他材料。陶瓷球轴承有一些有趣的特性:

 [https://www.youtube.com/embed/h1Sfjf3VrYQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/h1Sfjf3VrYQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 流体动力轴承

一种简单得多的轴承是*流体动力轴承*，或称滑动轴承。在孔中旋转的轴是最简单的例子，尽管在金属与金属直接接触的情况下，这种轴承在大多数实际情况下并不长久。大多数流体动力轴承依靠流体的特性来达到减少摩擦和控制载荷的目的。油脂或油是流体动力轴承中最常用的流体；润滑剂在轴和轴承表面之间形成一层薄膜，防止金属与金属接触，并且由于流体的不可压缩性，能够传递大量的径向载荷。

[![](img/f45c1b6dadb6fa2e2a73b7b7238bd4e7.png)](https://hackaday.com/wp-content/uploads/2018/02/oil-impregnated-bushing.jpg)

Oil-impregnated bronze bushing from [National Bronze](http://www.nationalbronze.com/News/)

一种常见的流体动力轴承是烧结青铜轴承，在许多业余爱好者的马达和伺服系统中都有。青铜颗粒被压制并加热成多孔的圆柱形，中心有一个孔。马达的轴穿过孔，渗入孔中的油提供了减少摩擦所需的流体膜。内燃机曲轴中也有滑动轴承，既在连杆的端部，也在曲轴和曲轴箱之间，并且通常通过飞溅或通过在压力下泵送通过小油道的油来间接润滑。一般来说，像这样的滑动轴承在旋转部件之间有一层较软的金属，以防止发动机缺油时损坏，并便于在大修期间更换。

当然，这仅仅触及了该领域的表面，完全错过了令人着迷的轴承，如磁性轴承，其中金属与金属的接触是通过磁性排斥来防止的，或使用加压气体或液体将轴与轴颈分开的流体轴承。但这些至少是一些最常见的轴承，以及一些机械装置背后的工程。

专题图片来源: [GMN 保罗穆勒工业有限公司&股份有限公司](http://gmn.de/en/ball-bearings/)