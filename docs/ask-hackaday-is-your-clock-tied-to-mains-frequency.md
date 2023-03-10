# 问 Hackaday:你的时钟和电源频率有关系吗？

> 原文：<https://hackaday.com/2018/03/29/ask-hackaday-is-your-clock-tied-to-mains-frequency/>

三月早些时候，我们听说互联的欧洲大陆电网发生了一个奇怪的现象，导致今年到目前为止时钟慢了大约六分钟。这是由于电源频率略有下降。这种下降并没有使任何东西停止工作，但设计用于累积 50 赫兹电网频率的总过零事件的时钟在该频率下(比如说 49.985 赫兹)无法保持准确的时间。

这个话题引发了一系列有趣的对话。有几种说法认为，现代闹钟和大多数连接到电源的设备不再从电源频率获得时钟计时。我已经研究过这一点，我将在下面深入探讨。但我们真正想知道的是:你的闹钟和其他设备是否与电网或其他东西保持同步？

## 闹钟芯片

[![](img/a36bed72d73665d864c35403fc59412b.png)](https://hackaday.com/wp-content/uploads/2018/03/magnovox-alarmclock-bottom-label-cropped.jpg) 我总是有兴趣了解很多我脑子里出错的东西。在这个特别的例子中，我在 Twitter 上放了一个我每天使用的大约 30 岁的闹钟的图片，作为电源频率时钟设备的例子(我家里至少有五个这样的设备之一)。有人回答说，这是一个石英钟，因为它是数字的，因此不会从电源获得时间。

我当然可能错了。我只是假设它与电源频率有关，但我说不出为什么我会这么想，除了听说大多数挂钟都是这样。在思考这个问题的时候，我想知道如果这个钟是和电源相连的，它怎么会有备用电池呢？这实际上是一个非常有趣的问题。事实证明，我对这个钟的工作原理没有错，但我现在才知道，因为我把它拆开来研究了。

时钟内部有两个不同的部分:时钟模块和收音机模块。我忽略了无线电，仔细查看时钟模块，寻找通常出现在“音叉”外形中的 32.768 kHz 时钟[晶体](https://hackaday.com/2017/01/17/understanding-the-quartz-crystal-resonator/)。我找不到。

[![](img/d8e3d37c72bb4af2fda91a009482b8cc.png)](https://hackaday.com/wp-content/uploads/2018/03/magnovox-alarmclock-overview.jpg)

接下来我看的是什么芯片在驱动计时板。它被标记为 LM8562，一个[快速数据表搜索](http://www.datasheetcatalog.com/datasheets_pdf/L/M/8/5/LM8562.shtml)结果是一个“宾果”！这部分被列为“数字闹钟”。通过更多的网络搜索，我认为这是大多数闹钟中的芯片。如果你通过按住一个按钮来设置时间和闹钟，并使用快速或慢速按钮来改变它，我敢打赌它是基于 LM8562。

[![](img/bd9623337a3ca1f14708fdfcbe5fa7fd.png)](https://hackaday.com/wp-content/uploads/2018/03/magnovox-alarmclock-timing-board.jpg)

Ew. 30 years of yuck.

该芯片驱动显示器，并具有我刚才提到的用户输入按钮。我正在寻找的关键功能如下所列:“12/24 小时模式，50/60 赫兹可选(前提是不可能选择 24 小时模式和 60 赫兹的组合)”。这款芯片确实与电源相连，数据手册中吹捧的下一个功能回答了我关于电池备份的问题:“片内 CR 振荡器，在断电时作为备用”。所以有一个内置的 RC 振荡器，在断电时用电池供电。我应该做一些测试，看看这有多准确。很有可能你的时间在 RC 时钟源上运行时会非常快，但只要它没有完全重置时钟，如果电源恢复，它仍然会在早上叫醒你。

 [![9V battery compartment](img/56c5860927e26b88e28b4fe8310ff593.png "magnovox-alarmclock-battery-backup")](https://hackaday.com/2018/03/29/ask-hackaday-is-your-clock-tied-to-mains-frequency/magnovox-alarmclock-battery-backup/) 9V battery compartment [![Radio board closeup for anyone interested](img/e0a6a31ff32cf995f5cd7106b2e6c26f.png "magnovox-alarmclock-radio-board")](https://hackaday.com/2018/03/29/ask-hackaday-is-your-clock-tied-to-mains-frequency/magnovox-alarmclock-radio-board/) Radio board closeup for anyone interested

## 没有接通电源的时钟

[![](img/18447255b9ce3d20c758815338e0fce0.png)](https://hackaday.com/wp-content/uploads/2018/03/microwave-clock.jpg)

The cheapest built-in microwave I could buy certainly doesn’t have special time keeping.

我现在根据经验来识别电源连接的时钟。如果它插在墙上不动，很可能是电网频率造成的。尤其是微波炉、录像机、传统烤箱和非互联网连接定时器等具有时钟功能的电器，如可编程恒温器和电灯开关。但是当然每条规则都有例外。如果时钟使用的是将交流电转换为 DC 的壁式电源，那么它就没有连接到电源，因为 DC 没有过零事件可以计数。有可能你有一个壁式电源转换器，但不太可能。

你还会注意到，我提到过时钟不会自动调整。有些时钟在通电时(通过插头或电池)会设置自己的时间和日期。在向埃利奥特·威廉姆斯推销这篇文章时，他提到每个模块相当于 1 个€，很可能为德国的大多数东西计时。这些通过收听来自无线电台的时间数据来工作。美国也有类似的标准，叫做 [WWVB](https://en.wikipedia.org/wiki/WWVB) 。我的主张是，如果一个时钟有这些模块之一，他们会设置自己，这是一个简单的方法来告诉设备没有使用电源频率。但这些设备可能仅限于稍微高端的产品:当没有它也能获得同样稳定的计时工作时，在竞争性消费品的成本上增加一欧元可能不值得。

最后，你可能有一个使用非常精确的时间标准的时钟。我最喜欢的例子是 DS3232(你可能知道它是 [Chronodot](https://hackaday.com/2009/10/27/parts-chronodot-rtc-module-ds3231/) )，这是一个内置在芯片中的温控振荡器(TCXO)。对于一个可以在硬币电池上运行多年的单芯片来说，这些东西具有难以置信的精度。但对于消费品来说，它们有点贵，所以我相信你很少看到使用它们的设备。我客厅里的[球形时钟](https://shop.evilmadscientist.com/productsmenu/156)就有一个——这是一个附加的，但正如我说过的，这是我最喜欢的时间芯片。

## 告诉我们你的钟表

所以我们问你:你身边的钟是怎么得到时间的？我们很想知道您的时钟是否使用 LM8562，是否来自更高级的信号源，如无线电信号，或者这里根本没有提到的东西。您的设备从哪里获得时间标准？