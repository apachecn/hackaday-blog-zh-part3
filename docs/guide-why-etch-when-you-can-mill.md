# 指南:当你可以磨的时候为什么要蚀刻 PCB？

> 原文：<https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/>

我记得我开始认真对待电子学的时候，虽然很兴奋，但一想到要面对爱好者甚至专业人士面临的两个主要障碍，一是制造自己的 PCB，二是摆弄不断减少的表面贴装尺寸，我就感到恐惧。事实证明，对后者的任何抵制都是徒劳的、昂贵的，而且坦率地说，回想起来有点愚蠢。廉价的 SMD 工具使得储存、放置和焊接所有的 SMD 变得非常容易。

一旦你把所有的业余设计/实验都局限于 SMD，你如何着手生产原型所需的 PCB？就我个人而言，我害怕蚀刻自己的电路板。这个过程很费力，涉及到杂乱的化学物质和特殊敏化的 PCB 这些我都不感兴趣。我只做过几次，并发誓再也不做了。专业但廉价的 PCB 制造更像是 it 业。OSH park 等电路板联营服务让这一切变得既简单又实惠——如果你能等待转机的话。

那么有哪些选择呢？如果你真的想从你自己的实验室快速制作原型，我提出了铣削你自己的 PCB 的例子。请继续阅读，我将带您了解从设计到原型的典型工作流程，并说服您忍受购买 PCB 工厂的相对较高的启动成本。

## 行业工具:

### 磨坊:

近年来，购买一台既坚固又足够精确的数控机床的可怕成本已经显著下降。在易贝和速卖通上快速搜索“雕刻数控机床”会返回一些有趣且价格合理的结果。这些网站上的通用机器被称为 CNC 3020，工作面积为 30 厘米×20 厘米，价格约为 250- 300 英镑(350-400 美元)。其他型号有 3040 和 6040。这些机器似乎都是基于一个单一的设计(甚至是一个制造商)，而且制造精良。铝为基础的建设是坚实的，并处理一系列的材料给予正确的主轴当然。

![](img/7fe1af85122974d19f8b17a375975d24.png)

The CNC-3020

最便宜的机器倾向于安装一个简单的 DC 50W 电主轴，这个电主轴足够可靠，更重要的是，替换起来很便宜。它适合以中等的进给速度雕刻和切割木材，但仅此而已。最近的机器配备了水冷 200 瓦主轴，这无疑是一个更好的选择。你也可以用它们切割厚度适中的铝。

