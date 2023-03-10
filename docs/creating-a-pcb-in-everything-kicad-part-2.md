# 在所有事物中创建 PCB:KiCad，第 2 部分

> 原文：<https://hackaday.com/2016/12/09/creating-a-pcb-in-everything-kicad-part-2/>

这是我在每一个可以想象的软件套件中创建 PCB 系列的延续。[上周，我看了一下 KiCad](http://hackaday.com/2016/11/17/creating-a-pcb-in-everything-kicad-part-1/) ，制作了一个元件的原理图，并制作了我在这些教程中使用的标准参考 PCB 的原理图。现在是时候拿着原理图，给器件分配尺寸，设计电路板了。

[![The completed schematic for our board](img/a130a4ff261494ab8d707ce0c7fc0484.png)](https://hackaday.com/wp-content/uploads/2016/11/completesch1.png)

The completed schematic for our board

所有 PCB 设计工具都有不同的方法将元件的原理图与其在成品电路板上的显示方式相关联。Eagle 使用包含元件原理图和 PCB 图的库。在 PCB 设计软件的历史中，Autotrax 完全忽略了原理图。

[![Click this button to run PCBnew](img/55cb6c72b0a547209fcaa12974efee8e.png)](https://hackaday.com/wp-content/uploads/2016/11/pcbnew1.png)

Click this button to run PCBnew

KiCad 在符号(原理图视图)和封装外形(PCB 视图)之间有明确的区分。如果我们拿着原理图，通过运行 PCBnew 创建一个新的 PCB，什么都不会发生——我们的符号与任何封装无关。

[![Click this button to run CvPCB](img/c7a97d11b13bea936d7acebd002e6f5a.png)](https://hackaday.com/wp-content/uploads/2016/11/cvpcb.png)

Click this button to run CvPCB

要将符号与足迹相关联，我们需要运行 CvPCB。这个隐藏在 KiCad 中的子程序使我们能够将封装外形与原理图符号相关联。

[![cvpcbview](img/2f058b98881f010abfdc60ae5d915600.png)](https://hackaday.com/wp-content/uploads/2016/11/cvpcbview.png)

CvPCB, with another window open allowing you to view the footprints

### 这就像云，只是不是完全没有价值

CvPCB 是 KiCad 4.0 的一个新特性。KiCad 有效地将所有足迹存储在 Github 中，而不是我们到目前为止看到的所有其他 PCB 设计工具。在 KiCad 的 [Github repo 中，你会发现一堆文件名为. pretty 的文件。这些是你能想象到的几乎每个组件的足迹。如果你正在运行一个全新安装的 KiCad，一切都会自动出现在 CvPCB 中——没有什么需要担心的，足迹*只是发生*。](https://github.com/KiCad)

这个实现有一个微妙的优点。这就像云一样，只是它是完全可验证的，如果某个部分不工作，你可以修复它并提交一个拉取请求。这已经明显优于 Eagle 范式，在 Eagle 范式中，分散在互联网上的数千个不同的库中有数百万个足迹。如果你正在按顺序阅读这个系列，请注意:当我们谈到其他基于云的 PCB 设计工具时，这个“作为云的 Github”将是一个主要的比较点。

[![viewfootprint](img/ce5c3110946152dd97e321352f1bf49c.png)](https://hackaday.com/wp-content/uploads/2016/11/viewfootprint.png) 也就是说，我们需要将示意图上的脚印与符号联系起来。为此，请进入 CvPCB 窗口中间的列表，其中包含原理图中所有元件的列表，并将封装与每个器件相关联。足迹在右边，库(或类别)在左边。要在新窗口中查看所选封装外形，单击“查看所选封装外形”按钮。

[![selecting](img/7949153d2cef5623264578812bd1df11.png)](https://hackaday.com/wp-content/uploads/2016/11/selecting.png)

Selecting a footprint for the USB port

### 让图书馆井然有序

[![](img/aa9ca06510c62edfca5307f28c4b7942.png)](https://hackaday.com/wp-content/uploads/2016/11/footprint-editor.png)

The footprint editor window

[![](img/fe6625e23a681c9068b6c467503110ef.png)](https://hackaday.com/wp-content/uploads/2016/11/footprintlauncher.png)

The footprint editor, found in the launcher

这个项目(主要)使用所有通孔器件，因此，我可以很容易地为 ATtiny85 选择一个 DIP8 封装，然后完成整个项目。*这是一个教程，不过*，我需要演示如何从头开始制作一个零件——原理图和 PCB 图。

为了制作一个封装外形，KiCad 提供了一个封装外形编辑器。这可以从 PCBnew 或启动器中访问。点击它，选择文件->新封装外形，输入该封装外形的名称(“ATtiny85”即可)，封装外形的名称和参考指示符被放置到封装外形编辑窗口中。

**[![selectfplb](img/ab4d0d7e21e92a841e5a4ea9a5b3014c.png)](https://hackaday.com/wp-content/uploads/2016/11/selectfplb.png) 库很重要**，由于 KiCad 现在运行在“并非毫无价值的云技术”上，我们必须为这个项目创建一个库，它不会与我们的标准 Github 库副本一起保存。选择 File->Save Footprint In New Library，*Save*this Library where the rest files for this project，并给这个库起一个名字。

我们刚刚创建了一个新的库，但这并不意味着 KiCad 知道我们在使用什么库。在 Footprint Editor 中，选择 Preferences-> Footprint Libraries Manager，并点击“项目特定库”选项卡。点击“追加库”按钮，将我们刚刚创建的库的路径放到“库路径”字段中。这更奇怪，但一旦我们完成了，我们终于可以创建一个足迹。

[![library-table](img/fa23359f9fe0421ebff4ec9d680dadfa.png)](https://hackaday.com/wp-content/uploads/2016/11/library-table1.png)

### 留下足迹

既然我们已经打开了封装外形编辑器，封装外形的一个部件名称和一个参考，以及库都已经设置好了，现在是时候实际放置一些焊盘了。屏幕上有几个相关的按钮:

![](img/bf1f6da13c76c1bba1fda2e52ee162d0.png)

Add a pad

![](img/6296cf88dd08015c46b19441a824a1c4.png)

Add a line

![](img/a7d5de6c50d7a814b50ff644e42d2f9d.png)

Add an arc

![](img/c9afcfa5afd09bae35504497a5f7c27d.png)

Add a circle

显然，最重要的是“添加 pad”按钮。单击该按钮，并在它们应该在的地方放下一些垫子。这是一个标准的 DIP8，即两排四个引脚相距 0.3 英寸。你可能已经注意到了，默认网格是 50 英里。

[![](img/39a12d63dbff7b6f8dfd892f8fcdd4d1.png)](https://hackaday.com/wp-content/uploads/2016/11/padproperties.png)[![](img/8c9be923011220a64cc0476e7c562169.png)](https://hackaday.com/wp-content/uploads/2016/11/footprintdone.png)

放置焊盘后，使用热键“E”编辑每个焊盘的属性。在这里，您可以将通孔零件更改为 SMD，更改焊盘、孔的尺寸以及所有东西的形状。重要的是，焊盘属性窗口允许您更改焊盘的*号*。焊盘编号是 KiCad 将零件的示意图与示意图连接起来的方式。把这件事做好，否则什么都不会起作用。

向封装外形添加几行，将您的工作保存在项目库中，然后返回原理图。你完了。这就是你留下脚印的方式。

### 从原理图到电路板

现在原理图已经有了与所有东西相关的足迹，是时候打开 PCBnew，移动器件，并在器件之间放置一些走线了。去吧。哦，什么都没出现。这是为什么呢？*您需要在原理图视图中生成一个网表，并将其导入 PCBnew* 。两个程序中都有一个写着“NET”的按钮。点击这些。现在，当网表成功导入到 PCBnew 中时，我们会得到什么？你在任何设计项目中见过的最糟糕的混乱:

[![This is fine.](img/e1d04ad14b3b528fd123988acfdab51d.png)](https://hackaday.com/wp-content/uploads/2016/11/wtf.png)

I desperately want to see someone import a netlist for a large project in KiCad.

[![movemode](img/9de79916c4017bbc46f752dbedef6f19.png)](https://hackaday.com/wp-content/uploads/2016/11/movemode.png) 我们最终会面临一个巨大的烂摊子。别担心，“M”是移动部件的热键。您也可以使用“移动足迹”模式自动放置这些零件。参考我们为[这个系列的介绍](https://hackaday.com/2016/09/21/creating-a-pcb-in-everything-introduction/)设计的 PCB，移动一些部件，直到我们得到类似下面的电路板。相关的 hokeys 是“M”代表移动,“R”代表旋转。像往常一样，有“？”热键告诉你你需要知道的一切。

[![layout1](img/111e4afaac666b429c79fbe392782225.png)](https://hackaday.com/wp-content/uploads/2016/11/layout1.png)

很近，但是看起来很恐怖。取消选择封装外形模式，使用光标，移动所有这些标签和参考。我们不需要电路板上的“CONN-01×04 ”,电阻值在它们自己的尺寸范围内真的很有帮助。做一点工作并删除这些标签，您将得到如下所示的内容:

[![layout2](img/c75c47f386461911c467139c4d79fa8b.png)](https://hackaday.com/wp-content/uploads/2016/11/layout2.png)

天啊，那看起来像是什么东西。所有的电阻和二极管都标上了它们的值，所有多余的参考都没有了，这个*其实看起来还不错。*在 Eagle 里你可不容易做到这一点。

[![layers](img/8fbe56865a1e40f88d736ce753ae05c3.png)](https://hackaday.com/wp-content/uploads/2016/11/layers.png) 跟*的布局差不多了*想通了，是时候最后画点痕迹了。这需要对各层进行描述。

*   **F.Cu** 和 **B.Cu** 是顶部和底部铜层。这些层的热键是 PgUp 和 PgDn
*   **边缘。Cuts** 相当于 Eagle 中的“铣削”层。这是你的板的轮廓。
*   F.SilkS 和 **B.SilkS** 是丝网印刷——你的组件的文本和轮廓。
*   **F .掩膜**和 **B .掩膜**就是阻焊掩膜。它通常是绿色的，或者是奥什帕克的紫色。
*   **F .粘附剂**和 **B .粘附剂**是用于贴片元件的胶水。
*   **F .焊膏**和 **B .焊膏**是要涂焊膏的地方。

对于一个不会被送到装配车间的简单电路板，你唯一需要担心的是铜层，即**边缘。切割**，并进行丝印。

完成电路板的第一件事是绘制“边缘”或铣削层。选择右边工具栏上的“添加图形线”按钮，在我们所有的部分周围画一个矩形。这很简单。

现在是时候实际上放下一些痕迹了。您可以在顶部工具栏中选择要使用的铜层，相关热键为“X”。点击“X ”,点击一些 airwires，然后像参考 PCB 一样布线。不要担心电源或接地走线，我们会用铜填充。完成后，您应该会看到这样的内容:

[![layout3](img/a713877cf57eddfe7450c0f52dc5746d.png)](https://hackaday.com/wp-content/uploads/2016/11/layout3.png)

[![filledzone](img/88459a4ec857d62a04dc1fc0d10ce193.png)](https://hackaday.com/wp-content/uploads/2016/11/filledzone.png) 除了铜钱，差不多就这些了。为此，我们需要添加一个“填充区”或“倒铜”或“多边形”。不管怎么说，它只是原理图中连接到单个网络的一大块铜。

点击“添加填充区域”按钮，将出现“铜带属性”窗口。在这里，您可以将一层铜分配给特定的信号。我们的评估板在背面铜线上加+5V 电压，在正面铜线上加 GND 电压。在铜区属性中，选择 B.Cu 层，即+5V 网，点击确定，并沿电路板边缘进行描摹。对 F.Cu 层和 GND 网做同样的操作。当这些填充变成棋盘边缘的阴影时，点击热键“B”来渲染铜填充。

[![](img/5a8f81bc6488aac28e46ab54c652a310.png)](https://hackaday.com/wp-content/uploads/2016/11/layout4.png)[![](img/5d04c1d1dc15501f833b9216f65d7466.png)](https://hackaday.com/wp-content/uploads/2016/11/copperzoneprop.png)

就是这样。我们在技术上已经完成了。如果保存并拖动*。kicad_pcb* 文件放到 OSHPark 的网页上，你会在一两周内得到一个漂亮的紫色 pcb。这并不是说这个 PCB 实际上可以工作——我搞砸了原理图中的 USB 信号，这些信号传播到了 PCB。没关系，因为没人会真的去造这种板。

KiCad 的“在一切事物中创建 PCB”教程到此结束。如果您已经阅读了最后 5000 个单词，那么您已经对 KiCad 有了很好的介绍，并且至少应该能够构建一个分线板。这并不意味着我已经完成了 KiCad——还有一些技巧需要学习，包括 DRC 和 ERC，KiCad 中的布线有多棒的演示*,无论如何，我需要在电路板上放置一个去耦电容。在所有事物中创建 PCB:KiCad 第 3 部分(可选部分)将于下周某个时候发布。*

 *### 关于 KiCad 的思考

这一系列文章有两个目的。首先，它是各种 PCB 设计工具的快速教程。读完这些文章后，你应该能够通过 PCB 设计工具猜测你的方法，并构建一个简单的 PCB。其次，这些教程都是对各种 PCB 设计工具的虚拟回顾。这些帖子中的每一个都用来说明 PCB 设计工具的古怪之处，并作为一个通知，我仍然有一笔无人认领的奖金，用于奖励第一个在 Fritzing 中从零开始为 attini 85*创造一个零件的人。别用 Fritzing，太烂了。*

来自鹰，KiCad 是彻头彻尾的怪异。不过，这并不是说它很难，它通常与任何其他 PCB 设计工具一样。像几乎所有的开源项目一样，这个界面是迟钝的，并且有五种不明显的方法来完成任何任务。从网表导入电路板的零件被挤压在一起是没有原因的。自定义库可以而且应该自动导入。KiCad 社区尤其充满敌意。用户界面有一种无形的错误，尽管在使用了几个小时后，这种错误似乎减轻了。从某种意义上说，KiCad 正是您所期望的开源项目，它已经有几十年的历史了，非常成熟，并且具有丰富的特性:它非常强大，但是对初学者来说不友好。

尽管 KiCad 初学者会很难理解这个接口，但它将是我在这一系列文章中使用的最强大的 PCB 设计工具之一。没有其他免费(啤酒)程序会给你 32 铜层和无限的布线空间。没有其他东西像 KiCad 一样使用 cloud/GitHub。太棒了。

几个月前，如果有人让我建议一个 PCB 设计工具，我会给 Eagle 或 KiCad 作为建议。Eagle 很容易学习，并且自收购 Autodesk 后会变得更好。KiCad 是健壮的，即使在 Eagle 开发的最好情况下，Autodesk 也只能达到 KiCad 的水平。

现在，我越来越喜欢凯德了。我有一个秘密项目，我需要建立和制造一千个相对复杂的董事会。我以前的首选是 Eagle，但我想我会在 KiCad 中做这个板。*