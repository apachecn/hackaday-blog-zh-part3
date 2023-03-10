# 莱克丝在深海中寻找暗物质

> 原文：<https://hackaday.com/2016/01/12/lux-searches-in-the-deep-for-dark-matter/>

霍姆斯特克矿于 1876 年开始生产黄金。如果你问当时的经营者乔治·赫斯特，这个矿井是否有一天会揭示宇宙的秘密，我打赌他会笑得把你赶出房间。但是毫无疑问，到 1960 年，矿井深处的一个实验室开始这样做了。自那以后的 55 年里，在那里进行了许多实验。大型地下氙(LUX)实验就是其中之一，现在被称为 T2 的桑福德地下研究设施(SURF)已经运行了大约四年。LUX 的第一轮数据是在 2013 年收集的，实验和其他数据预计在 2016 年结束。用勒克斯包装的方法、硬件和结果完全令人着迷。

### 这都是关于噪音过滤

探测暗物质极其困难。以至于我们从来没有真正做过。像 LUX 这样足够大的探测器每年只能捕捉到几次相互作用。为了确保这些不被遗漏，尽可能多地过滤掉非事件是很重要的。这就是地下位置背后的原因；4850 英尺的地球站在探测器和露天之间，以将宇宙射线减少一百万分之一。这并没有消除一切，但有可能识别错误的读数。

超纯氙气进一步过滤了系统中的噪音。留下的是一个非常黑暗的环境，等待弱相互作用大质量粒子(WIMPs)穿过它。理论告诉我们，每秒钟有数百万到数十亿的 WIMP 暗物质粒子穿过一平方厘米的空间。但是在亚原子尺度上，一平方厘米是一个巨大而空旷的空间。随着噪音被过滤掉，研究人员正在等待一个 WIMP 与一个氙核相撞。

### 检测光线

氙是一种闪烁体；当原子核被快速运动的亚原子粒子撞击时，它会释放出一个光子。电离电子也是相互作用的结果，它们反过来产生二次闪烁。初级和次级光的模式是特定于相互作用类型的，如果测量得当，可以用来区分暗物质相互作用和其他事件。好消息是我们真的很擅长测量光线。事实上，你可能已经猜到测量中使用了什么机制:光电倍增管(PMT)。

PMT 用于各种科学测量设备，也经常出现在医疗器械和摄影设备中。我们把最后这个例子看作是一个 PMT 的来源，Kerry Wong 用它来演示光速。

[![LUX-detector-diagram](img/3e2d346f5b027f27472bdab574c4ed6c.png)](https://hackaday.com/wp-content/uploads/2016/01/lux-detector-diagram.png)

LUX 的传感器阵列中有 122 个 PMT。大量的信号调节在被送入定制触发系统之前设置电平。然后事情真的开始变得有趣了。读数被汇总成 16 组 PMT，然后由触发系统处理，以确定该模式是否是一种可能的暗物质相互作用。如果你需要做很多非常快的，并行的处理，你选择什么样的硬件？你说得对，你找到了 FPGA，并围绕它构建了一个系统。

如果你正迫不及待地想了解细节，研究小组已经取得了重大进展。11 月他们发表了一篇题为 *[基于 FPGA 的勒克司暗物质实验触发系统](http://arxiv.org/pdf/1511.03541v1.pdf)* *的论文。*即使你不想挖那么深，罗切斯特大学的 Frank L.H. Wolfs 教授有一套简洁的页面[专门介绍触发硬件](http://teacher.pas.rochester.edu/LUX/Electronics/TriggerOverview.html)，它是由 [Wojtek Skulski](http://www.pas.rochester.edu/~skulski/) 设计的。

 [![LUX-event-diagram](img/1a2052252a67cb7b238f8551f54780ac.png "LUX-event-diagram")](https://hackaday.com/2016/01/12/lux-searches-in-the-deep-for-dark-matter/lux-event-diagram/)  [![DDC-8DSP](img/a40fc3f4a2f61f6c4a49174836675000.png "DDC-8DSP")](https://hackaday.com/2016/01/12/lux-searches-in-the-deep-for-dark-matter/ddc-8dsp/) 

触发脉冲数字化板的当前版本的零件号为 DDC-8DSP。其中两块板使用 Xilinx Spartan-3A 以 64 MHz、14 位分辨率采集信号。每块电路板都会收集和处理信号，然后通过 HDMI 电缆将数据发送到 Trigger Builder 电路板。这个板之所以得名，是因为它负责检查表明 WIMP 相互作用(并区别于其他相互作用)的初级和次级闪烁的特征模式。左图来自已发表的论文，说明了硬件正在寻找的信号模式。

### 成功了吗？

[!["LUX-ZEPLIN](img/1bc6932c62b1e4e34693e6ebd8cd5c59.png)](https://hackaday.com/wp-content/uploads/2016/01/lz_schematic_v2notitle1.png)

[LUX-ZEPLIN diagram](http://lz.lbl.gov/detector/)

啊，小心你问的。是的，LUX 发挥了作用，如期交付了 2013 年的第一轮数据。真正的问题是它探测到暗物质了吗？暗物质的证据还没有在数据中得到证实。但是这个，有史以来为此目的建造的最灵敏的探测器，没有浪费。研究小组已经能够进一步确定 WIMPs 不具备的特性。

该实验目前正在进行另一轮，并根据 2013 年的数据进行了进一步配置。该数据集预计将于今年 6 月准备就绪，并将是 LUX 这一迭代的最后一次运行。LUX-ZEPLIN 项目正在进行中，该项目将使用[一个更大的探测器](http://lz.lbl.gov/detector/)设备，配备更多的液态氙，传感器阵列中有 488 个 PMT，以及其他几项改进。

### 值得拥有名人地位的实验

当第一次听说 LUX 时，你可能会想起类似的探测中微子的实验，因为这两个实验都需要位于地下，以过滤宇宙噪音。中微子实验具有更高的公众形象，尽管它们可能不像大型强子对撞机那样处于名人地位。不久之后，将会有一个令人兴奋的中微子探测实验与莱克丝共享冲浪设施。

投入十亿美元建造新的[深层地下中微子实验](https://en.wikipedia.org/wiki/Deep_Underground_Neutrino_Experiment)(沙丘)，计划在 2022 年开始寻找中微子，很容易将这些类型的实验视为新的太空竞赛。毫无疑问，对实验的投资将带来技术进步，这些进步与人类进入太空的进步具有同样的变革性。拼图中缺失的一块是公众对科学发现的广泛认知和兴奋。

#### 图像来源:

*   主图:[lux dark matter Flickr](https://www.flickr.com/photos/luxdarkmatter/8058196460/)CC-BY-ND
*   缩略图:[lux dark matter Flickr](https://www.flickr.com/photos/luxdarkmatter/3950659619/)CC-BY-ND
*   缩略图:[lux dark matter Flickr](https://www.flickr.com/photos/luxdarkmatter/6901946342/)CC-BY-ND