# 检测有无头痛的水

> 原文：<https://hackaday.com/2016/12/15/detecting-water-with-and-without-headaches/>

在德克萨斯州，至少在休斯顿附近，我们没有地下室。然而，我们确实有膨胀。当没有人注意时，这两者都容易进水。我的一个朋友问我如何看待一个演示如何用几个分立元件制作水传感器的仪器。这个电路可能会工作——它依靠大多数水的导电性向双极晶体管的基极提供足够的电流来开启它。

人们很容易过度思考这样的事情，所以我告诉我的朋友，他应该选择一些更传统的东西。我不知道它的来历，但它比我还老。你可以用家里已经有的东西做一个完美的探水器。我的观点不是你应该(或不应该)建造一个自制的水传感器。我的观点是，你并不总是需要去高科技的解决方案。

另一方面，这是黑客日，所以我相信你想知道如何从普通的家庭用品中破解一个水传感器。图片可能会告诉你这个故事，但如果没有，请继续阅读。

## 你需要什么？

水传感器的核心是一个弹簧衣夹。你还需要两个扁平的金属片。我见过用硬币做的，但是你也可以用几个垫圈或者金属碎片。我甚至见过用铝箔做的，但不推荐。还有一个关键因素:一片阿司匹林。你也许可以用一些其他的东西，但是它必须足够坚硬以保持衣夹打开，而且在接触水的时候会溶解。

剩下的你可以想出来。你把电线连接到金属触点上，在触点中间夹上阿司匹林，用衣夹把它夹在一起。如果探测水不是你的事，你可能会喜欢[美国黑客]的视频(见下文)，它使用相同的想法来探测何时开门。

## 更简单的传感器

![Anti-static foam, wire, Plasti Dip for an analog pressure sensor](img/726195ec893a51d57bd916c30a4876c9.png)

Anti-static foam, wire, Plasti Dip for an analog pressure sensor

阿司匹林和衣夹只是制作简单传感器的一种方法。导电泡沫很好地充当了压力传感器(特别是如果你用一点塑料浸渍来密封它的话)。很多传感器使用另一个元件的特性(像这个[温度传感器](https://hackaday.com/2016/06/10/zero-parts-count-temperature-sensor/))。[的陪衬似乎也是常见的成分](https://hackaday.com/2015/11/30/conjuring-capacitive-touch-sensors-from-paper-and-aluminum-foil/)。

很多时候，一个用来创造某种东西的组件也能感觉到它，这听起来很奇怪。例如，[led 可以充当光传感器](http://www.instructables.com/id/Better-LED-as-light-sensor/)。一个扬声器可以作为[一个麦克风](http://www.zyra.org.uk/sp-mic.htm)(或者，你可以把磁铁扯出来，偷一个继电器线圈，让[成为一个磁性速度传感器](http://www.instructables.com/id/Magnetic-speed-sensor/))。

## 对…咆哮

如果你仔细想想，我的观点是我们经常在 Hackaday 帖子的评论中看到的。不，不是“那不是黑客”我想到的更多是最新的 Raspberry Pi 项目，它会在天黑时打开灯，这将引发许多关于如何使用 2N2222(或运算放大器，或 555，或任何您选择的武器)实现这一点的评论。

一般来说，我们不介意这样的项目。人们不需要一个打印“Hello World！”但这是熟悉编程语言的好方法。出于同样的原因，有时候用 Arduino、Raspberry Pi 或 FPGA 做一个简单的项目，更多的是为了熟悉开发环境以及如何应用该工具。

另一方面，你的 LED 闪光灯不需要 2 GHz 的 CPU 和 32 GB 的内存来运行 RTOS。我对这些传感器的看法是一样的:有时候你真的需要一个灵敏、精确的传感器。大多数时候你需要的要少得多。如果你不是去做一个教育项目，花点时间想想你是不是在用铲子往咖啡里放糖。

## 轮到你了:自制传感器

有很多方法可以制造简单的传感器。轮到你了。你最喜欢的 DIY 传感器是什么？请在评论中留言，让我们知道你从不可能的事情中破解出了什么传感器。

 [https://www.youtube.com/embed/aLQLhyaH_QU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aLQLhyaH_QU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

