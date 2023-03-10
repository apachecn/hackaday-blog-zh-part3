# 复习:TS100 烙铁

> 原文：<https://hackaday.com/2017/07/24/review-ts100-soldering-iron/>

温控烙铁可以便宜、轻便、质量好。当你选择一个熨斗时，选择其中的两个属性，因为你永远不会同时拥有这三个属性。你可能会认为这句格言代表了一条铁一般的规则，没有哪种铁能够将这三者结合起来，制造出一款不会倾家荡产的轻量级高性能工具！直到最近，你可能还有点道理，但也许现在有一个竞争者可以实现这一不可能的壮举。

迷你电烙铁 TS100 是一种相对便宜的中国温控烙铁，已经悄悄地进入了市场，一些在线评论员声称它与昂贵得多的专业级烙铁不相上下。我们以不到 50 英镑(约 60 美元)的价格订购了一台 TS100，然后等着它的到来，这样我们就可以看看到底发生了什么。

[![Constituent parts of a TS100 iron.](img/c9224c087129dc36387cd2876d22ba58.png)](https://hackaday.com/wp-content/uploads/2017/06/ts100-parts.jpg)

Constituent parts of a TS100 iron.

## 货物

这些铁被包装在一个智能纸板容器中，通过国际航空邮件很好地完成了保护它的任务。泡沫塑料里放着铁把手、一个单独的组合元件和钻头，还有一个信封，里面有一份简短的说明书和一个卡式密封袋，袋里有一把内六角扳手和一个备用螺钉来固定钻头。没有电源，你自己提供 12 到 24 伏的 DC 来供电。

手柄是一根塑料棒，包含大约 100 毫米(4 英寸)长的温度控制电子设备，周长类似于一只粗钢笔。在其后部是一个用于 DC 电源的桶形插座，旁边是一个用于固件和配置的微型 USB 插座，在其顶部是一个小型有机发光二极管显示器和几个按钮，在其前面是一个用于元件单元的插座。同时，元件单元约为 105 毫米(3.15 英寸)长，露出钻头末端的长度约为 70 毫米(2.75 英寸)。

[![The assembled TS100 iron](img/a78422f262a147c17a1a7cdb9f1d0ca5.png)](https://hackaday.com/wp-content/uploads/2017/06/ts100-iron.jpg)

The assembled TS100 iron

组装熨斗很简单，将元件插入插座，拧紧一个内六角螺钉就可以了。整个组装单元重 30 克，或一盎司多一点，几乎在它的中心有一个平衡点。

我们没有为 TS100 订购电源，但如果你手头没有合适的功率等级和极性，你无疑可以购买一个。我们使用了 19.5 V 的上网本电源，这远远超过了说明书中声称的 19 V 时 40 W 的功率。24 V 时最大功率为 65 W，12 V 时最小功率为 17 W。

在手中，铁是轻的，容易在手指上。就其本身而言，它在重量和手感上类似于握着一支自来水笔，很容易看出与 Weller 等更昂贵的熨斗相比的原因。然而，熨斗本身并不是故事的全部，因为你对电源的选择，尤其是它的引线，会对它在实践中的感觉产生巨大的影响。Weller 将安装一个特别灵活的硅胶导线，可能是为了在更高的温度下工作而设计的，相比之下，廉价电源上的导线可能更坚硬，更便宜。我们的上网本电源有一个直角插头，虽然它不是一个很好的柔性硅胶电缆，但一旦确保它不在热端的范围内，它就不会成为一个重要的负担。

[![The TS100 ready to use](img/5b18d09b0beeef628b7074c5c7e9893d.png)](https://hackaday.com/wp-content/uploads/2017/06/ts100-in-holder.jpg)

The TS100 ready to use

加热时，TS100 可能没有一些熨斗快，但它也不懒散。它的说明书上说，在 19 伏电压下，15 秒到 300 摄氏度，我们的熨斗当然没有让人失望。设置温度是一个简单的例子，使用按钮上下移动有机发光二极管显示器上的温度，一旦它保持在一个特定的温度，它将设置存储在其非易失性存储器中。

## 测试中

为了测试 iron，我们组装了一个小型无线电套件，这是一种表面贴装设计，旨在用于首次表面贴装焊接器，因此使用相当大量的 1206 元件和 SOICs，而不是 sop 或更小的集成电路。我们发现熨斗非常容易使用，但有一个警告:股票位是一个铅笔尖，类型“B2”是好的较大的表面贴装器件，但在我们看来可能有点笨拙的任何小于 0805。幸运的是，还有各种形状和大小的烙铁，包括表面安装专家可能想看的更细的烙铁。

TS100 的一个特点是其固件可以通过 USB 轻松升级，为此，很容易[下载最新版本](http://www.minidso.com/forum.php?mod=viewthread&tid=892&extra=page%3D1)并安装它。只需按住 live USB 插件上的一个按钮即可进入固件升级模式，当它在插入它的计算机上显示为驱动器时，将固件文件复制到该驱动器，它就会自我升级。

不幸的是，在我们的情况下，固件升级的诅咒袭击了我们，在下载和解包文件后，我们无法让我们的铁接受它。我们可以确定这个过程在 Ubuntu、Windows 和 MacOS 电脑上失败了，所以也许今天不是我们的幸运日。幸运的是，TS100 不是那种容易被失败的固件升级摧毁的设备，所以我们只是看到了一个错误文件，而不是一个死铁。烙铁本质上是一种硬件设备，而不是软件设备，所提供的固件版本适合焊接，所以这就是我们正在审查的内容。

这里值得指出的是，TS100 固件是开源的，代码和原理图可以从上面的链接中获得。我们说*被宣传为*开源，因为虽然代码是官方免费提供的，但它似乎没有附带任何形式的开源许可。这可能比许多读者更关心*软件自由纯粹主义者，但仍然值得一提。*

![The TS100 config file](img/7ff0a4ffcc2e082cf25adf47f380480c.png)

The TS100 config file

我们被告知，最新版本的固件通过设备本身的菜单系统提供对熨斗参数而不是温度的调整，但在我们的型号上，当你将熨斗的 USB 端口插入计算机而不按住按钮进入固件升级模式时，旧固件需要编辑出现在驱动器中的文本文件。在该文件中，您可以找到不同温度和时间的设置，并根据您的喜好进行调整。

## 底线

在拥有 TS100 几周后，我们的结论是什么？它是一个好的熨斗吗？它能让那些昂贵的熨斗物有所值吗？我们会建议你考虑一个吗？

回答这些问题时，将烙铁市场作为一个整体来考虑是很重要的。如果你花四位数的钱买一个焊台，你会发现你的烙铁比 TS100 更轻，它的射程更短，预热时间更快，软件控制更好，可用位数更多，事实上它在各方面都优于 TS100。十年来，你每天都要辛苦地使用那个焊台，它仍然会交付货物。

然而，如果你花三位数的低价从一个高质量的制造商那里买一个焊台，你会得到更接近的东西。它可能会有类似的选择位和一个很好的额外灵活的硅胶电缆，它可能会持续更长时间，但在焊接方面，这将是一个惊人的相似的体验。即使不得不在电源上多花几美元，这个范围内一个像样的焊接站的价格仍然是 TS100 的两倍多。

在与 TS100 相同或更低的价格范围内，焊接站的质量可能会开始下降，来自没有替换位支持的匿名制造商，并且不会有这么好的用户体验。也许价格相似的一体化熨斗，如[我们今年早些时候评估的 Antex TCS 50](http://hackaday.com/2017/03/02/review-antex-tcs-50w-digital-temperature-controlled-soldering-iron/)是更好的比较，此时我们开始看到 TS100 如何重新定义这一领域。Antex 是日常焊接的好熨斗，它与 TS100 重量相同，延伸范围也相同。它由电源供电，配有一根非常灵活的硅胶电缆，但当你并排比较熨斗时，很明显 Antex 被落下了。相比之下，它的手柄很大，温度控制仅限于非常基本的上/下设置，没有可配置性。

因此，如果你是一个高端专业用户，每天都在寻找一个熨斗来工作，TS100 可能不是取代你的顶级型号的选择。但是，如果你是一个经常焊接或严重的电子爱好者谁正在寻找最好的爆炸降压，你绝对应该考虑一个作为低端焊接站的替代品。如果你在温控铁食物链的底端购买，那么你真的应该认真看看 TS100。回到我们在这篇评论开始时的观点，它便宜、轻便，当然足够好。

与此同时，如果你制造烙铁，这可能会让你担心。我们期待看到与之竞争的车型能提供什么。

迷你 TS100 烙铁，以及相关的钻头和电源，可以在网上从所有中国电子产品的常见供应商那里找到。