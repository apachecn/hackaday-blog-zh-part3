# 最简单的镶板方式

> 原文：<https://hackaday.com/2017/06/21/panelizing-boards-the-easy-way/>

由于某些在未来某个时候才会公开的原因，我最近需要对一些 PCB 进行面板化。面板化是一种艺术，它将你已有的 PCB 设计，无论是 KiCad 板文件、Eagle 板文件，还是 Gerbers 板文件，转化成一个 PCB 集合，然后送到工厂。

[![](img/66011c31eaa26175eae598188440fd6b.png)](https://hackaday.com/wp-content/uploads/2017/05/panelracing.jpg)

Now *this* is panel racing

如果你仍然想知道这意味着什么，看看你从 OSH Park 得到的最后一块电路板， [Seeed](https://www.seeedstudio.com/fusion_pcb.html) ，Itead，或者肮脏的 PCB。在你的冲浪板周围，你会发现一些粗糙的地方。这些是“鼠标咬痕”和标签，在这里，电路板被串在一起，形成一个巨大的矩形面板，发送给制造商。[你可以看看这篇来自奥什公园的【莱恩】的精彩采访](http://theamphour.com/the-amp-hour-149-purple-pcb-philosophy/)，了解一下这是如何运作的，但基本流程是拿一堆 Gerbers，添加标签和鼠标咬痕，解决背包问题，然后把完成的面板送到板房。

嵌板是我们大多数人不会经常做的事情。真的，当你在制造东西的时候，你只需要一块木板。对于小规模生产和原型，裸板就足够了。仅仅是因为嵌板远没有在 OSH Park 或 Seeed 扔一些 Gerbers 那么普遍，就没有多少(好的)教程，甚至更少(好的)工具来这样做。这就是如何使用开源工具快速轻松地对电路板进行面板化。

#### 我想要的

[![](img/faa95b97cd034567786de9ca8549cb59.png)](https://hackaday.com/wp-content/uploads/2017/06/defbadge_bright.png)

The DEF CON 24 badge, in a panel

面板化电路板，或者将电路板的多个副本放在一个 Gerber 文件中，并不是什么新鲜事。我们已经在 Eagle 中用 ULP 脚本实现了这一点，也在 KiCad】中用 Python 实现了这一点。【达夫·琼斯】给[做了一个 Altium](https://www.youtube.com/watch?v=VXE_dh38HjU) 的面板化教程。所有这些都有其缺点。通常的工具和教程不包括在一个面板上放置多个电路板设计。大多数嵌板方法只适用于矩形板。Altium 可以做任何事情，但是 Altium 很贵。

我需要的是一种方法，将不止一块形状怪异的板放在一个矩形面板上。需要这样的例子吗？看看右边的 DEF CON 24 徽章。这是一个形状怪异的板，设计成适合自动化装配的矩形面板。代替 v 形槽，板子只是从面板上磨出来，用老鼠咬的地方，或者玻璃纤维的小标签和小孔固定住。这种技术的巧妙实现还允许面板上有焊盘和走线，用于对每块电路板进行编程。

在 Eagle 和 KiCad 这两种最流行的低规模 PCB 设计和制造工具中，您能做到这一点吗？是的，但是很难。Altium 将很容易做到这一点，但对于那些正在制造数万块电路板的人来说，这确实是一个工具。到目前为止，我只发现了一个工具，它可以让你把多个 Gerber 文件放到一块板上，然后合并它们。

### 格柏镶板仪

我发现的最好的工具是[【斯蒂安·库伊佩斯】](http://blog.thisisnotrocketscience.nl/projects/pcb-panelizer/)。他的 PCB Panelizer ( [在 GitHub](https://github.com/ThisIsNotRocketScience/GerberTools) 上有售)是我发现的最好的东西，可以把你已经设计好的 Gerbers 变成一个容易制造的面板。在找到这个神奇的工具之前，我花了大约一天时间试图找出如何对 Gerbers 进行小组讨论。找到这个工具后，我能够在大约二十分钟内创建我需要的面板。Gerber Panelizer 是一个非常棒的工具，我将在这篇文章的剩余部分详细介绍这种简单易行的制作 PCB 面板的方法。

### 使用 Gerber Panelizer

使用 Gerber Panelizer 再简单不过了。你所要做的就是设置面板的大小，放下。将 gerber 文件压缩到面板上，添加一些分页符，然后导出合并的 gerber 文件。在你的电脑做了一点思考后，你得到了一块板，准备送往工厂。

[![](img/26ada7ab2652d042e99bfb37778e736c.png)](https://hackaday.com/wp-content/uploads/2017/05/app1.png)

Step 1: Open Gerber Panelizer

[![](img/f7dee2e1d97755f7204ae3739939145e.png)](https://hackaday.com/wp-content/uploads/2017/05/app2.png)

Step 2: Define your panel size

[![](img/43402eab20ec45ba7300f9b99f0cdb4d.png)](https://hackaday.com/wp-content/uploads/2017/05/app3.png)

This is the Panel Properties window. Use this to define the board size, fill empty space, set the offset, etc

[![](img/f2b02d34b4b334cf8885568e8fb6b92a.png)](https://hackaday.com/wp-content/uploads/2017/05/app4.png)

Step 3: Drop Gerbers onto the window

[![](img/0eef43d53a21105e91cac6da56b4172a.png)](https://hackaday.com/wp-content/uploads/2017/05/app5.png)

Step 4: Place Breaktabs

[![](img/df3ebd80e7eba74bb2a78ea699020e33.png)](https://hackaday.com/wp-content/uploads/2017/05/mandalapanel.png)

Step 5: Enjoy a panelized board

当然，Gerber Panelizer 并不局限于方形或矩形电路板。任何形状都可以，面板属性窗口中的'*填充空白区域'*,使得创建形状怪异的 PCB 面板变得容易。

我迅速制作了一个 GitHub Unicorn 的艺术版(五分钟鹰)，并窃取了 T2 Freeduino 的源代码。这是 Gerber Panelizer 所能做的最好的例子。有了这个工具，你可以嵌板形状奇怪的板，并把一个以上的设计放在一个面板上。

[![](img/b189222e021e388cfe344ba5d82ed8d8.png)](https://hackaday.com/wp-content/uploads/2017/05/horsepanel.png)

### Gerber Panelizer 注意事项

Gerber Panelizer 是一款非常棒的工具，可以让您快速轻松地将多个 Gerber 文件拼接到一块易于制造的电路板上。不幸的是，DIY PCB 人群和开放硬件爱好者一般都是小气鬼。传统观点认为，唯一值得拥有的工具是那些像啤酒一样免费的工具，这一论点通常明显伪装成“像演讲一样免费”。这意味着该软件是在没有支持的情况下提供的，并且通常具有不完整的功能。

Gerber Panelizer 并不是没有重大问题，尽管有些指责可以指向 KiCad。KiCad 理念区分了铣削层、镀层和电路板的最终切口。在 KiCad 中，这意味着。GKO 和。GML·葛伯档案。KiCad 以其无限的智慧，决定板的剪切层应该使用文件扩展名. GM1 作为输出 Gerber。[这引起了很多混乱](https://github.com/ThisIsNotRocketScience/GerberTools/issues/23)，但好消息是这个问题将很快得到解决。装有 Nvidia 驱动程序的 Windows 上的 OpenGL[是一堆垃圾](https://github.com/ThisIsNotRocketScience/GerberTools/issues/21)。这个问题可以通过使用我的笔记本电脑而不是我的桌面战斗站来解决。另外，当前版本(至少在撰写本文时)不支持在 Gerber 文件和“填充空白区域”之间添加分页符。这是[Arsenijs]在 Hackaday.io 上解决的一个 bug，我欠他的是他为我修复了那个 bug，但这里重要的是我为开源开发贡献了资金。

这是面板印刷电路板的完美解决方案吗？不。理想情况下，你会希望基准点沿着面板的边缘，这样抓放机就可以知道面板在空间的位置。您还需要在电路板侧面设置一些 M4 孔，这样拾放机就可以沿着生产线移动电路板。然而，这确实是面板化一堆板的最简单的方法。没有其他工具比得上 Gerber Panelizer 的易用性。

尽管有这些问题，Gerber Panelizer 是一款非常棒的软件，应该放在每个人的工具箱里。是的，有一些问题，但是看起来最关键的问题会在下一个版本中得到解决。

如果你想玩这些 Gerber 文件，你可以在 hackaday.io 上找到它们[。](https://hackaday.io/project/24935-flying-ostrich)