# 让您的 PCB 从优秀走向卓越:墨粉转移

> 原文：<https://hackaday.com/2016/09/12/take-your-pcbs-from-good-to-great-toner-transfer/>

[![dscf8697](img/732966b350e1eda37aa7eaf745a25507.png)](https://hackaday.com/wp-content/uploads/2016/09/dscf8697.jpg)

One-offs that I never would have gotten professionally made, but that were infinitely handy during development

我们很多人在家制作电路板。我发现，在完成项目的过程中，即使完成的版本将被发送到 PCB 工厂，在我的技巧包中包含中间步骤也是一项有用的技能。例如，当我需要一个可以与其他开发工具相结合的分线板时，没有什么比能够快速制作一些插件更好的了。快速地做这件事，继续项目的其余部分，而不是下订单和等待交货，有助于我保持流畅。

到目前为止，调色剂转移是在家制作电路板最快的方法——只需在激光打印机上打印出电路，在铜上熨烫，然后蚀刻。当它工作的时候，它是令人敬畏的。当它不一致时，找出无数因素中的哪一个是不一致的，可能是一件非常棘手的事情。

很长一段时间以来，我一直在使用一种非常可靠且可重复的方法。最近，我对系统的性能做了一些调整，我想我应该分享一下我所得到的。目前，我能够非常可靠地生产 6 密耳(0.15 毫米)走线和 8 密耳(0.20 毫米)间距的电路板。在后期制作中稍加小心，4 密耳/ 6 密耳是完全可能的。

这足以满足我的大部分原型制作需求，涵盖 0.65 mm 引脚间距的 TSSOP 器件，并允许我通过 0805 表贴电阻或电容馈入两条走线。这和最便宜的专业制造公司不相上下，但是我可以在大约十五分钟内转动一块板。在我看来，比点菜和等待强多了。当我需要像[丝印](http://hackaday.com/2014/01/27/toner-transfer-pcbs-double-sided-with-color-silkscreen/)和[通孔电镀](http://hackaday.com/2015/02/25/diy-through-hole-plating-like-a-boss/)这样的奢侈品时，会有变通办法，但大多数情况下，我会在最终版本制作出来之前节省这些。

[![dscf8696](img/ae63175d9a8678d1c8f29d1c9db6e4a1.png)](https://hackaday.com/wp-content/uploads/2016/09/dscf8696.jpg)

Scientific Apparatus: an updended clothes iron, a rolling pin, and a decent IR thermometer.

秘密？科学！或者至少采用大量的变量和秘密技术，将它们简化为一次改变一个变量的实验，然后沿着那个维度进行优化。有一系列令人眼花缭乱的技术，其中很多只有在你有正确的墨粉品牌、正确的纸张或正确的熨烫方法时才有效。简而言之，它们是不可复制的。当你的设置和别人的不完全匹配时，所有的赌注都取消了。在这里，我将展示一种可重现的方法，并向您展示如何校准它。

## 无关紧要的事情

许多互联网上的墨粉转移指南关注的都是无关紧要的细节，比如用于转移介质的纸张类型，或者熨烫前清洁铜片的方法。这并不是说你不需要先清洗铜器——你绝对需要——而是说你怎么做并不重要。我用过细沙砂纸，绿锅刷，最近我用一些在五金店买的海绵在铜焊前打磨管道接头。我接着用丙酮擦拭。关键是你要去除表面的氧化和油脂。我不在乎怎么做。

[![](img/103984e65d562817b0a507668a494b80.png)](https://hackaday.com/dscf8707/)

Scrubbie, acetone, and oxidized copper

[![](img/7feedebf6a63bf8b9ae84acf9b23a596.png)](https://hackaday.com/dscf8681/)

Tape magazine to regular paper and print

[![](img/88835176d1f4adfe5ee5cbd57cbe0a71.png)](https://hackaday.com/dscf8739/)

Wet paper virtually dissolves in water

同样，转印纸的选择也是相当开放的。我在光滑的杂志页面(《经济学人》是我目前最喜欢的)和有剥离标签的塑料涂层衬纸之间选择。这两个表面的工作方式完全不同；贴纸背纸直接剥离，而杂志纸用拇指摩擦时会在冷水中溶解。外面有更好的东西。转印纸的要点是它有光泽，所以它不会使图像变形，并且容易释放，使墨粉留在铜上。剩下的就是方便了。

[![dscf8748](img/925a08fec47ca9e27d78e1bbe5b3d148.png)](https://hackaday.com/wp-content/uploads/2016/09/dscf8748.jpg) 最后，蚀刻剂的选择并不重要。我使用[氧更新氯化铜酸](http://www.instructables.com/id/Stop-using-Ferric-Chloride-etchant!--A-better-etc/)，因为它基本上是无限回收，我讨厌处理有毒化学品的麻烦。人们使用氯化铁或过硫酸铵。其他人用醋和盐，或者龙的唾液和会计师的眼泪。有些人在罐中搅拌液体，有些人用喷雾器，还有一些人用海绵擦。什么都行。

当然，这些东西对于制造一个好的墨粉转移印刷电路板都是绝对重要的，但是没有一个是唯一不可替代的。

## 物理学

另一方面，有三个基本因素影响墨粉对铜的粘附力，这归结于物理因素:时间、温度和压力。将这三个减少到一个是迈向可靠性和可重复性的一大步，这是我们的第一步。

### 首先确定压力和时间

就压力而言，越多越好。事实上，有些激光复印机根本不需要加热辊就能工作。他们用力挤压塑料碳粉颗粒，使其在室温或室温左右粘附在纸上。我们不能施加那么大的压力，但是我们会把压力变量固定在“尽可能多”。

[![dscf8715](img/9b78f25d2a757373665e4c8db2fb4a28.png)](https://hackaday.com/wp-content/uploads/2016/09/dscf8715.jpg)

You can almost hear me grunting…

我把 PCB 放在我的倒铁上，用我全部的重量压在擀面杖上。由此产生的压力相当大，因为擀面杖与板子的接触面积很小，而且相当稳定，因为我只重这么多。

我从[这个方法](http://www.pcbfx.com/main_site/pages/tech_support/tips_n_tricks/rolling_pin.html)中获得了灵感，这个方法本质上颠倒了做同样的事情。我的经验是，使用这种程序，电路板永远不会均匀地滚过销钉，但我可以理解，如果你不想在你的房子里暴露我设置的电恐怖。任何坚固的热表面都可以工作，并且改进的设置将具有更好的温度控制。如果你有一个[改进的层压机，可以产生足够的压力](http://hackaday.com/2016/02/29/pcb-laminator-is-its-own-project/)，那可能会更好。我有一个废铁。

与压力越大越好不同，停留时间越长的效果下降得越快。在激光打印机中，每分钟的页数是一个关键的卖点，他们试图将停留时间降到最低。如果你在板上滚得太快，附着力会不均匀，所以解决办法就是慢慢滚，来回滚。你可以把时间从等式中去掉，只要滚动得很慢，滚动速度的任何降低都不会实质性地改变什么。一两分钟就够了。

当然，所有这些都是相对的。你用的墨粉和我不一样，体重和我不一样，甚至和我对“慢”的想法也不一样。但是，只要你保持自己的实践一致，这些变量不会对结果产生很大影响，我们可以自由处理会产生影响的变量:温度是秘方。科学来了！

### 温度:塑性，但不熔化

当碳粉被加热时，它会经历几个不同的阶段。起初它是一种硬塑料，然后当它通过[玻璃化转变](https://en.wikipedia.org/wiki/Glass_transition)时变得粘稠并略有延展性，然后随着温度进一步升高，它融化并变成液体。

我不知道网上关于你应该把你的熨斗调到“尽可能热”的谣言是怎么来的。但我知道这样做的结果是什么——油污转移对施加的压力极其敏感。这和我们在这里寻找的正好相反。相反，我们的目标是保持碳粉处于玻璃化转变状态，温度尽可能低，以便在我们大致恒定的最大压力下与铜融合。

校准程序的第一步是在升高的温度下进行一系列的转移。你的体温不会和我的一样，但这没关系，因为你不用我的碳粉，也不会在我家制造多氯联苯。诀窍是始终如一。

 [![Lower temp on top, higher on bottom](img/ac7815cb9dc75e0e2f85d825049374b5.png "dscf8718")](https://hackaday.com/dscf8718/) Lower temp on top, higher on bottom [![98 degrees](img/352fe7ea033ee96a1b03823bb7bf6038.png "dscf8727")](https://hackaday.com/dscf8727/) 98 degrees [![125 degrees](img/e2088ee58a3b43584d025b686564ce43.png "dscf8728")](https://hackaday.com/dscf8728/) 125 degrees [![142 degrees](img/5fe5e72d908acab9bd1758c7297e60a1.png "dscf8729")](https://hackaday.com/dscf8729/) 142 degrees [![166 degrees](img/288706dd749618893ce9ccf2ff410372.png "dscf8731")](https://hackaday.com/dscf8731/) 166 degrees

这里的四个例子是在 98℃、125℃、142℃和 166℃下转移的。第一个例子显然粘合得不好，事实上，除了 16 密耳走线之外，其他走线在蚀刻后都不连续。尽管在地面浇注上使用了 20 密耳的间隙，但最高温度的电路板仍然到处短路。令人惊讶的是，TSSOP 尺寸基本正常，即使 6 密耳间距的两条走线短路。

从转移单上看，极端温度的问题也很明显。在低温板的情况下，有许多墨粉留在纸上。它只是没有很好地粘在铜上。撕下高温纸时，它裂开了，可能是因为它的塑料层融化在碳粉中。

两个中间的板子看起来很不错，但是外表可能会有欺骗性，所以可能值得蚀刻它们。实际上，125°C 电路板存在一个小缺陷——6 mil 走线样品仅在底部与焊盘连接处断裂。在 142°C 电路板上，穿过 0805 器件的两条闭合走线短路，尽管所有其它走线都是连续的。介于这两者之间的温度可能是最佳温度。

我在 132°C 的温度下重新测试了这个测试板，并打印在杂志纸上，结果非常完美。除了剪下杂志纸并将其粘贴到一张普通纸上以使其能够正确通过打印机之外，杂志纸可能是理想的基底。当它溶解在水中时，碳粉上的压力很小，在这里或那里拉起斑点的风险也很低。

并非巧合的是，自从我上次在购买了当前的激光打印机后进行校准以来，我一直使用 130°C 左右的温度。获得一个具有设定温度的一致程序是成功的一半以上。

## 打印机及其软件

在这一点上，随着墨粉转移过程本身的引入，限制打印可靠性和分辨率的因素将是打印机本身和驱动它的软件。我发现不同的打印机驱动程序(PCL 和 Postscript)之间，以及用于保存作品的不同文件格式和读取它们的程序之间有着惊人的巨大差异。

[![](img/21f09990db9c1d00937acf49337e0240.png)](https://hackaday.com/2016/09/12/take-your-pcbs-from-good-to-great-toner-transfer/dscf8783/)

Postscript file, postscript driver

[![](img/fb8938cca71f599e959fea09f5849f34.png)](https://hackaday.com/2016/09/12/take-your-pcbs-from-good-to-great-toner-transfer/dscf8792-2/)

Jaggies transferred beautifully! Garbage in, garbage out.

特别是，我的系统上的两个驱动程序似乎都将 KiCad 的 Postscript 和 PDF 输出解释为彩色文件，并对结果应用抖动。使用 Postscript 驱动程序，这会导致锯齿边缘，这种效果[其他人在](http://hackaday.com/2014/01/05/testing-the-limits-of-home-pcb-etching/)之前就已经注意到了。随着传输顺利进行，这些锯齿最终出现在 PCB 的铜中。

[![](img/d2e241021bf8bf06e97667a616d37e2c.png)](https://hackaday.com/dscf8776/)

PCL driver does strange dithering

[![](img/694a93d28c4c3d20f6895423b8371c4a.png)](https://hackaday.com/2016/09/12/take-your-pcbs-from-good-to-great-toner-transfer/dscf8780/)

Dithering results in weedy, thin lines

对于我一直使用的 PCL 驱动程序，它似乎应用了一种分辨率更高的抖动算法，结果是线条看起来更细，以至于出现了不连续。原来，我在打印细线时遇到的问题是由驱动程序引起的。

[![SVG file, postscript driver](img/1da79d65882f0a6457ca67597c01693f.png)](https://hackaday.com/wp-content/uploads/2016/09/dscf8786.jpg)

SVG file, postscript driver

最后，当我将文件保存为 SVG 图形并在 Inkscape 中打印出来时，所有的颜色抖动伪像都消失了，但结果是漂亮平滑的深色痕迹，一旦传输就有点太粗了。也许有了这些改进的痕迹，我可以把温度降低一点？粘纸上的转印也有一些灰尘，而杂志纸不会出现这种情况，所以也许纸张类型确实有点关系。

重要的是要注意，在你控制住温度和压力的主要变量之前，你无法真正诊断出像这样的细节。但是一旦你这样做了，并且链的软件阶段出现的最小的故障是可见的和可重复的，你就有了一个新的限制因素，是时候调整软件了。

不幸的是，每个人都有不同的软件和打印机设置，并不是所有适合我的调整都适合你。现在，你只能靠自己了。只要知道打印机的分辨率、打印机配置选项，甚至驱动程序和文件类型都很重要。这需要做很多实验，所以一次只考虑一个变量。

## 冲洗、重复、提炼

所以一切都相互影响:温度、压力、纸张类型，甚至文件格式和打印机驱动程序。我今天放弃了实验，因为我对可靠的 6/8 迹线感到满意，当我需要为某个项目进一步推动它时，我可能会从进一步降低温度开始，看看这是否能解决加粗的线条。如果我真的需要 6 密耳的间隙，我会在蚀刻前仔细检查这些位置并用手术刀清理，或者用 4 密耳的走线宽度进行实验。毕竟，使用 SVG 输出和 Inkscape 进行打印，我在 6 mil 处没有一个不连续的痕迹。

然而，有一点我绝对不会改变，那就是基本技术。大约十年前，我第一次开始通过滚筒施加恒定的最大压力并调整温度，从那以后，这一直是一种非常可靠的制造 PCB 的方法。最近对最大分辨率的追求是一种有趣的转移，我很高兴知道我可以在需要时做一些小功能，也很难过进一步改进的道路似乎要通过调整软件和驱动程序，因为有太多的选择了。

在某些时候，让专业人士为你工作会变得更加容易。但对我来说，墨粉转移几乎适用于原型制作的所有初始阶段，而且周转时间绝对无法超越。