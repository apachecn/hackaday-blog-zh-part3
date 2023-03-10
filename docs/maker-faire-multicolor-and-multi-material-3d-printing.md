# Maker Faire 多色多材料 3D 打印

> 原文：<https://hackaday.com/2016/10/03/maker-faire-multicolor-and-multi-material-3d-printing/>

桌面 3D 打印的下一个前沿是多材料和多色打印。现在，你可以为 Lulzbot 购买一个双工具头，其他公司的双工具头也存在，尽管它们有点罕见。在接下来的几年里，我们将会看到许多打印机能够打印可溶解的支持物和全彩色 3D 打印机。

在这里，用多种颜色印刷几乎是不可能的，但这并不意味着我们正处于一场彻底革命的风口浪尖。多材料印刷有点落后；明年你将能够打印两种颜色的 PLA，但是用 PLA 和 ABS 打印一个物体将会有点棘手。用 PLA 和尼龙打印东西会很辛苦。同样，颜色混合也很棘手。我们可以做到这一点，工具正在到位，但请将今年视为我们五年后将要做的事情的预演。

### i3 四路车

上周， [Prusa 推出了 4 挤出机升级版](http://hackaday.com/2016/09/28/prusa-releases-4-extruder-upgrade/)，升级到 i3 Mk 2 的最新版本。本周末在 Maker Faire 上，世界第一次看到这台机器在运行，打印出多色的鱼。

 [![dsc_0281](img/322bf47d4ac7a14dc49192cd6087cf9f.png "dsc_0281")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0281.jpg?ssl=1)  [![dsc_0254](img/0d8ca3050e98aa8145df1527f6b8bf33.png "dsc_0254")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0254.jpg?ssl=1)  [![dsc_0294](img/10b5355ba6f12695071ea8162bd833e9.png "dsc_0294")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0294.jpg?ssl=1)  [![dsc_0285](img/aab05267a4e012b6dae3fa58652b4a50.png "dsc_0285")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0285.jpg?ssl=1)  [![dsc_0250](img/cf33f0787650a2707b6ab900ef7f7c94.png "dsc_0250")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0250.jpg?ssl=1)  [![dsc_0257](img/1a13d588490a29a365d1e4930d1f879b.png "dsc_0257")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0257.jpg?ssl=1)  [![dsc_0296](img/36ef25ff8ca7ab31038a9f4aa424186f.png "dsc_0296")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0296.jpg?ssl=1)  [![dsc_0252](img/e26f033812da4f5705c6c6b1b5f41d25.png "dsc_0252")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0252.jpg?ssl=1)  [![dsc_0291](img/f7402fb5ef90d92b493f6ebcaa1c7600.png "dsc_0291")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0291.jpg?ssl=1)  [![dsc_0249](img/bbafc7f76c561b0ae368a7cc07527a4f.png "dsc_0249")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0249.jpg?ssl=1)  [![dsc_0284](img/0fa75fbae5776a500f2dce8bf356723f.png "dsc_0284")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/dsc_0284.jpg?ssl=1) 

下面是 Prusa 的 4 色 mod 的工作原理。一个小型的基于 SSR 的驱动器连接到控制器板上，允许独立控制四个不同的步进驱动器，但不能同时控制。这些步进器通过一个鲍登管将灯丝送入一个四向 Y 形适配器，该适配器就在轴端上方。为了改变颜色，打印机非常快速地将细丝从 Y 形适配器中退出，推入新的颜色，并将先前颜色的细丝的剩余部分喷射到废料塔上。

当这个 mod 第一次发布的时候，有一些关于这个废塔会有多浪费的问题。它实际上是非常优化的，有照片为证:

![prusa](img/4e315cfcb15d0c689069df6f660d9a75.png)

“废塔”有三个“槽”，在那里发生颜色变化。打印机只在需要的时候浪费灯丝，切片机也是需要多聪明就有多聪明。这里几乎没有浪费。

对我来说，这就是我们在不久的将来要做的多色 3D 打印。步进电机很便宜，开关电机的电路板也很便宜。Hotends 很贵，双 hotends 意味着调平和偏移问题。也就是说，这种设置有局限性:没有颜色混合，用两种不同温度的材料(例如 PLA 和尼龙)打印将很难或不可能。还是很牛逼的。

### 颜色混合

光谱的另一端是 [ORD Solutions RoVa4D 打印机](http://www.ordsolutions.com/rova4d-full-color-blender-3d-printer-pre-order/)。您的桌面喷墨打印机使用青色、洋红色、黄色和黑色墨水来打印任何颜色。RoVa 使用青色、品红色、黄色、黑色和白色灯丝来打印任何颜色的物体。这台打印机上还有两台挤出机，专为柔性和支撑材料设计。这是一台打印机，有七个挤压机，供给一个水冷混合热端。这是 3D 打印机工程的一次胜利。

 [![img_20161002_114547](img/52e21f871fa028f8e9ae3ee7919ffe37.png "img_20161002_114547")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/img_20161002_114547.jpg?ssl=1)  [![img_20161002_114557](img/2b9343195f9cd26833dea76be63bb4ed.png "img_20161002_114557")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/img_20161002_114557.jpg?ssl=1)  [![img_20161002_114619](img/7a654e7b51e6c2185f7ee49960d3bb41.png "img_20161002_114619")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/img_20161002_114619.jpg?ssl=1)  [![img_20161002_114628](img/8e9c117c8ff1d46a981457a5ab0c6fbd.png "img_20161002_114628")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/img_20161002_114628.jpg?ssl=1)  [![img_20161002_114808](img/42b7c32c2b692000e8a0a02af585b863.png "img_20161002_114808")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/img_20161002_114808.jpg?ssl=1)  [![eien](img/40d1d77704d33e668708f6b19ade78e3.png "eien")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/10/eien.jpg?ssl=1) 

现在，切割多色印刷品很难。ORD 有一个工具可以让你把一个标准。STL 文件并“绘制”一个对象，以便可以在他们的打印机上打印。太神奇了，不过是闭源的。对 3D 打印感兴趣的软件开发人员，有一个项目适合你。

就印刷质量而言，RoVa 处于一个奇怪的位置。现在，没有人在混合彩色 3D 打印机。拥有这种能力值得赞许。但是，所有的印刷品都有颜色伪影。看着印刷的爱因斯坦半身像，我可以很容易地在嘴唇被印刷的地方看到一条粉红色的条纹。如果我给分数，我不知道我是否能为此扣分。它可以工作，但它是在点阵图像写入打印机上制作的彩色位图打印的 3D 打印版本。质量会上去，但我不知道这台机器会不会这样。

这纯粹是推测，但我不知道 ORD Solutions 怎么能卖得起这种打印机。目前，带水冷热端的七挤出机版本售价为 3750 美元，将于 2017 年 5 月交付。人们普遍认为它太便宜了。

### 2017: ~~双重~~多重挤压

3D 打印慢慢走向双挤压和多挤压。颜色是一大原因，但不是最好的。LulzBot 的柔性挤出机提出了将柔性和刚性材料结合起来的观点，以应对一些超材料的怪异之处。可溶解的细丝允许任何双挤压机打印机制造任何物体，而不考虑几何形状。

可溶性细丝已经存在了一段时间，从 Makerbot 的水溶性 PVA 细丝到在丙酮中溶解 ABS，再到柠檬烯可溶性 HIPS。除了高抗冲聚苯乙烯之外，这些细丝从未真正成为可溶解的支撑材料。这种情况可能会改变。去年 3 月在 MRRF， [E3D 宣布他们正在研究支架](http://hackaday.com/2016/03/30/mrrf-innovating-extruders-and-dissolvable-filament/)，这是一种水溶性的支持材料，其基础材料与制作凝胶帽的材料相同。要清除支架支撑材料，只需将您的零件放入洗碗机中即可。它就要来了，很快我们就会真正使用双重和多重挤压。

我们正慢慢向一种紧凑的桌面设备发展，这种设备能够以任何方向、任何颜色打印任何对象。无论如何，这是我们努力的目标。我们还没有到达那里，但是它正在到达那里，我们真的很期待这项技术走向何方。