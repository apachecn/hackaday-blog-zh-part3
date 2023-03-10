# 介绍 MENSCH 微型计算机

> 原文：<https://hackaday.com/2017/04/05/introducing-the-mensch-microcomputer/>

几周前，我在我的一个每日拖网上浏览 Tindie，寻找一些有趣的东西来写。我遇到了一些我以前没见过的东西。[Mensch 微型计算机](https://www.tindie.com/products/dcwdc/mensch-microcomputer/)是西方设计中心(WDC)的产品，它将基于 65xx 内核的微控制器放在一个小型分线板上。

[在](http://hackaday.com/2015/07/29/review-single-board-65c02-and-65c816-computers/)之前，我已经摆弄过 WDC 的一些工具和玩具，那时他们给了我一些开发板让我查看。它们很酷，我已经考虑过为微控制器和片上系统之间的这种奇怪的交叉建立一个小的分线板。生活碍事，那个项目就搁置了。然而，Mensch 很便宜，很适合冲动购买。在买了一台之后，WDC 的一位副总裁问我是否有兴趣对他们最新的硬件再做一次评估。当然可以。我明白了。

### WDC 目录的简要概述及其重要性

西部设计中心是 65xx 系列 CPU 及相关外围芯片的承担者。如果你曾经用过 Apple II、任天堂娱乐系统、Atari 8 位、Commodore 64、电子鸡，或者 met Bender Bending Rodriguez 或 T-800 Terminator，你会遇到 6502 或其他足够相似的东西，任何差异都是学术上的。

65816 是 6502 的后续芯片，可以在超级任天堂和苹果 IIgs 中找到。这个芯片很奇怪；启动时，它*是* a 6502。用两条指令翻转寄存器中的一位，你就有了 16 位寄存器、24 位地址空间和一堆其它你无法装进 3500 个晶体管的东西。816 是那种如果早几年问世就会改变世界的芯片，但那是另一个时代的故事了。如果你想建立自己的基于 6502 的单板计算机，我强烈建议你看看 65816。

任天堂、Commodores 和 Ataris 运行 6502 的日子已经一去不复返了，但 65xx ISA 仍然存在。它存在于从玩具到生命支持设备到航空航天的所有东西中，如果你想玩这些设备，你需要学习一些 6502 组装。想要证据吗？有史以来最伟大的黑客——[[Sprite _ TM]的电子鸡矩阵](http://hackaday.com/2015/11/24/building-the-infinite-matrix-of-tamagotchis/)——只是一个模拟几个 6502 内核的服务器。

这些奇怪的设备显然没有使用完整的 DIP40s 和相关的支持芯片。相反，他们要么使用带有授权 65xx 内核的定制 ASICs，要么使用 WDC 的微控制器产品之一。 [65C134SXB](http://wdc65xx.com/boards/w65c134sxb-engineering-development-system/) (基于’02)和 [W65C265SXB](http://wdc65xx.com/65xx-store/sxb-boards/w65c265sxb-engineering-development-system/) (基于 65c816)是微控制器和片上系统交汇处的小芯片。这就把我们带到了 WDC 的最新产品，即 [W65C265WBX](http://wdc65xx.com/w65c265qbx-mensch-microcomputer-educational-sbc/) ，即 Mensch 微型计算机。

[![](img/7f89ecc5bf0dcce5715c0b1010ba9e59.png)](https://hackaday.com/wp-content/uploads/2017/03/menschbreak.jpg)

### 挖掘男人

[![](img/aa7730ecf9f381fddb106d8ceedb7c38.png)](https://hackaday.com/wp-content/uploads/2017/03/2651.png)

The W65C265SXB – the bigger version of the Mensch

Mensch 微型计算机是围绕 65C265 构建的，而 65c 265 本身是围绕 65816 构建的微控制器。这是一个小电路板，只有微控制器、几个无源器件、八个发光二极管和几个接头。实际上，这是 WDC 基于 816 的微处理器的分线板，只需要最少的东西就可以运行。我们现在看到的是我不久前看过的 816 微控制器开发板的简化版。

这是 65C265 的分线板。在板上，您有一个完整的 816 内核、一个监视器 ROM、一点点 RAM、几个串行端口、一组 led，以及对 16 条地址线和 8 条数据线的访问。如果你想为 6502 或 65816 开发，这就是你所需要的。如果你想要更多的内存，只需抓一些 perfboard 和电线。如果你想建立一个口袋大小的 SID 播放器，为这个微小的开发平台建立一个“盾牌”。

[![](img/3fb3fae59c8cda2cd438e34ca8afad51.png)](https://hackaday.com/wp-content/uploads/2017/03/coolterm.png)

The Mensch Monitor ROM

与全尺寸的同类产品相比，Mensch 没有那么强大。W65C265SXB 是基于同一芯片的更大的微控制器开发板，在一个单独的芯片上有 32kB 的 SRAM，一个闪存芯片插座，以及一个 USB 到串行转换器。不过，这是 WDC 微控制器产品的低成本版本，任何想要构建 65xx 内核的人可能已经有了 USB 到串行转换器。

监控 ROM 正是您所期望的，允许通过终端仿真器访问芯片。在这里，你可以输入机器码，跳转到一个地址，让 led 灯随心所欲地闪烁。[可以用 Python 和这个板子](https://github.com/WesternDesignCenter/TerminalPython)对话。如果您曾经想玩 65xx 芯片，这款主板正适合您。

### 结论

[当我回顾 WDC 功能稍强的产品](http://hackaday.com/2015/07/29/review-single-board-65c02-and-65c816-computers/)时，我感叹这些单板计算机和微控制器开发板的成本。是的，它们是 6502 的最佳玩法。可以说，它们是学习汇编语言的最佳途径。然而，这是一个两美元 Arduinos 的世界，很难在价格上竞争，特别是与美国制造和组装的不含假冒芯片的电路板竞争。

尽管如此，我还是为 WDC 让他们的芯片落入更多黑客手中的努力喝彩。你仍然可以用 6502 做很多很酷的事情，如果这些年轻的黑客最终进入行业，他们可能会在职业生涯的某个时候遇到 6502 内核。这是一个不会消失的 CPU 核心，即使垂死的盖子和腐蚀的触点意味着我们的苹果 ii 和 Commodores 正在消失。这是一个很棒的小板子，我迫不及待地想看看用它会做出什么样的项目。