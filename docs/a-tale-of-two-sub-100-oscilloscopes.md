# 两个示波器的故事(低于 100 美元)

> 原文：<https://hackaday.com/2016/01/27/a-tale-of-two-sub-100-oscilloscopes/>

嗨，我是艾尔，我是个示波器迷。只要环顾我的办公室，我就能数出六个示波器或类似示波器的设备。我车库里还有更多。如果你数一数我拥有的望远镜的数量(从一个旧的 RCA 望远镜开始，它有一个圆形的管子和一个垂直的刻度)，这将是令人尴尬的。

另一方面，如果你想把电子聚集起来做有用的事情，示波器是必要的。你无法想象电路中发生的事情比使用示波器更好。过去，这些设备既昂贵又笨重。我有许多 Tektronix 和 HP scopes 留在一个地方，你把你正在做的东西带给他们(有时称为“船锚”)。不久前，我的一个老式泰克望远镜有自己的专用手推车，所以我可以把它推到需要的地方。

如今，示波器相对便宜，这取决于你对性能的想法。它们也非常便携，这很好。事实上，这表明我已经被宠坏了，我的主要工作台——Rigol ds 1104 z——重 7 磅，但我仍然在寻找更小的快速工作。

这就是我如何拥有两个我想说的廉价望远镜的。他们在某些方面相似，但在其他方面不同。两者都不会取代真正的台式瞄准镜，但是如果你想要便携的东西，或者你的预算有限，它们可能值得一看。

## 廉价的望远镜

在我深入任何细节之前，你可能想一想你愿意为一个瞄准镜花多少钱——尤其是如果这将是你唯一的一个瞄准镜。如果你只是想省钱，我的意见是，你最好买一个更便宜，更老的板凳范围。Owon、Rigol 和其他公司的 300 美元范围内的非常好的瞄准镜的出现意味着旧的瞄准镜只能卖这么多。诚然，如果你真的需要一个 5 GHz 带宽的示波器，你仍然需要花很多钱，但对我们大多数人来说，一个 50 或 100 MHz 的示波器和几个通道就足够了。例如，在易贝上快速搜索，在第一个结果页面上就出现了两个不错的泰克示波器和一个售价 100 美元的安捷伦。如果你货比三家，你可能会买到更便宜的东西。

基于快速 ARM 或其他处理器的廉价示波器层出不穷。这些都很简洁，但现实是许多都有低带宽前端或遭受其他问题。一些 15 美元或 20 美元的套件在这个价格上是合理的，但一旦你达到 100 美元左右，我认为如果你正在寻找你的第一个范围，你应该有更好的。同样的道理也适用于[“声卡”示波器](http://hackaday.com/2014/05/27/an-audio-based-usb-oscilloscope-and-signal-generator-for-20/)(主要是一个输入网络，将信号输入到你电脑的声卡)。对于 DIY 项目很好，但可能不是你想要的唯一范围。

我现在想看的两个望远镜是 Owon Wave Rambler 和 AllSun(或者有时是 ESun) EM125。Owon 是一个带有 USB 电缆的小型手持探头，可以将数据发送回 PC 应用程序。EM125 是一款示波器——它有一个小显示屏，也可以作为电压表或欧姆表使用。它不连接到 PC。这两种仪器的价格都在 100 美元左右，而且很容易买到。

## EM125

[![em125a](img/336d2806d4af94bdc7ff273c7b500139.png)](https://hackaday.com/wp-content/uploads/2016/01/em125a.png)EM125 大约是一个中型数字电压表的大小，但大多数电压表都是纵向放置的，em 125 是横向放置的。事实上，它看起来有点像廉价的山寨 Playstation 手持视频游戏。

我喜欢 EM125 的一点是它有一个可持续很长时间的 USB 充电电池。我有一个旧的 Velleman 手持镜，使用镍镉电池或普通电池，当你想使用它时，你必须做的第一件事就是充电或更换电池。

EM125 的单色屏幕不会给 iPhone 带来任何竞争，但它很耐用。菜单系统并不完全直观，但它工作得足够好。仪器的示波器部分具有报告的 25 MHz 带宽，并且有示波器探头的正确连接。仪表部分使用标准屏蔽香蕉插头。这意味着你不能把一个探针挂在一个点上，然后从探针上读取所有的数据。

有一个漂亮的小支架，如果你想使用它，它可以将仪表保持在一个好的角度，还有一个开关可以打开耗尽电池的 LCD 背光。我不喜欢使用示波器的自动功能，但在这个小仪器上，按住按钮让它为给定的波形找到合适的设置是很方便的。

不过，你可以手动设置一切。您可以在上升沿或下降沿触发，并设置水平和垂直刻度。你也可以设置一种自动触发模式和触发等级。仪表显示信号的频率和电压(您可以选择 RMS、平均值或峰峰值读数)。还有一个显示电池电量的显示器和一个选择交流或 DC 耦合的开关。有一个 USB 端口，但据我所知，那只是为了给电池充电。不幸的是，没有探头补偿信号或其他测试输出。

## 欧文·漫步者

[![owon1](img/deff797038dabbc5094bb69448cea880.png)](https://hackaday.com/wp-content/uploads/2016/01/owon1.png) 漫步者在成本或性能上与 EM125 没有太大区别。它还声称有 25 兆赫的带宽。它是 USB 供电的，所以电池不是问题。然而，除了作为设备一部分的示波器探头之外，它几乎没有什么功能(你不能使用自己的探头)。有一个选择 1X 或 10X 的开关和一个多功能轨迹球，这让我想起了黑莓珍珠。

您必须使用 Windows 软件才能看到任何结果。我在 Linux 下运行软件时运气不佳，尽管我没有使用 VirtualBox。OWON RDS scopes 有一些非常基本的开源软件，但我无法让它与这个特殊的设备一起工作。

从好的一面来看，你最近可以买到一些非常便宜的 Windows 平板电脑(远低于 50 美元)，scope 确实可以用。不过，在平板电脑上，软件界面有点笨拙，所以我最终主要使用 Windows 笔记本电脑。但如果你需要一个便携式解决方案，平板电脑和漫步者可能是一个答案，该软件比 EM125 更强大。像 EM125 一样，没有可用的校准或探头补偿信号。

## 它们是如何工作的？

主观上，这两种设备感觉和使用普通示波器不一样。EM125 很方便，有一个真正的示波器探头，但相对较差的屏幕质量意味着你无法真正看到你可能想要的细节。另一方面，漫步者给了你很多细节，但是握着粗探头和使用轨迹球需要一些时间来适应。它还绝对需要连接 PC 或平板电脑。

如果您想了解这些设备的更多信息，请观看下面的视频。下一次，我将用一些简单的波形来测试这两种示波器，并以一种不太主观的方式来看看它们的表现。

老实说，如果它很好地支持 Linux，我可能会更多地使用漫步者。它在功能上更像一个普通的示波器，如果你能习惯它的感觉，并且不介意拖着一台电脑到处跑的话。另一方面，EM125 在我的 go 包中赢得了一席之地。除了基本的电表，你可以随身携带这个，得到一个电表和一个示波器(虽然电表不会测量电流)。也许范围不是很大，但总比没有范围好。

请记住，以同样的价格，你可以得到一个传统的二手示波器，它可能有多个频道和一系列你真正喜欢和使用的其他功能。当然，它可能比你的整个电脑还重，但它会更有用。但是，如果您需要可移植性，这两种方法都是不错的第二种方法。

 [https://www.youtube.com/embed/YpFgJtL1Q4o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YpFgJtL1Q4o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/KlQXnffzEB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KlQXnffzEB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

