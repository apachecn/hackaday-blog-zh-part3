# 在所有产品中创建 PCB:在 Fritzing 中创建定制零件

> 原文：<https://hackaday.com/2017/01/06/creating-a-pcb-in-everything-creating-a-custom-part-in-fritzing/>

这是我在各种 EDA 工具中创建原理图和 PCB 的一系列帖子的继续。我们已经看过了 [Eagle CAD](http://hackaday.com/2016/09/22/making-a-pcb-eagle-part-1/) 、 [KiCad](http://hackaday.com/2016/11/17/creating-a-pcb-in-everything-kicad-part-1/) ，并且带着 [Protel Autotrax](http://hackaday.com/2016/11/10/creating-a-pcb-in-everything-protel-autotrax/) 的 IBM PC 的首批 PCB 设计工具之一走过了记忆之路。这些教程中最有争议的一个是我在 Fritzing 上的帖子。Fritzing 是一个可怕的工具，你不应该使用，但在我开始之前，我需要备份和解释这一系列的职位是什么。

这一系列帖子的简介把它展示得非常清楚。在本系列的每篇文章中，我都将引用一个支持 USB 的小型 ATtiny85 开发板的参考原理图。我重新创建原理图，重新创建电路板，并在每一个软件中构建一个新的符号和足迹。最后一部分——制作一个新的符号和足迹——是 Fritzing 用户争论的焦点。[你不能在烧结中创造一个全新的零件](http://blog.fritzing.org/2012/10/09/new-parts-editor-released/)。这是直接从开发者那里引用的。对于一个 PCB 设计工具来说，这是一个令人困惑的决定，不知道现在还能不能称 Fritzing 为 PCB 设计工具。

### 将整个混乱联系起来

如果你像大多数台式机或笔记本电脑用户一样，制作像素艺术最简单的工具是微软画图。使用 MS Paint，您可以编辑单个像素，选择颜色，甚至进行整体填充。如果你想用一个易于使用的工具快速创建像素艺术，这正是你所需要的。不过，有更好的工具来创建像素艺术。Photoshop 可以让你放大看到单个像素，并具有透明度和图层，而 [Aseprite](https://www.aseprite.org/) 是专门为像素艺术的创作和动画设计的专业工具。

很容易将 KiCad、Fritzing、MS Paint、Photoshop 和 Aseprite 相提并论。Fritzing 和 MS Paint 是简单易学的工具，您可以快速生成可接受的结果。然而，这是一个错误的等价关系；在 MS Paint 中你可以做任何你想做的事情，但是在 Fritzing *中你不能做任何你想做的事情，因为你不能添加自定义部件*。如果 MS Paint 没有蓝色，Fritzing 就是一个类似 MS Paint 的工具。

创建定制器件是 PCB 设计工具的必要功能。[首款面向 PC 发布的 PCB 设计工具具备这一功能](http://hackaday.com/2016/11/10/creating-a-pcb-in-everything-protel-autotrax/)。如果不能创建定制器件，Fritzing 就不能合法地称自己为 PCB 设计工具，也不应该这样使用。

### 当然，你可以定制零件(这很乏味)

Fritzing 常见问题是错误的。当然，您可以在 Fritzing 中定制零件。今年夏天，Adafruit 创建了一大堆尚未添加到核心库中的 Fritzing 部件。与其抱怨相对较小的核心库，或者添加自定义部件的困难，我将做一些更好的事情:在接下来的两千字中，我将演示如何在 Fritzing 中创建一个自定义部件。

需要注意的是，自从 0.7.9 版(该版本取消了创建定制零件的功能)中引入了新的 Fritzing 零件编辑器之后，就没有关于如何在 Fritzing 中创建定制零件的教程了。这是第一个这样的教程，也是最好的在 Fritzing 中创建定制零件的教程。我鼓励 Fritzing 团队在他们的博客和 FAQ 上发布这个教程的链接。

有了为什么你不应该使用 Fritzing 和为什么这个教程是必要的理由，让我们开始。这就是在 Fritzing 中创建定制零件的方法。

### 简单又愚蠢的方法

[![proof](img/78d23f5103fa311b53e3c5b06d1f7287.png)](https://hackaday.com/wp-content/uploads/2016/12/proof.png)

上图是 ATtiny2313，是 Fritzing core 库中的一个零件*而不是*。我用 Fritzing 内置的工具在几分钟内创建了这个部件。是的，你可以在 Fritzing 制作你自己的零件。我是这样做的。

[![edit-a-part](img/b20825df801b43aa961933ef618a272d.png)](https://hackaday.com/wp-content/uploads/2016/12/edit-a-part.png) 从 Fritzing 的“核心部件”选择器中，取出通用 ic 部件并将其放到试验板视图上。在 Inspector 窗口中，您会发现该部件的封装类型、引脚数量、标签，甚至引脚间距等选项。如果你想把 40 针 CERDIP 6502 放入你的 Fritzing 项目，你可以这样做。如果你想把 64 针的摩托罗拉 68000 放入你的 Fritzing 项目*中，你可以这样做。*如果出于某种原因，你想添加一个不在核心 Fritzing 库中的 IC，你也可以这样做。所有这些都是通过烧结半自动完成的。你需要做的就是告诉 Fritzing 针的数量，以及它的包装。

[![newpartsed](img/902c9eaf4100624e2e0e75347a2e97a0.png)](https://hackaday.com/wp-content/uploads/2016/12/newpartsed1.png)

底线是什么？如果你处理的是 DIP 芯片、QFN、SOIC 或其他标准封装，*你大概可以在大约三分钟内制作一个熔结部件*。这是从零开始制造零件吗？不，但是对于大多数用例，这就是你所需要的。

* * *

### 实际上是从零开始创造一个零件

本教程的挑战是从头开始创建一个零件。为此，我打算打造一款紫金 64 针 DIP 摩托罗拉 68000。为什么不呢，对吗？

[![The relevant documentation from the 68000 datasheet.](img/829a7bbde0f8022b1e2d46a08ffc578e.png)](https://hackaday.com/wp-content/uploads/2016/12/purpleandgold.png)

The relevant documentation from the 68000 datasheet.

### 步骤 1:创建试验板足迹

下载 [Inkscape](https://inkscape.org/en/) 。它就像 Illustrator，只不过它不会把你的灵魂送回土坯母舰。选择文件- >文档属性，并将画布的大小设置为 3.2 x .98 英寸。在该窗口中，将默认测量单位设置为“英寸”。

画布的宽度是封装的标称宽度，高度是封装的标称高度*加上引脚的空间*。大头针将是尺寸为 0.04 x 0.04 英寸的正方形，因此在画布的顶部和底部添加 0.08 英寸。

根据画布的尺寸，画一个矩形。如果你觉得特别有艺术感，就把矩形变成紫色，再加点金色。现在是添加引脚的时候了。这是一个 64 针设备，所以加上 64 个矩形。使用 Inkscape 对它们进行逻辑排列和分发。在 Inkscape 的“对象属性”窗口中(Shift+Ctrl+O)，将每个矩形的 ID 设置为“connector0pin”到“connector63pin”。是的，Fritzing 使用零索引数字来标记试验板视图上的所有引脚。

[![connector3pin](img/b310964864200854c788834d12b653d9.png)](https://hackaday.com/wp-content/uploads/2016/12/connector3pin.png)

一旦所有的引脚都被标记，选择所有，分组所有的东西，并在对象属性窗口中命名这个组为“试验板”。将这个文件以普通的 SVG 格式保存到你的桌面上(不是一个 *Inkscape* SVG)。这就是构建试验板部分的墨迹部分。现在我们把它带到 Fritzing。

在 Fritzing，创造一个新的部分，就像你在'简单，愚蠢的方式'以上。在部件编辑器中，选择 File -> Load Image For View，并选择刚刚从 Inkscape 中保存的 SVG。你会得到类似这样的东西:

[![newpartseditor68k](img/4925d07cf97ae9cfe90be14a3e2ada00.png)](https://hackaday.com/wp-content/uploads/2016/12/newpartseditor68k.png)

是的，字体变了，但是*随便*。这是任何人在 Fritzing 中最接近定制零件的一次。在屏幕的右侧，有一个连接器列表，每个引脚旁边有一个标有“选择图形”的按钮。对于我们 64 针怪物上的每个引脚，单击“选择图形”按钮，然后单击相应引脚的灰色矩形。如果您在 Fritzing 中正确标记了您的零件，这应该是不必要的，但这是您的另一个选择。

保存零件，打开一个新的 Fritzing 窗口，下面是您得到的结果:

[![fritzing68k](img/5c009578dad74e72ab2fa5b46e64f4fb.png)](https://hackaday.com/wp-content/uploads/2016/12/fritzing68k.png)

再次重申，这是一个自定义部件，具有自定义试验板视图。没有其他教程告诉你如何做到这一点。不客气

### 步骤 2:创建原理图示意图

面包板视图只是制作 Fritzing 所需的三分之一。现在我们将转向示意图。这是器件的简化视图，显示了所有引脚的功能。

[![schematicview](img/ac3352d6c29dd19d2e79305e93b2e98b.png)](https://hackaday.com/wp-content/uploads/2016/12/schematicview.png) 首先，新建一个宽 1.5 英寸、高 3.3 英寸的 Inkscape 文档。如果要制作 DIP 原理图，则计算器件高度的公式为([一边的引脚数] + 1) * 0.1。对于一侧有 32 个引脚的 64 引脚芯片，它是 33*0.1 = 3.3。

示意图的主体是矩形，无填充，黑色轮廓，描边宽度为 1px。针脚是一条 0.25 英寸长的直线，沿着黑色矩形的边以 0.1 英寸为中心排列。

现在，我们有了示意图的简化版本。是的，我们遗漏了所有引脚的标签，但遗漏了更重要的东西:IC 端子，或者原理图上线路连接的位置。Fritzing 认为这些应该是 0.2 像素见方的矩形(是的，*点两个像素*，所以我们需要将这些添加到这个足迹上的每个引脚的末端。

在原理图的每条边的尖端创建一个 0.2 乘 0.2 *像素*的矩形，并在对象属性对话框中将其标记为“连接器 0 端子”到“连接器 63 端子”。完成后，在“对象属性”对话框中，将管脚标记为“连接器 0 管脚”到“连接器 63 管脚”。是的，那是你需要重新命名的一百二十八件事物。需要一段时间。完成后，将其保存为 SVG，进入 fritzing 中的零件编辑器，选择 File - > Load Image For View，并选择刚刚在 Inkscape 中创建的文件。以下是您将获得的内容:

[![schematicviewfritz](img/36fe8a41a726922cf4ca90fffc7edbec.png)](https://hackaday.com/wp-content/uploads/2016/12/schematicviewfritz.png)

我在这个示意图中添加了一些东西，最明显的是引脚标签。除此之外，它是非常标准的，现在我们几乎已经完成了在 Fritzing 中从零开始创建一个部件。

### 步骤 3:创建 PCB 封装

你现在知道该怎么做了。创建新的 Inkscape 文档。画布的尺寸为(包装的宽度+ 0.02 英寸)×(包装的高度+ 0.02 英寸)。68000 的尺寸是 3.22 英寸乘以 0.92 英寸。你的垫只是圆圈，没有填充，和某种黄色的中风。排列这些便笺簿是留给读者的练习。

熔结要求您命名这些焊盘，因此将其命名为“连接器 0 引脚”到“连接器 63 引脚”。将所有这些焊盘分组，并将该组称为“铜 0”，然后再次分组，并将组称为“铜 1”。表面上，这是针对顶部和底部铜层的。

[![inkscapepads](img/2f294c2f1dc3e5e227607be19e91c981.png)](https://hackaday.com/wp-content/uploads/2016/12/inkscapepads.png)

将其保存为常规 SVG，打开 Fritzing，进入器件编辑器，用刚才保存的 SVG 替换 PCB 封装。

[![fritzingpcbfinished](img/46f25b66028211eb28c09440e8e039d0.png)](https://hackaday.com/wp-content/uploads/2016/12/fritzingpcbfinished.png)

就这样，我们结束了。这就是在烧结过程中如何从零开始制作零件*主要是*。点击保存，关闭 Fritzing，把你的电脑扔进垃圾箱。现在已经被污染了。

### 这一切意味着什么

[![The Fritzing breadboard layout of the Lilipad Mini.](img/b19ec39027b329a5afd536744e4e5cfd.png)](https://hackaday.com/wp-content/uploads/2017/01/lilipad.png)

The Fritzing breadboard layout of the Lilypad Arduino. Yes, this is a Fritzing part, made from scratch.

不可否认，我在 Fritzing 中从头创建了一个 64 针 DIP *并没有让自己变得容易。在烧结中制作零件是一个繁琐的过程，不应该由任何人来做。不过，这是可能的，如果你有足够的时间，你可以在 Fritzing 中创建漂亮的矢量图形，这些图形也是真实的工作部件。*

Fritzing 的支持者说，它最大的优点是，它是一个易于使用的工具，如果你想快速制作一个原型 PCB，它很有用。它们是正确的，只要您想要使用的所有部件都已经在 Fritzing 的核心库中。从头开始创建器件是可能的，但这是一项在任何 PCB 设计程序中都可以更快完成的任务。我们现在看到的是一个有围墙的花园问题，对于第二流行的开源 PCB 设计软件来说，这没有任何好处。

然而，应该注意的是，制造烧结部件所需的许多任务是可以自动化的。PCB 和原理图封装可以自动生成。理论上，一个简单的命令行工具可以将这些器件直接与试验板封装联系起来。如果有人想以一种有意义的方式为开源做出贡献，有一个项目适合你:制作一个工具，将一个芯片或组件的 SVG 转换成 Fritzing 部分。

结束这篇教程，我想感谢[Arsenijs]创建了第一篇关于在 hack aday . io 上制作 Fritzing part 的教程。(Arsenijs)这样做是因为我为第一个从头开始制作 Fritzing 的指南提供了奖金。我不仅为开源做出贡献(这意味着我比你强)，我还为开源*文档做出贡献。*我是会下金蛋的独角兽。

油炸就这样了。我不会再碰它了。在这个*系列的下一篇文章中，我将看看基于云的 PCB 设计工具， [Upverter](https://upverter.com/) 。会比油炸好吗？谁知道呢。也许吧。大概吧。*