我以相当便宜的价格购买了一台早期版本的 CNC-3020。该机器没有终点挡板，拥有一个旧的基于并行端口的接口，并具有大部分 PCB 功能，如自动主轴控制。不久前，我们写了一篇文章，讲述了[whitequark] [成功改造了他的机器](https://hackaday.com/2014/02/15/chinese-3020-cnc-machine-gets-some-upgrades/)来升级硬件。我也做了必要的修改，只是简单地将 3 个终点挡板连接到 CNC 上，并在表面探针上焊接一个未安装的连接器。许多较新的机器现在都预装了这些软件。

### 比特

机器准备好了，我们需要合适的工具来铣削 PCB。其中最重要的是雕刻位，负责将所有实际走线提交到 PCB 上。这个钻头需要锋利，这样它实际上切割而不是撕裂铜，当然它也需要足够细，以磨出任何微小的脚印或痕迹。经过大量的实验，我用易贝的通用 0.1 毫米 V 钻头得到了最好的结果。这些是足够便宜和可靠的大约 8-10 中型工作。然而，当在软件中指定其切割宽度时，V 形轮廓确实带来了挑战，因为你越深入，它们切割得越宽。这可以通过一些试验和错误来调整。

接下来，我们需要一些钻头来钻通孔元件安装和通孔。您指定的每个不同的孔都需要手动更换工具，因此最好简单地使用一个 0.8 毫米-1 毫米的钻头，这应该适用于大多数情况。我会推荐买[这套便宜的钻头](https://www.ebay.co.uk/itm/Tungsten-Carbide-Micro-Drill-Bits-PCB-End-Mills-Avail-INDIVIDUALLY-or-in-SETS/182811363286?hash=item2a906807d6:m:m-niywvlmwKsjIPGJfD71aA)。

我们需要的最后一点是端铣刀，负责从较大的 PCB 包层中切割出我们的电路板。1-2 毫米的立铣刀可以很好地完成这项工作。

除了上述要素，我们还需要实际的印刷电路板包层，我发现易贝通用的，便宜的，单面的是可怕的，他们像饼干一样破碎时被切割。所有更好的似乎都是双面的，无论哪种情况，在选择我喜欢的供应商之前，我都必须尝试几个不同的供应商。在 Hackaday 的整个历史中，采购优质覆铜似乎是一个尚未解决的话题。

 [![Drill bits](img/a89e8372e224d8e89d0fa19e15a39a71.png "milling-pcbs-drillbits")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170331_151216/) Drill bits [![End mill](img/81a3e753d2b7cdf8d38afede5954ac51.png "milling-pcbs-endmill")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170331_151200/) End mill [![Engraving V bit](img/3a61c4c1f765d76818012731ec811693.png "milling-pcbs-Vbit")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170331_151112/) Engraving V bit

### 多方面的

除了上面列出的重要物品，我们还需要以下物品:

*   薄双面胶带，用于将 PCB 包层固定到 CNC 的废料切割板上。这不应该是泡沫背衬，而是经常用于织物的薄膜背衬。
*   带有硬金属刷毛的抛光刷，用于一些后期处理。刚从 CNC 出来的电路板不可避免地需要去毛刺。
*   细磨砂块或砂纸清除一些较细的毛刺。
*   外用酒精和更软的刷子(我用的是牙刷！)进行收尾工作。

## 机械装置

[![](img/2d456c66e14050a58683fd63b9816053.png)](https://hackaday.com/wp-content/uploads/2017/05/20170401_161118.jpg)

DFN-8 Breakout

这个 DIY 过程中最大的挑战是获得正确和一致的切割深度。这些 V 型钻头切割得越深，切割范围就越宽，有效地剥夺了宝贵的雕刻分辨率。如果你没有调到合适的深度，有些痕迹会显得太薄太脆弱。成功的关键是试验几个切割深度，最重要的是探测 PCB，以补偿包层高度的任何变化。

为了调整正确的切割深度，我整理了一个简单的测试设计，包括超小型 [DFN-8 封装](https://www.elnec.com/pics/qfn/dfn8-2x3m.gif)的分线板。这块板上的走线尺寸和我的设计一样小。接下来，我尝试了几种不同的切割深度，最终找到了一种对这些细痕迹有可靠结果的深度。我用 0.1 毫米的 V 型钻头切削 0.8 毫米的深度。

### 准备自动调平

自动调平过程在软件中设置，只包括铣削前的探测程序。我们需要做的只是将一根废电线焊接到 PCB 覆层的一角，并使用大量双面胶带将其固定到一块理想的扁平废木料上。

完成后，将木材固定到 CNCs 工作区，并将铣刀固定在卡盘上。一对鳄鱼夹连接到焊接在 PCB 和铣刀上的电线，完成探测设置。这个想法是建立 PCB 的高度变化图，如果 PCB 不完全水平，工厂将主动补偿误差。

 [![Tape strips](img/f93934121de758a9d13ace3a85492e4a.png "milling-pcbs-tapingpcb")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170331_145547/) Tape strips [![Copper clad secured to wood](img/9327d341264185ae77d64b8b9714c52e.png "milling-pcb-fastenpcb")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170331_150356/) Copper clad secured to wood [![Copper clad and alligator clip](img/608789ce3a55533a5d3124d52cdde5bb.png "milling-pcb-probingA")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170401_140807/) Copper clad and alligator clip [![Bit and alligator clip](img/6ca35eec94fe7adf47bca6033e2b73bd.png "milling-pcb-probingB")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170401_141413/) Bit and alligator clip

## 软件

### PCB CAD

第一步是准备 CAD 文件，我们最喜欢的 PCB CAD 软件只需要 3 个 GERBER 文件:Top、Bottom 和 Drill。但在我们这样做之前，我们需要确保所有必要的预防措施都已采取，以最大限度地提高工厂复制电路的机会

作为一个例子，让我们谈谈我在设计下面的 PCB 时确保的一些事情，我已经成功地铣了好几次了。对于好奇的人来说，这是基于 ADI 公司 ADF4008 IC 的 DIY 频谱分析仪的锁相环部分。

*   **Choose footprints wisely:** This board is based around an IC available in both TSSOP-16 and LFCSP-20.![](img/d94d1a3e2287855c0696eb038734de52.png)

    The Board: Phase Lock Loop with VCO Amplifer

    为后来更小的封装进行铣削肯定会推动该工艺的能力。因为更小的足迹也意味着更小的轨迹，这使得整个过程更不可靠。基于同样的理由，我尽可能坚持使用 0805 或 0603 的被动语态。

*   **迹线到迹线间隙:**根据经验，我保持迹线间隙至少为钻头宽度的两倍。对于 0.1 毫米的钻头，0.2 毫米的最小间隙就足够了。
*   **倾卸间隙:**这种减法的一个好处是，您可以随意使用自然接地层。然而，成品电路板的走线周围往往会有铜毛刺，如果靠近接地层，可能会短路。因此，浇注到走线的间隙至少应为 0.3-0.4 mm，这也将使没有阻焊膜的电路板更容易回流。
*   **走线宽度:**同样，任何大于两倍位宽的东西都可以正常工作。我通常坚持 0.3 毫米的痕迹

与任何专业制作相比，这些限制当然是非常严格的，但只要稍加让步，你就一定能制作出可用且逼真的电路板。

### 平板摄像机

一旦我们确保上述所有约束都得到遵守，我们需要导出 GERBER 文件，然后将它们转换成 CNC 可以运行的 GCODE。为此，我们使用了一款优秀的开源软件: [FlatCAM](http://flatcam.org/) ，它是专门为 2D PCB CAM 流程设计的。它有一套广泛的功能，你真的应该看看。

![](img/2e2f0ebd10ec650c3442135336837078.png)

FlatCAM

关于 FlatCAM 的教程超出了本文的范围，请查阅官方文档。总之，对于您导入的每个 GERBER 文件，您可以选择为不同种类的作业生成不同的刀具轨迹，如切割、隔离铣削等。你所需要做的就是输入一些参数，指定你的切割深度和钻头尺寸。

对于单面电路板，我们需要来自 FlatCAM 的 3 个 GCODE 文件；顶层、钻孔和切割。有了这些在手，我们几乎准备好推出我们的董事会！

### 自动调平

最后一个软件步骤是通过对 FlatCAM 生成的顶层 GCODE 文件进行后处理来添加自动调平例程。为此，我们使用了另一款优秀的软件，名为[自调匀整器](https://www.autoleveller.co.uk/)，这款软件[我们早在](https://hackaday.com/2014/12/12/mill-warped-pcb-blanks-on-an-uneven-bed/)中就有介绍。

有免费版和付费版，免费版缺乏跨子任务共享探测数据的能力。这一点有些重要，因为在作业开始时，您只能探测电路板一次，也就是说，在您已经切割并因此将电路板的一部分与 PCB 包层隔离之后，您不能探测钻孔作业！老实说，我还没有觉得有必要购买完整版，因为探测只对铣削轨迹至关重要。

这个过程中最重要的参数是决定探测分辨率的探针间距。探针间距越小，探测的点越多。虽然这需要一段时间，但为了取得好的效果，至少做 80-100 次是值得的。一旦这个文件生成，它将取代我们旧的顶层 Gcode 文件，我们就可以开始制作我们的电路板了！

## 磨出来

在这一点上，我们将有 3 个文件为我们的单层板:顶层文件与探测，钻孔文件和最后的轮廓铣削文件。我们从铣削顶层文件开始。启动你最喜欢的 GCODE 解释器/CNC 控制器，我用 MACH-3，但 Linux CNC 或其他大多数都是可行的选择。

我们首先将所有 3 个轴归位，将主轴定位在 PCB 一角上方大约几毫米处，并将所有 3 个轴归零。重要的是不要忘记不同工作之间的 X-Y 零点位置。每个新任务都需要在 Z 轴上重新调零，但 X 和 Y 零点位置不会改变。确保探测电路设置正确，否则研磨机会撞上 PCB！一旦我们开始工作，工厂就应该开始例行的探查。一旦完成，铣削程序将开始，取决于你的进给速度和走刀次数，这通常需要一段时间。一旦完成，我们的板应该有望类似我们的设计，尽管混杂着玻璃纤维粉末。

接下来，我们继续钻孔，这一步不需要精确的重新调平。我们只需插入钻头，将 Z 轴调零，使钻头与 PCB 表面齐平。完成后，所有指定的孔都应钻入板中。

最后但同样重要的是，电路板需要从 PCB 覆层的其余部分切割下来。该过程与上一步非常相似，只是钻头不同，进给速度较慢。我们再次将 Z 轴归零，让作业运行。如果一切顺利，我们应该有成品 PCB！

 [![Isolation Milling](img/68c30b51f7080f18a938401df4fd82a6.png "milling-pcbs-iso-done")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170401_145557/) Isolation Milling [![Drilling](img/6ff4f3f906e298ec10fd5728de939cb9.png "milling-pcbs-drill-done")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170401_150319/) Drilling [![Cut out](img/6cd33e45d18f3f3d7f0ba5ac37699a73.png "milling-pcbs-cut-done")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170401_151217/) Cut out

## 收尾工作和组装

现在来看看这个过程中更有意义的部分。铣削过程并不完美，尤其是当雕刻钻头变钝时，它往往会撕裂而不是切割。要清除散落的铜屑，先用粗毛刷擦洗 PCB，然后用较细的砂纸。最后用酒精擦拭后，我们终于可以把元件焊接上去了！

 [![Close up](img/359771d4c3b5861a5a869ae80f93e465.png "milling-pcb-closeup")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170401_155453/) Close up [![All done](img/7056fa836c117c467f4218ccf92f7051.png "milling-pcbs-all-done")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170401_154643/) All done [![Components soldered on](img/87a24831ffdc2498bc2170e6de33bcad.png "milling-pcbs-soldering-done")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20170401_200808/) Components soldered on

看看最后的结果。它看起来很好，虽然你可以看到一些缺陷，如在实际的痕迹之间残留的铜痕迹。这些应该不是问题，因为我们规定了走线和浇注之间足够的间隙！

## 下一步怎么样

现在你可能想知道这个过程是否适用于双面板？答案是肯定的。虽然对齐两边可能有点麻烦，但通过正确的练习和夹具，这不会太难。

事实上，FlatCAM 提供了一种为对齐 2 层设计而钻对齐孔的方法。最后，您可能还想知道这个复杂的工作流程是否能为要求苛刻的足迹产生一致的结果。答案还是，是的。我已经生产了多个电路板，用于 DFN-8 (3 mm * 3 mm * 8 引脚！)在单次运行中！查看这款基于 DFN-8 中 LTC5560 IC 的 1 GHz 混频器。

 [![DFN-8 vs 0.7mm Pen](img/8f7595ee7448aef2827aa8fc358dca75.png "20171225_195707")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20171225_195707-3/) DFN-8 vs 0.7mm Pen [![Closeup](img/5e776e5bb693a83946b7c6e7bba63968.png "20171225_195707-closeup")](https://hackaday.com/2018/01/04/guide-why-etch-when-you-can-mill/20171225_195707-closeup/) Closeup