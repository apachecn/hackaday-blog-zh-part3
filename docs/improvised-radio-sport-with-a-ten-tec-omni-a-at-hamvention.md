# 两个人，一个酒店房间和一场无线电火灾

> 原文：<https://hackaday.com/2016/05/13/improvised-radio-sport-with-a-ten-tec-omni-a-at-hamvention/>

你能在一个周末，在路上，用旧货市场的零件制造一个高频单边带无线电收发器吗？我可以，但显然不能在不放火的情况下。

当然，我指的是交易会，2016 年的交易会很快就要开始了。在之前的一次汉默文德之旅中，我和斯科特·帕斯托尔(Scott Pastor，KC8KBK)挑战自我[在代顿地区一家破旧的酒店房间](http://hackaday.com/2014/05/23/dodgy-hotel-beer-and-a-wwii-era-tube-receiver/)里修复电子管收音机设备，我们在那里修理了一台二战时期的 BC-224 和一台 Halicrafters 接收器，从 Hamfest 里搜罗零件。

我们 2014 年的冒险非常有趣，这促使我们在 2015 年创建了我们自己的黑客挑战，拼凑了一个 100 美元以下的高频单边带收发器(美国制造，以应对额外的预算压力)，一个特设的天线系统，将它播出，并在 ha vention 结束前使用在 ha vention 找到的零件和设备进行州外联系。没有时间学习手册、天线、电磁理论或真空管电路。你所拥有的就是你的 whits，一些基本的工具，和所有你能吃的华夫饼屋。但是你有一个优势，世界上最大的剩余电子产品和无线电垃圾收集地。能做到吗？

 [https://www.youtube.com/embed/i4Z_gi3THTE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/i4Z_gi3THTE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



低于 100 美元的高频收发器选项非常少，尤其是美国制造的收发器，如果有功能性的机会，这些收发器通常具有收藏价值，价值要高得多(例如 Heathkit、Drake 等)。我们可能会以一些非常早期的 SSB 装置或者可能是 70 年代末或 80 年代初的固态钻机而告终。选择余地很小。

### 选择“捐赠”收音机

![A crusty but serviceable Ten Tech Omni A for a very reasonable price.](img/00a5b9ab1929ffaa4e72866b2dc54223.png)

A crusty but serviceable Ten Tech Omni A for a very reasonable price.

周五早上，我们花 80 美元找到了一台带有阻塞的 PTO(磁导率调谐振荡器)的 Ten Tech Omni A 。这台收音机没有可选的频率计数器，而是有一个坏的计算尺调谐指示器。我喜欢它的模块化，你可以清楚地看到顶盖下的信号流。

星期五早上，斯科特以 60 美元的价格找到了一台旧的真空管供电的 Hallicrafters [SR-160](http://www.radiomuseum.org/r/hallicraft_sr_160_sr160.html) 项目收音机。不幸的是，53 岁的年龄导致一些干燥的电解质和漂移的电阻值。它确实有一些东西，它有一个电源，麦克风和我带来了我的高压帽库存，所以我们可以重新封顶。重新加帽和可能的重新对准将是耗时的。

星期五晚上，Omni-A 启动了，看起来急于运行。在 PTO 的几次快速修复尝试后，我们尝试了谷歌搜索，并意识到机械堵塞是一个非常常见的问题。固定的最好方法是完全拆开机械装置，用异丙醇浸泡，然后用锂基润滑脂润滑。没有时间完全拆卸和清洁机械装置(它类似于一个[精致的怀表](http://hackaday.com/2014/07/08/go-vintage-learn-to-repair-and-restore-mechanical-pocket-and-wrist-watches/))，我们唯一能找到的润滑剂是隔壁加油站的一小罐 WD40。在喷涂动力输出装置和用一对槽锁加工螺纹黄铜件后，它松了。这种收音机能够用一根 20 英尺长的电线从天线插孔中伸出来，收听许多单边带电台。

接下来，我们试图重新串调指示器，这不太好。所以我们最终得到了一个可以工作的收发器，但不知道它在什么频率上。我们确实考虑过将 Halicrafters VFO 引导至 Omni-A，两者都是 5 MHz VFOs，但这被放弃以支持更快的解决方案。

为了确定我们使用的频率，我们使用了一个旧的 Hammarlund [HQ-170](http://www.eham.net/reviews/detail/3807) 接收器，它是单独购买的，不属于竞争对手(当我看到一个漂亮的船锚时，很难抗拒购买)。由于 Hammarlund 使用了陶瓷圆盘电容器，这台收音机无需维修就能正常工作。我们使用 HQ-170 零击败我们的频率特权的底部范围，然后决定只回复 CQ 的或者跳入另一个正在进行的 QSO。频率感知问题解决。

### 天线:室外不是一个选项

几乎零成本，我们买了几个冷线线轴，一些随机长度的同轴电缆，和几个 WW2 剩余可变电容器，知道我们可以很容易地用废线缠绕电感。当有人免费送给我一台旧的 VSWR 仪表时，我们的原材料储备就完成了。看起来偶极天线或随机线是最好的选择。不幸的是，酒店房间的窗户打不开。由于无处可串的随机线天线，这是回到绘图板。

![First attempt at a Mag Loop transceiving antenna using RG58 coax and loop-coupling.](img/78bf32bd43a95c87ee10160f0ff92198.png)

First attempt at a Mag Loop transceiving antenna using RG58 coax and loop-coupling.

如何制作一款能在混凝土结构中工作的像样的室内天线？磁环看起来是个不错的选择。磁环对电磁场的磁场分量起作用。Mag loops 几乎用于所有的 AM 广播电台，并且经常被空间宝贵的西欧业余无线电爱好者使用。不幸的是，它们效率不高。

效率取决于工作波长下磁环导体的欧姆损耗。此外，由于环的物理孔径小，mag 环的方向性(天线增益是方向性和效率的乘积)通常很差。为了获得最佳性能，我们希望将环路做得尽可能大，以适合酒店房间的大小，并使用最粗的电缆或电线作为环路本身。

在 Hamvention 查找资料不像逛 Digi Key 目录。这是一个狩猎和采集练习。根据我的经验，很难找到一个特定的项目，在 hamventions 购物的模式更类似于“当你看到它时，你就会知道你想要什么”，而不是搜索你最喜欢的零件目录。

[![block diagram and schematic](img/a0bd23635c3d097ca6270e74845273ff.png)](https://hackaday.com/wp-content/uploads/2016/03/block-diagram-and-schematic.png)

Schematic of mag loop coupling and tuning network.

在周五晚上未能获得 RG58 的 4 '循环工作后，我周六一直在寻找替代品。10 美元购买了一段“hardline”或 heliax 同轴电缆(一种非常大的工业同轴电缆)、更大规格的连接电线和一些接线端子。现在我们有了制作一个真正的磁环所需要的一切。

我们决定使用电容耦合，而不是电感耦合。一个可变电容用于谐振回路，第二个串联用于耦合。我们使用短长度的#14 电线和端子接线片回填焊料将其连接起来。

在对最大接收机噪声的两个上限进行峰值化之后，环路在低发射功率下调谐良好，轻松实现了小于 1.5:1 的 SWR。我确实注意到，当我接触到同轴电缆时，环路失谐了。因此，我在耦合电容的正前方滚动了一个带有 10 匝 RG58 的[并联巴伦](https://www.eznec.com/Amateur/Articles/Baluns.pdf)。手电容的问题解决了，SWR 表现良好，环路现在被一条平衡线馈入。

 [![Second Loop Attempt](img/a304e9a6a54de2c6cf2fc908ae53c4ae.png "second loop attempt that worked IMG_3188")](https://hackaday.com/2016/05/13/improvised-radio-sport-with-a-ten-tec-omni-a-at-hamvention/second-loop-attempt-that-worked-img_3188/) Second Loop Attempt [![Capacitive Tuning Network](img/8257c830c57f9d30bad0695215a5a065.png "capacitive tuning network IMG_3192")](https://hackaday.com/2016/05/13/improvised-radio-sport-with-a-ten-tec-omni-a-at-hamvention/capacitive-tuning-network-img_3192/) Capacitive Tuning Network [![Second attempt at a transceiving mag loop with 3/4" hard line and a capacitive tuning and match network, this one worked quite well.](img/36f27b9ad597ab8b045553a23c92e196.png "action shot testing SWR IMG_3193")](https://hackaday.com/2016/05/13/improvised-radio-sport-with-a-ten-tec-omni-a-at-hamvention/action-shot-testing-swr-img_3193/) Second attempt at a transceiving mag loop with 3/4″ hard line and a capacitive tuning and match network, this one worked quite well.

该直播了。我们打开了全向天线的电源，打开了收音机。不幸的是，它看起来不像我们正在传输 100 瓦。酒店房间的灯甚至是收音机本身都没有闪烁。这个无线电/天线系统中似乎没有任何东西在试图传输。收音机上的输出功率计读数平平，一两瓦。

我们确实用汉穆兰确认了良好的单边带传输音频，所以有些东西出来了，但不多。在摆弄了一会儿 OmniA 之后，看起来这是一个无线电发射机的问题。作为最后的努力，查阅了 Omni-A 的手册(这不一直都是这样吗？).

自动电平控制(ALC)有点像接收机的自动增益控制(AGC ),只是它用于发射。这样，您可以获得比传输简单的线性语音单边带信号更高的平均功率。我还没有把 ALC 融入我自己制作的收音机中。愚蠢的是，由于对 Omni-A 一点都不熟悉，我们在 0 离开了 ALC 控制中心。谁有时间看手册呢？

我们把它顺时针转了 3/4 圈，不管那是什么意思。发报机启动了。酒店里的灯光变暗到 SSB 载波，收音机上的功率表显示稳定的 75+瓦。Omni A 在被忽视了几十年后工作了，多么坚固的收音机！

### 电气火灾

该直播了。当我在调谐网络附近观察到一个非常明亮的电弧时，斯科特正在以全功率进行一些“检查 1 2 3 4 测试”。为了确保我让斯科特再试一次，我观察到在磁回路的耦合电容器附近有什么东西似乎在喷火，与他的声音成比例。

调谐网络由两个非常大和旧的可变电容组成，这些是大型 WW2 剩余可变电容，其中一个使用陶瓷绝缘体，另一个由石板制成。这些应该能够处理射频电流和电压。这些帽子和相关的电线放在地毯地板上，在环的底部，靠着旅馆的床。

![IMG_3149](img/1b94a8247848c02494384fdecdbb7f42.png)

Omni A back on the air!

我用很短的 14 号铁丝把网络绑在一起。绝缘击穿电压额定为 600 伏。这是你可以在当地五金店买到的标准物品。我让斯科特再次打开收音机，同时我观察调谐网络，它就在那里！实心弧线。哇，这是一个景象。再来一次！另一条弧线。第三次，试着点着火的东西。房间里充满了烟。

它很容易被扑灭，但是烟很难闻。我们把它清理出了房间，幸运的是没有触发烟雾报警器。在检查调谐网络布线时，似乎廉价的#14 布线上的绝缘已经损坏并烧毁。为了解决这个问题，我重新调整了线路，在线路之间留出更多空间，并在网络下放置了一个酒店冰块托盘，以增加绝缘。我们顺利地重新开始了广播。

### 成功！

我们联系了佛罗里达的一个站，收到了一个 5x 7 的信号报告。够好了。

即兴广播运动使干预变得更加有趣。以前，老式的无线电接收器被赋予了生命，现在，一个零件无线电被重新广播，并进行州外联系。下一个挑战应该是什么？还有谁想去凑热闹？请在下面的评论中告诉我们。

* * *

[![gregory-charvat-bio](img/2b19f55b65f652bf9da2382fc75e0ef5.png)格雷戈里·l·查瓦特](http://glcharvat.com/Dr._Gregory_L._Charvat_Projects/About.html)博士，喜欢在短时间内将旧东西重新投入使用，是 [Humatics Corp.](http://site.humatics.com/) 的首席技术官，[小型和短程雷达系统](http://www.amazon.com/Short-Range-Practical-Approaches-Electrical-Engineering/dp/143986599X)的作者，Hyperfine Research Inc .和 Butterfly Network Inc .(都在 4catalyzer)的联合创始人，系列图书《现代和实用电气工程方法》的编辑，CNN、CBS、Sky News 等的客座评论员。作为麻省理工学院媒体实验室的访问科学家，他发明了飞行时间微波照相机。作为麻省理工学院林肯实验室的技术人员，他创建了一个穿墙雷达成像系统，该系统在 2010 年 MSS 三军雷达研讨会上获得了最佳论文，并且是麻省理工学院 Provost 办公室 2011 年的研究亮点。Greg 曾在麻省理工学院教授短期雷达课程，他的“构建小型雷达”课程是 2011 年排名第一的麻省理工学院专业教育课程，并被其他大学、实验室和私人组织广泛采用。