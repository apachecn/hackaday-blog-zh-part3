# 点评:Monoprice MP Select 迷你 3D 打印机

> 原文：<https://hackaday.com/2016/06/13/review-monoprice-mp-select-mini-3d-printer/>

2016 年是消费级 3D 打印机年。是的，自 2012 年以来，对 3D 打印的大肆宣传已经平息。三年前的 Maker Faire 上有太多的 3D 打印机。尽管如此，3D 打印机的销售从未如此强劲，行业正在增长，低端机器变得非常非常好。

打印机也越来越便宜。在去年 1 月的 CES 上，你购买以太网和 HDMI 电缆的同一家公司 Monoprice 推出了一系列将于今年发布的 3D 打印机。虽然 300 美元的树脂打印机已经上市，但 Monoprice 发布了他们的 [MP Select 迷你 3D 打印机，售价 200 美元](http://www.monoprice.com/product?c_id=107&cp_id=10724&cs_id=1072403&p_id=15365)。这台打印机上个月底出现在 Monoprice 上。

我的好奇心价值超过 200 美元，所以 Hackaday 的读者可以看到 MP Select 迷你 3D 打印机的评论。底线呢？这台打印机有一些问题，但没有什么是在价格是它三倍的打印机上找不到的。这是一台改变游戏规则的机器，2016 年是入门级消费者 3D 打印机之年。

## 无聊的规格

[![](img/5b0cf148bc0f8f137cfc556ab322fa5b.png)](https://hackaday.com/wp-content/uploads/2016/06/buddahred.jpg) 

标准佛从[金](http://tf3dm.com/3d-model/jade-buddah-69408.html)。该打印展示了 Z 带，但这是切片机(Cura)的问题，而不是打印机的问题

MP Select Mini 的规格表拥有 120 x 120 x 120mm 毫米的构建面积、100 微米的分辨率、加热构建板和 55 毫米/秒的打印速度。令人惊讶的是，这台打印机将 Cura、Repetier-Host、ReplicatorG 和 Simplify3D 列为兼容软件。这意味着它说正常的 g 代码。

Monoprice 的 MP Select Mini 不需要特殊的灯丝，可以使用标准的开源 3D 打印软件。这与 2014 年的 [XYZPrinting 达芬奇](http://us.xyzprinting.com/us_en/Product/da-Vinci-1.0)形成鲜明对比。达芬奇使用芯片、DRMed 灯丝和专有接口，而不是标准的 g 代码。MP Select Mini 没有这些技巧，对于一台 200 美元的打印机来说是一个小小的奇迹。

像去年 1 月在 CES 上发现的大多数名牌打印机一样，这台打印机是中国某个地方已经在制造的东西的翻版。制造商最有可能的嫌疑人是一家名为 Infitary 的公司。你现在可以在全球速卖通上买到一台和 Monoprice MP Mini [几乎一模一样的打印机，而且似乎 Monoprice 并没有给这台打印机增加什么特别的东西。](http://www.aliexpress.com/store/product/Infitary-Portable-Mini-Lesser-Panda-3D-Printer-Fully-Assembled-High-precision-Auto-Leveling-FDM-3d-printer/2184116_32663993735.html)

从规格表来看，我猜买方垄断者甚至不知道他们手上有什么。这台打印机的真正规格实际上比 Monoprice 公布的要好。这种打印机能够打印高度远小于 100 微米的层。

## 印刷品

[![The first layer of Wade's Gear](img/dad841ab6a0ac9ec76fd541a42aeb935.png)](https://hackaday.com/wp-content/uploads/2016/06/wadesgear.jpg)

The first layer of [Wade’s Gear](http://www.thingiverse.com/thing:1794)

[![The 3D Benchy. With this print, the printer demonstrated issues in cooling the filament and overhangs.](img/7c01ab0118f21a708035bfabaf854b08.png)](https://hackaday.com/wp-content/uploads/2016/06/benchy.jpg)

The 3D Benchy. With this print, the printer demonstrated issues in cooling the filament and overhangs.

在展示 Monoprice MP Select Mini 可以打印的照片之前，我必须提到一个简单的事实:*样张照片并不代表打印机的质量。*3D 打印机只是一台 CNC 机器，把 STL 文件变成实物的大部分工作都是由切片器完成的。

也就是说，通过查看一些 3D 打印样本，你可以知道一些事情。z 轴摆动可以很容易地通过观察直的垂直墙壁来识别。打印机控制加热温度和使用风扇的能力可以很容易地在突出部分看到。

我的第一批印刷品是 Benchy，拖船 3D 基准工具。虽然不完美，开箱即用，并采用推荐的 Cura 设置，这台打印机生产的 Benchy 在质量上至少与任何其他未校准的打印机相当。只需做一点工作来获得正确的设置，我可以看到这台打印机生产的 Benchys 至少与其他任何中档打印机生产的 Benchys 相当。

Monoprice MP Select Mini 有一个明显的问题:hotend 的温度控制回路非常糟糕。我的打印机在几分钟内有+/- 5 度的温度波动，这已经在该型号的其他评测中看到过。其原因是未校准的 PID 环路。几乎每个打印机固件[都有一个 PID 自动调节功能](http://reprap.org/wiki/PID_Tuning)来解决这个问题。据我所知，这台打印机的固件没有 PID 自动调节功能。

[![](img/3a3bfe72b2d3102b45cb8efe906e7673.png)](https://hackaday.com/wp-content/uploads/2016/06/singlelayer.jpg)

A single solid layer, printed at a low temperature. The ‘gaps’ are where the filament jammed, and is due entirely to poor temperature control

[![](img/6632e6b2f3ad6548e8f31d3a5a81bc33.png)](https://hackaday.com/wp-content/uploads/2016/06/marvinback.jpg)

The back of a 3X scaled Marvin. No Z-banding, but some trouble with overhangs.

[![](img/fd3d3d1164c725e7815ec150dd55c113.png)](https://hackaday.com/wp-content/uploads/2016/06/yellowbenchy.jpg)

A Benchy in yellow. This print demonstrated much better control of overhangs.

[![](img/2e90bf82466c37bd934216afc08bbab5.png)](https://hackaday.com/wp-content/uploads/2016/06/wall-print.jpg)

The outside perimeter of a 110 x 110 x 110 mm cube. There is no Z-banding

[![](img/9ba26bc5aa08e84fdecf9af4b3c5030a.png)](https://hackaday.com/wp-content/uploads/2016/06/benchy.jpg)

The 3D Benchy. With this print, the printer demonstrated issues in cooling the filament and overhangs.

[![](img/4f95fe37c884379c65ce0c5d51465bd1.png)](https://hackaday.com/wp-content/uploads/2016/06/buddahred.jpg)

The standard buddha from [kim]. This print exhibits Z banding, but it’s an issue with the slicer.

[![](img/804d093eb5ffe8bff81a289d9b474bfe.png)](https://hackaday.com/wp-content/uploads/2016/06/marvin.jpg)

A 3X 3DHubs Marvin. Overhangs were acceptable for such a large print. This was printed at 260 degrees in PET-G

[![](img/30f3a1b107c6164258aa2d5f1b769a25.png)](https://hackaday.com/wp-content/uploads/2016/06/benchy2.jpg)

A second view of the 3DBenchy

[![](img/f6670ac035b40dd398cabf2811f69749.png)](https://hackaday.com/wp-content/uploads/2016/06/marvin-infill.jpg)

The infill for the 3X 3DHubs Marvin print. Notice a few breaks in the infill. This was printed at 260 degrees in PET-G

MP Select Mini 上的打印效果好吗？是的，他们可以。MP Select Mini 有一些问题，但这些问题不会在几个月内被 3D 打印机社区轻易解决。

## 拆卸

这台打印机是按价格制造的。奇怪的是，这个事实直到你开始把它拆开才真正显示出来。机箱是全金属的，X 轴和 Y 轴是由 6 毫米的杆驱动的，Z 轴是由丝杠驱动的，真的没有太多东西值得大书特书。这台打印机造得很结实，我可以很容易地预见到它会经受住许多虐待。

 [![Back cover off](img/fc1cc6c293b4d53f5f9f7687ac7e8c28.png "Back Cover off")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/06/back-cover-off.jpg?ssl=1) Back cover off [![NEMA 17s for all motors (except Z)](img/65e4d70f067901513d006901375c8dd3.png "mnotor")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/06/mnotor.jpg?ssl=1) NEMA 17s for all motors (except Z) [![The bottom guts](img/5b16c89c0958671dc02b54d2e371a22b.png "Guts")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/06/guts.jpg?ssl=1) The bottom guts

### 马达和机械

从最便宜的 fleaBay specials 到高端的 Lulzbots 和 Ultimakers，所有 3D 打印机的标准都是步进电机。如果你有一台 3D 打印机，你很可能拥有四五台 NEMA 17 步进电机。它们是最佳解决方案吗？这是有争议的，但这是标准。MP Select Mini 在 Z 轴上安装了一个圆形的非 NEMA 电机，扭转了这一趋势。

Z 轴由 M4 螺杆驱动。很奇怪，Z 轴非常慢。然而，这是买方垄断没有提到的一个卖点。因为 Z 轴丝杠的螺距非常小，所以这台打印机可以生产非常非常小层高的物体。[【Prusa】的计算器](http://prusaprinters.org/calculator/#stepspermmlead)给出了一个非常低的*理论最小层高*用于此设置。最小层高度不是规格表中所说的 100 微米，但这可以作为证据，证明 Monoprice 低估了这台打印机的能力。这确实意味着 Z 轴移动非常慢，但这真的无关紧要。

### 电子产品

这就是 MP Mini Select 的亮点。如果您正在寻找这款打印机的一个改变游戏规则的功能，它就是控制板。

在我拿出六角扳手进行拆卸之前，我对固件和电子设备的唯一印象来自于观看正在制作的测试图。这台机器有非常不同的地方:加速度。从床的一端移动到另一端时的加速斜坡是我在 3D 打印机上从未见过的。它平滑、精确，看起来几乎很美。我以为这是定制固件。是的，但这只是故事的一半。

这台打印机的电子板是 32 位 ARM Cortex M3，这是对几乎所有其他 3D 打印机控制器中的 8 位 ATmegas 的巨大改进。

 [![LCD](img/1be32ffc954b56647cbec432f253c82d.png "LCD")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/06/lcd.jpg?ssl=1)  [![Board Wired](img/96020c303582de1d19660b55b18faaa4.png "Board Wired")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/06/board-wired.jpg?ssl=1)  [![Board Bare](img/ef3eadbbed000f12f391d06d7075085e.png "Board Bare")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/06/board-bare.jpg?ssl=1)  [![Board Back](img/def4dc8639d4f83c145195156e46368c.png "Board Back")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/06/board-back.jpg?ssl=1) [![The brains of the entire printer, an STM32F103 microcontroller. 32-bit 3D printers have finally arrived.](img/581ebf80994842982bf9be2298c16578.png)](https://hackaday.com/wp-content/uploads/2016/06/chip.jpg)

The brains of the entire printer, an STM32F103 microcontroller. 32-bit 3D printers have finally arrived.

这台打印机是一次测试，测试你能以多低的成本生产一台打印机，这些努力清楚地显示在电子板上。该电路板上只有六个芯片:四个 HH4988 电机驱动器(我假设是流行的 A4988 步进电机驱动器的非品牌克隆)，一个降压转换器(最有可能用于 LCD)，以及一个微控制器 STM32F103 微控制器。是的，32 位打印终于来了。

我不可能低估 ARM 微控制器在这台打印机中的重要性。到目前为止，[除了 Smoothieboard](http://smoothieware.org/smoothieboard) ，绝大多数 3D 打印机都是围绕 ATMega 微控制器构建的。考虑到历史背景，这是可以理解的；第一批 RepRaps 是在 2009 年左右开发的，当时 Arduino 非常大。3D 打印机控制器板是围绕这些 8 位微控制器开发的，并且开发一直持续到今天。

每个人都认识到 ARM 微控制器是 3D 打印机控制板的未来。ARM 微处理器更便宜——这种打印机板上的 STM32F103 的价格是所有其他打印机控制器中“标准”ATMega2560 或 AT90USB 的一半。ARM 芯片更强大，加速更流畅。ARM 微处理器只是一个更好的解决问题的方案。

尽管这些显而易见的现实，成千上万的人一直致力于 8 位控制器板的大部分十年。在开源 3D 打印领域，有很多技术债务需要偿还。这笔技术债务刚刚由中国的一个随机嵌入式开发人员还清。如果你想看到 3D 打印机控制器板的未来，你需要做的就是从中国购买一台 200 美元的打印机。

至于液晶显示器和控制去，他们正是你所期望的。这是一个全彩色 TFT，很可能是旧的非智能手机中使用的相同型号，只有一个旋转按钮。我相信 LCD 和按钮组件是通过 SPI 连接到印刷电路板的。控件允许用户从 SD 卡加载文件，移动轴，并设置温度。这是最低限度，但你真的不需要更多。

### 加热床

在大多数消费 3D 打印机上——无论如何，那些有加热床的打印机——你会发现一个 PCB 加热床被拧紧或夹在一个铝或玻璃板上。这是标准。MP Mini Select 没有单独的构建板和 PCB 加热器。取而代之的是，一片薄铝片直接粘合到 PCB 加热器上。

 [![The PCB heat bed is bonded to an aluminum build plate](img/973b9a9a09ca0ac3b8f33da7c36a9c78.png "bedcorner")](https://hackaday.com/2016/06/13/review-monoprice-mp-select-mini-3d-printer/bedcorner/) The PCB heat bed is bonded to an aluminum build plate [![Heated Bed](img/bb44434d1ff03f31874dfd91dbc1b285.png "Heated Bed")](https://hackaday.com/2016/06/13/review-monoprice-mp-select-mini-3d-printer/heated-bed/) 

虽然这使得建造成本更低——除了任何紧固件之外，您不必在 BOM 中添加铝或玻璃板——但我担心它不会像标准的单独铝/玻璃建造板和加热器那样坚固。这并不意味着这是一个坏的解决方案，只是一个粘合铝板将无法承受这么多的虐待而不翘曲。

### 创新的低成本酒店

这种打印机的主题是建立一个价格，这是最明显的比酒店。值得制造商称赞的是，这款 hotend 确实使用了标准的加热筒和可更换的热敏电阻。这是旅馆的未来，尽管你仍然可以买到带有镍铬合金加热器芯的旅馆，但它们已经过时了。

 [![The hotend. Note the air gap between the Bowden end and the beginning of the heat break. When changing out filament, it can jam in this air gap](img/05c6ee3dccc3df2b2185236bff17f493.png "hotend")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/06/hotend.jpg?ssl=1) The hotend. Note the air gap between the Bowden end and the beginning of the heat break. When changing out filament, it can jam in this air gap [![The aluminum heatsink extrusion. This is the part that bolts onto the x carriage and holds the heat break.](img/008d14e0432501884259eb78337d043b.png "Extrusion")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/06/extrusion.jpg?ssl=1) The aluminum heatsink extrusion. This is the part that bolts onto the x carriage and holds the heat break.

hotend 由一个 0.4 毫米的黄铜喷嘴和一个断热器组成，前者拧入一个加热块，后者拧入一个铝制散热片挤压件。这可能是现存的最简单的 hotend，但这并不意味着它在功能上有所欠缺。我还没有把这个 hotend 拆开，但我怀疑它是一个全金属 hotend。聚四氟乙烯衬里在热障中根本没有空间。这是令人惊讶的，因为这显然是你能买到的最便宜的旅馆，并允许 MP Select Mini 用奇异的塑料打印。

不过，我不建议用奇异的塑料印刷。这款 hotend 有一个非常缺少的功能:第二个风扇来冷却从喷嘴喷出的塑料。MP Mini 使用一个 20 毫米的风扇将空气吹到热沉和散热片上，并吹到从喷嘴出来的熔融塑料上。这是一个糟糕的设计，加上固件中较差的温度控制，导致该打印机的桥接能力较差。

## 这些是你想要的升级

每台 3D 打印机都需要升级。有些，如 Lulzbot Taz 6，提供了您想要的一切，但理想情况下，您仍然希望在其中添加一个树莓 Pi，以实现无头、联网打印功能。便宜的易贝工具包？你会想要一个更好的建筑板，一个新的挤出机，也许还有一个更好的酒店。MP Mini 的设备相当好，但还有一些你想要的额外设备。

### 新的构建表面

如上所述，这台打印机的一体式加热床是我见过的最有趣的设计之一。不过，MP Mini 附带的打印表面只是一大张遮蔽胶带。这只能让你印几张照片，但之后你会想要更好的。

在这篇评论中，我使用了一条 6”宽的 Kapton 和胶棒，但目前“构建板的最佳材料”是[一张 PEI 或 Ultem](http://reprap.org/wiki/PEI_build_surface) 用一张 3M 468MP 胶带安装到构建板上。你可以从亚马逊花 16 美元买一张 12 英寸 x 12 英寸的 PEI 纸[，花 17 美元买一张 12 英寸 x 12 英寸见方的](https://www.amazon.com/dp/B0013HKZTA) [468MP 转印纸](https://www.amazon.com/dp/B007Y7D5NQ/)。这是 MP Select 的四个 PEI 构建表面，售价 37 美元，对于 PLA、ABS 和(据报道)PET 来说，这将是一个惊人的免维护构建表面。

### 树莓派/八开印花图案

有报道说 MP Mini 声音很大。我的不是，但显然结果可能不同。在任何情况下，您都希望将打印机安装在某个偏僻的地方——车间、车库或地下室——并让它一次工作几个小时。

虽然你可以从 SD 卡上打印(我有专用的)，但这仍然意味着你需要在电脑和打印机之间传输文件。Octoprint 消除了对这种 sneakernet 的需求，并允许通过网络远程控制打印机。如果你计划使用这台打印机，而不仅仅是偶尔的小饰品，Octoprint 设置将是一个巨大的好处。这些说明可以在[OctoPrint.org](http://octoprint.org/)上找到。你会想要一个已经积了几年灰尘的树莓 Pi，一个 USB WiFi 适配器，SD 卡和一个 USB 电源。

### Hotend 配接卡

[![Print this thing. Print this thing now.](img/8ca2b4b8624b46868835fd89b0514439.png)](https://hackaday.com/wp-content/uploads/2016/06/1194911465673603947.png)

Print this thing. Print this thing now.

每个旅馆都会死。酒店是消耗品。不过，它们可以持续一段时间，即使打印了 100 个小时，也没有什么可以告诉我 MP Mini 上的 hotend 不会像其他 hotend 一样持久。

不幸的是，没有直接替换的来源。如果你想更换这台打印机的盖子，你得再花 200 美元买一台新打印机。花 200 美元开一家新酒店是疯狂的，任何强迫消费者这么做的公司都会很快倒闭。

[如果你买了这台打印机，这应该是你打印的第一件东西](https://hackaday.io/project/12184-monoprice-mp-select-mini-e3d-hotend-adapter)。我在 OpenSCAD 中找到了一个适配器，可以在 MP 迷你打印机上安装 E3D hotend。它直接固定在 X 托架上。完美吗？不，但是如果你打印出这个适配器，你就可以用你的新旅馆打印出一个*更好的*适配器。把它打印出来，贴在打印机后面。你以后会感谢我的。

## 您应该购买这台打印机吗？

这台打印机有问题。这是一个封闭的源代码设计，不可能找到替换部件。该固件没有像马林的自动调谐 PID 值方便的功能。酒店的风扇设计需要改进。该打印机使用鲍登设置，因此柔性细丝——Ninjaflex 和 semi flex——不可用。相信我，我尽力了。

### 打印机比较

无论如何，Monoprice MP Select Mini 是我的第一台 3D 打印机，所以让我们来比较一下苹果和苹果。可以被称为我的第一台 3D 打印机的打印机不是 Lulzbots、Ultimakers 或其他价格在 1500 美元以上的机器。“初学者”3D 打印机更好地定义为 [SeeMeCNC 厄里斯](https://www.seemecnc.com/collections/ready-to-print-3d-printers/products/eris-desktop-3d-printer)、 [Printrbot Play](https://printrbot.com/shop/assembled-printrbot-play/) 和 [Metal Simple](https://printrbot.com/shop/assembled-simple-metal-with-heated-bed/) 、 [Deezmaker Bukito](http://bukito3d.com/) 、 [Maker's Toolworks MiniMax](http://store.makerstoolworks.com/printers-kits/minimax-by-makers-tool-works-full-printer-kit/) 、[达芬奇打印机](http://us.store.xyzprinting.com/us_en/catalog/printer/daVinci10pro3in1?)和【Prusa】的 [i3 Mk2](http://shop.prusa3d.com/en/3d-printers/53-original-prusa-i3-mk2-3d-printer.html) 。

Monoprice MP Select Mini 在其价格范围内脱颖而出。这台机器才 200 美元，而你得到的功能是 600 美元的打印机所没有的。这是一台改变游戏规则的机器，我会把它推荐给所有寻找第一台 3D 打印机的人。由于垄断，入门级消费 3D 打印机的整个市场都被颠覆了。200 美元几乎是冲动购买的领域，买方垄断者将会卖出*很多*这样的机器。

### 现在我们有一些工作要做

当两年前达芬奇打印机发布时，大量的努力被投入到芯片灯丝的逆向工程和控制板的重新编程中，以说出正常的 g 代码。现在同样的工作必须在这台打印机上完成。

这台打印机的控制板必须反向工程和复制。第一个做到这一点的人将为下一代 RepRap 控制电子设备奠定基础。我强烈建议将逆向工程的努力放在 [Hackaday.io](https://hackaday.io/) 上。也许更重要的是，一个合适的开源 3D 打印机固件必须移植到这台打印机上。现在，这台打印机的许多缺点可以通过固件更新来解决。有了开放的、可改进的固件，再加上像样的硬件，它可能会很出色。

即使没有重写马林固件和这个电子板的克隆，它仍然是一个了不起的打印机。它并不完美，但对于成千上万的人来说已经足够好了，他们最终会在他们的工作台上拥有一台这样的设备。