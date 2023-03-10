# 大地和电网

> 原文：<https://hackaday.com/2017/07/25/earth-ground-and-the-grid/>

电网通过电线将电力传输到我们的房子，我们的布莱恩·科克菲尔德在他的[电网揭秘](http://hackaday.com/2017/01/17/the-electrical-grid-demystified/)系列中对此做了很好的报道，但是大地扮演了什么角色呢？众所周知，它是用于安全，但你知道在某些情况下，它也用于电力传输吗？

## 典型的房屋接地系统

![Grounding system normal case](img/0185b5bc136f40f27c379478ca2dc534.png)

Grounding system normal case

这里显示了一个非常典型的房屋接地系统图，以及一些通常称为火线和零线的载流导体。最左边是屋外的变压器，最右边是插着电源的电器。在它们之间是一个断路器面板和一个北美风格的墙壁插座。绿色虚线表示电流流动的正常路径。

注意与大地进行电气连接的接地电极。以美国国家电气规范(NEC)为例，第 250.52 条列出了[八种类型的接地电极](http://lightning.org/wp-content/uploads/2014/12/Bonding-2013-ULPA-LPI-rev1.pdf)。一种非常好的类型是包裹在混凝土中的电极，因为混凝土继续从地面吸收水分，并由于其重量而产生良好的物理接触。另一种是至少 8 英尺长的接地棒或管道，插入地下足够深。所谓足够深，我们的意思是包括这样的因素，即霜线不能算作一个良好的接地，因为它有很高的电阻。你必须小心使用看似深入地下的金属水管，因为在定期维护期间，这些水管的一部分经常被非金属管道所取代。

请注意，在图中，各种金属外壳都有连接到接地系统的地方。这就是所谓的结合。

那么，所有这些系统接地对我们有什么帮助？让我们从处理一个故障开始。

## 处理故障

![Ground fault](img/3756a17e8c8d6228df12e981bcf26229.png)

Ground fault

接地系统的一个目的是当某处短路时，使断路器面板中的断路器跳闸。如果有一个带金属外壳的电器，电器中火线的绝缘损坏，导致里面的铜线接触到金属外壳，就会发生这种情况。外壳成为带电电线的延伸。这叫断层。

但是金属外壳连接到由插入墙壁插座的电源线中的接地线以及从墙壁插座到断路器面板的电线组成的电气路径。在美国国家电气规范(NEC)中，这些被称为设备接地导体。

至少在北美，在服务首次进入房屋的盒子中，设备接地导体连接到中性线。在这种情况下，该盒是主断路器面板。在大多数断路器面板中，这种连接是通过将两根电线连接到金属条上来实现的，金属条通过螺纹连接或粘接到面板的外壳上，从而通过外壳实现电气连接。

沿着故障的红色虚线，现在有一个大电流流过火线、电器外壳，并使用设备接地线作为断路器面板的回路。从那里，电流通过面板的情况下，中性酒吧和中性线回到变压器。一路上，带电的电线穿过断路器面板上的断路器，电流大到足以使其跳闸，从而打开电路，使其再次安全。

但是大地是从哪里来的呢？通常不会。然而，有时，如蓝色虚线所示，少量电流会流过包括接地电极和大地的并联路径。

## 释放杂散电荷

![Discharging stray charge](img/2b4785afb59900358957b6dc15f7300f.png)

Discharging stray charge

Hackaday 上的许多人都非常熟悉接地的目的，那就是杂散电荷和静电敏感器件和元件(如 MOSFETs、CMOS ICs 和 TTL 芯片)的静电放电问题。处理这种情况的方法是佩戴防静电带或在防静电垫上工作。这些通常有一个夹子或一个专用插座用于连接大地。

你身体上的电荷将使你处于不同于地面的电位，因此电流将在你和地面之间流动。大地在很大程度上是电中性的，将很容易吸收电荷，使地和你的结合是中性的。

并非所有的静电放电都是偶然的。我们之前报道过[Kevin Darrah]的实验，他故意测试了它对各种组件的影响，并尝试了防止它的电路。

金属外壳也可能因间接雷击而带电，任何积聚的电荷都会以同样的方式流失到大地。

## 单线接地回路(SWER)

[![v](img/a49c086cf86169ab1130d3a85d449214.png)](https://hackaday.com/wp-content/uploads/2017/07/swer.jpg)

Single-wire earth return

为了节省成本，大多在农村地区或偏远、孤立的住所，有时只使用一根电线进行传输。这消除了中性返回线的成本，只要成本节约弥补了效率的降低。效率的降低是由于使用了更高电阻的大地作为返回路径。这被证明是非常安全的，在澳大利亚和新西兰有超过 200，000 公里的输电线路是这样做的。在美国，它被用于中西部和阿拉斯加州的部分地区。

电力首先由电网提供给隔离变压器的初级，将电网与大地隔离。这里，电压通常从 22 kV 逐步降低到 19 kV。次级的一侧是单传输线，另一侧接地。

然后在客户处使用配电变压器，将 19 千伏转换成适合客户的电压，例如 240 伏。初级线圈的一端是单线，另一端接地返回，最终返回隔离变压器的接地端。

土壤阻力是一个问题。干燥的土壤比潮湿的土壤导电性差，在阿拉斯加，接地棒必须延伸到永久冻土层以下，因为冰的导电性也差。此外，这种更高的电阻还会导致初级电压浮动更高，并使自复位断路器难以复位，因为它们依赖于电位差。

可以通过增加第二和第三传输线来增加额外的相位。

## 接地

你有尝试创造一个好的土地的经验吗？也许你遇到过太干燥的土壤，不得不在它周围工作？或者，正如经常发生的那样，你工作的地方肯定有些墙上的插座根本没有接地。请在下面的评论中告诉我们。

或者走到配电的现场，看看布莱恩的[电网揭秘](http://hackaday.com/2017/01/17/the-electrical-grid-demystified/)系列。