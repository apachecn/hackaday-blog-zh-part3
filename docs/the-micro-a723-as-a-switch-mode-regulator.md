# UA723 作为开关模式调节器

> 原文：<https://hackaday.com/2018/02/15/the-micro-a723-as-a-switch-mode-regulator/>

如果您是一名电子工程师或接受过超出最基础的电子教育，您很有可能会熟悉飞兆μA723。这种芯片由传奇人物 Bob Widlar 设计，并于 1967 年发布，是一种用于构建各种电压调节器的套件。除了是一个非常有用的设备之外，它的长寿可能要归功于它作为教学范例出现在保罗·霍洛维茨和温菲尔德·希尔的开创性著作《电子艺术》中。这是我最喜欢的芯片，我已经在《T3》和其他地方写了很多关于 T2 的文章。

[![The Fairchild switching regulator circuit. From the μA723 data sheet in their 1973 linear IC databook, page 194 onwards.](img/fe377200b3a4f3d68d61ef3c8bdeae49.png)](https://hackaday.com/wp-content/uploads/2018/01/723-fairchild-data-sheet-switcher1-rethemed.jpg)

The Fairchild switching regulator circuit. From the μA723 data sheet in their [1973 linear IC databook](https://archive.org/details/bitsavers_fairchilddldLinearIntegratedCircuitsDataCatalog_30443462), page 194 onwards.

几十年来，我一直在用μA723 做实验，但它的数据手册上有一个有趣的电路是我从未有机会构建的。飞兆半导体原始数据手册上的图 9 是一个开关调节器，一个降压转换器，使用一对 PNP 晶体管以及您所期望的二极管和电感。它的性能几乎肯定会被大量最新的专用转换器芯片超越，但它仍然是我从未构建过的μA723 电路。显然，必须采取措施来纠正这种情况。

查看电路并参考数据手册，很明显，μA723 通过 1mω电阻 R4 提供的反馈配置为振荡器。额外的环路增益由 PNP 达林顿外部晶体管对和μA723 的内部输出晶体管共同提供，脉宽调制通过内部比较器实现，内部比较器将反相输入端的输出电压与通过 R1 和 R2 获得的基准电压进行比较。由此产生的振荡将电流切换到由 D1、L1 和 C2 组成的网络中，形成了一个典型的降压转换器。

## 重新开始旧的电路设计

自该数据手册发布以来已经过去了 50 年，在此期间，电子行业的发展已经到了今天的许多元件对于 20 世纪 60 年代的工程师来说已经面目全非的程度。电阻和电容执行相同的功能，但μA723 是半导体目录中罕见的幸存者，而两个晶体管和二极管已成为历史。与此同时，有太多现成的绕线电感器来代替原来建议的手动绕线电感器。

为了打造 2018 年的μA723 切换器，有必要对 1967 年的现代等效器件进行一些搜索。对于半导体而言，这意味着要查看原始器件的数据手册，并以相似的增益、电流处理能力、功耗和速度匹配现代器件。我选定 2N4403 作为 2N5545 的替代产品，并选定 MPS751 作为 2N5153 的等效产品，尽管由于晶体管在 50 年里有了如此大的进步，我可以从许多其他产品中选择。你可能认为二极管是快速整流器，我选择了 1N4837。最新的[德州仪器(ti)数据手册](http://www.ti.com/lit/ds/symlink/ua723.pdf)有一个意想不到的选择，虽然是 1N4005 通用整流器，所以速度可能并不那么重要。适合小型降压转换器的电感有多家制造商，[我选择的太阳光电第一部分](http://ds3.yuden.co.jp/TYCOMPAS/eu/detail.do?productNo=LHL10TB122J&dataUnit=M)只是其中之一。

[![My take on the 723 switcher, on a Boldport Club board.](img/a62bd96751085061e199ee294cc788fe.png)](https://hackaday.com/wp-content/uploads/2018/01/723-widlar-board.jpg)

My take on the μA723 switcher, on a Boldport Club board.

构建电路利用了最近的 [Boldport Club](http://www.boldport.club/) 项目、μA723 开发板和 Widlar 贡品。经常阅读 Hackaday 的读者会知道 Boldport 的 Saar Drimer，因为他独特的艺术 PCB 设计，Widlar 项目是他审美的典型代表。切换器带它稍微*场外*，但董事会已被设计为适应任何电路。是时候进行一点负责任的披露了:这是一块我非常熟悉的板，因为几个月前萨尔设计它的时候让我写它的说明。

我对原型构造的理解有点粗糙，如果冒犯了你微妙的电子敏感，我道歉。电路板上的通孔和焊盘的混合，用来支撑零零碎碎的元件蜘蛛网，这并不十分美观。它将基准电压分压器 R1/R2 及相关元件置于μA723 的左侧，电感和二极管置于其上方，两个晶体管置于其右侧。分压器选择 5 V 输出，1mω反馈电阻以笨拙的方式在芯片顶部形成环路。

## 部分成功

令人惊讶的是，我的μA723 切换器在第一次开启时就工作正常，从 12 V 输入向 50ω负载提供 5.01 V DC 输出。连接示波器揭示了该调节器的另一面，并展示了为什么在这种配置中很少看到μA723。

[![The yellow trace shows ripple on the DC output, while the blue one shows the waveform at the transistor collectors.](img/5a8bdbf9f9eafaa3f84aeb1d0b6dbd99.png)](https://hackaday.com/wp-content/uploads/2018/01/ds1z_quickprint1.png)

The yellow trace shows ripple on the DC output, while the blue one shows the waveform at the transistor collectors.

右侧截图中的黄色轨迹显示了 DC 输出的纹波，而蓝色轨迹显示了晶体管集电极的波形。该电路的振荡频率略高于 100 kHz，高于预期，直到人们意识到整个电路是自由运行的，其频率仅由其环路的特性决定，而不是像最近的设计那样由单独的振荡器产生。

DC 输出端的 260 mV 峰峰值纹波是该电路的杀手，对于大多数要求不高的应用来说，这是一个不可接受的高值。它提供了一个客观的教训，说明最近的器件在如何处理 PWM 产生方面投入了大量的思考，从而提高了这方面的性能。我强烈建议任何对这个话题感兴趣的人阅读一下 Jim Williams 写的[线性技术应用笔记](http://www.linear.com/designtools/app_notes.php)，尤其是 [AN35](http://cds.linear.com/docs/en/application-note/an35f.pdf) 和 [AN29](http://cds.linear.com/docs/en/application-note/an29f.pdf) 。尽管自由振荡μA723 产生相当基本的 PWM，但很容易看出占空比随条件而变化。将输入电压降低到大约 9 V 的相当高的值，在其开始失去调节之前，占空比从 50%增加到大约 70%。

因此，μA723 不是开关调节器的明星，这并不奇怪。该电路的另一个特点是完全不适合现代环境，因为它是一个功率稍大的 100 kHz 源，会产生大量 RF 辐射。范围内任何地方的调幅收音机一开机就被切断，让人想起一些老式阴极射线管电视机的效果。这不太可能通过 EMC 测试。

这是对开关调节器结构的一次有趣尝试，也是填补μA723 数据手册最后一个空白的机会。这是一个可行的设计，但人们有一种感觉，它进入数据手册是因为芯片有能力，而不是因为即使按照 1967 年的标准，这也是一个明智的选择。人们想知道这是否是 Bob Widlar 的一次硬件黑客攻击，将芯片推至其设计之外，自那以来，μA723 的每一份数据手册都超出了预期。如果是这样的话，那么我比喻性地向他脱帽致敬，如果我是这篇文章的作者，我就不会有勇气发表这篇文章。