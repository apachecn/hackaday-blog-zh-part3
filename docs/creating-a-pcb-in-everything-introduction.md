# 在所有事物中创建 PCB:简介

> 原文：<https://hackaday.com/2016/09/21/creating-a-pcb-in-everything-introduction/>

[![engineering-drawing](img/fd0c3a180c9e5ab20b38e591ee9ecf77.png)](https://hackaday.com/wp-content/uploads/2016/09/engineering-drawing.png) 几年前，我写过几篇题为 *[做一件事](http://hackaday.com/2014/01/22/3d-printering-making-a-thing-in-autodesk-123d/)的专栏。这些专栏是几个不同 3D 建模程序的指南。本专栏并不打算成为在 OpenSCAD 或 SolidWorks 中建模一个对象的完整指南，它只是一步一步地说明如何用一个特定的软件制作一个特定的东西。*

Hackaday 社区中不少人认为这个专栏很有用，或者至少是一个有趣的教学工具。当开始使用任何一种生产力软件时，你不需要知道如何做所有的事情，你只需要知道如何做最常见的任务。

既然*制作一个东西*专栏如此受欢迎，我觉得是时候用我们经常面临的另一个设计任务来恢复这个想法了。正如你已经猜到的，我们将生产印刷电路板。延续本专栏前一篇文章中创建的独特教程格式，*制作 PCB* 将在多个 EDA 套件中构建一个特定电路。

### 该电路

演示如何在一个特定的软件包中构建一个东西的整个概念需要一个模型。在我开始写第一篇*制作 PCB* 专栏之前，我需要设计一些足够复杂但仍然相对简单的东西，并且希望有些用处。分线板非常简单，也许太多了。在这些程序的过程中，我需要演示如何在每个特定的软件套件中制作一个部件，因此引脚越少越好。

由于缺乏自己的创造力，我决定从 Tim a.k.a. [cpldcpu]开发一款非常小的 ATtiny85 Arduino 衍生产品。 [Tim 的 Nanite 85](https://cpldcpu.wordpress.com/2014/04/25/the-nanite-85/) 是一款基于 ATtiny85 的非常小的 Arduino 兼容板，配有一个 USB 端口、LED 和几个 I/O 引脚。它简单但足够复杂，足以介绍 PCB 设计套件。

不过，我不会直接复制 Tim 的 Nanite 85。如果各部分不堆叠在一起，会清楚得多，我想在布局上给自己一点喘息的空间。我重新设计了 Nanite 85 的电路，在稍大的电路板上主要使用通孔部件。我称我的版本为纳尼特·韦斯利(T1)，如果你得到了那个参考，为你竖起大拇指。

[![ThingPCBSch](img/4e75d192739b533f820de54fa716e56e.png)](https://hackaday.com/wp-content/uploads/2016/08/thingpcbsch.png)

The schematic for the Nanite Wesley

[![naniteboard](img/f8cd1b2eaf8d411e05d42fdadbf2be29.png)](https://hackaday.com/wp-content/uploads/2016/09/naniteboard.png)

The Nanite Wesley board. Copper pours not shown

棋盘应该是这样布置的吗？不，绝对不行。我也许可以把它作为一个单层板来做。这是一个非常低效的布局，我喜欢我的板上有圆角。不过，这已经足够好了，而且很有效。这是如何使用 PCB 设计包的指南，而不是如何设计 PCB 的指南。你在这方面的批评被记录下来并被忽略。

### 这些教程将包括什么

除非你知道如何制作一个零件，否则你不能使用 PCB 设计包。是的，Eagle 拥有几乎所有你能想象到的精彩库，KiCad 在互联网上有大量的零件，如果你使用基于云的 PCB 软件，几乎所有东西都会为你提供。如果你制作一个 PCB，最终你将不得不制作你自己的部分，每个教程都将从制作 DIP-8 at nin 85 开始。这块板上的其他东西都是软糖。不管怎样，齐纳二极管的零件和封装制作过程与微控制器是一样的。

教程的下一部分将包括原理图捕获。这意味着在原理图中放置器件，在引脚和焊盘之间绘制导线，并命名它们。从那里，是时候实际制作电路板了，这意味着放下零件，在所有引脚之间放置走线，绘制电路板轮廓，浇注铜，以及机械方面的考虑。

随着原理图和电路板的设计，是时候把它送到工厂了。对于 Eagle 和 KiCad 来说，这很容易；OSHpark 接受鹰。brd 和 KiCad。pcb 文件，但这是作弊。我们将使用 CAM 来生成真正的 Gerber 文件。如果你制造了足够多的 PCB，你最终将不得不学习它。

### 警告和糟糕的设计

制作“合适”的 PCB 有很多因素，包括隔离、直接走线到去耦电容、确保 pixies 不会绕过尖角，以及其他一千多项不会在这些教程中讨论的因素。我不讨论这个是有原因的。这是关于如何使用 PCB 设计工具的指南，而不是如何设计 PCB。

### 我还应该做什么？

正如您可能从上面的原理图中猜到的，我要介绍的第一个 PCB 软件是 Eagle。KiCad 榜上有名，还有 Fritzing、Altium CircuitMaker 和 OrCAD。为了将 PCB 设计放在历史背景中，我有一份 AutoTRAX 和一台旧的 DOS 机。我还将介绍一些纯云设计工具，比如 Upverter。

这是足够的软件套件来开始，但正如*制作一个东西*系列，我将从花生画廊寻找建议。我不能改变我正在制作的电路，因为这是这个系列的整个要点，但我正在寻找其他工具的建议。我还能做什么？要我拿一块覆铜板、贴纸和一些感光胶片吗？我能做到。你是否在一家基于网络的 EDA 创业公司，想要一些免费广告？请在评论中留言。

由于我们努力慢慢改进 Hackaday 的后端，你将能够从下面的系列列表的[的帖子中访问所有的*制作 PCB。*](http://hackaday.com/2016/09/21/creating-a-pcb-in-everything-introduction/#series-of-posts-box)