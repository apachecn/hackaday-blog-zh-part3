# PCB 布局的计算机视觉

> 原文：<https://hackaday.com/2018/06/12/computer-vision-for-pcb-layout/>

进行 PCB 布局布线的一个大问题是为要使用的元件找到合适的尺寸。大多数工具都有一些库，当然，有些比其他的好。您也可以经常使用一些通用的足迹。不过，这对于原理图布局来说并不方便，因为您必须记住哪个引脚在哪里。但是如果你找不到你要找的东西，SnapEDA 是许多不同布局工具可用的组件的有趣来源。然而真正吸引我们眼球的是他们的一项相对较新的服务，该服务使用[计算机视觉和 OCR 直接从数据表](https://www.snapeda.com/instabuild/)中生成原理图符号。你可以在下面的视频中看到它的工作原理。

该服务似乎与数据库已经知道的部分绑定在一起。并且具有已知的可用足迹。正如您在视频中看到的，它会挖掘数据手册，让您选择其中的引脚表。系统对数据表的这一部分进行 OCR，让您修改结果，并添加任何遗漏的内容。

不可否认，这很酷，尽管一旦惊叹的因素消失，您会意识到您仍然需要定位表和设置 pin 类型。他们的演示展示了如何添加接地垫等其他东西。对于像演示中这样的小零件。这并不比仅仅将数据输入表格简单多少。一个巨大的部分可能有更多的好处。

当然，一旦你有了一个符号，你就可以为很多流行的软件包包括 Eagle，KiCAD，OrCAD 等得到它。你可能会担心人们创造出不好的符号，但是他们已经想到了。当您创建这样的符号时，它只对您的帐户可见。所以如果你搞砸了什么，只会影响到你自己的项目。

这一点最吸引人的地方可能是——即使你没有建立自己的足迹——你如何为各种布局程序获得零件。当我们[查看布局工具](https://hackaday.com/2016/09/22/making-a-pcb-eagle-part-1/)时，你要做的第一件事就是[制作一个新的符号和足迹](https://hackaday.com/2016/11/17/creating-a-pcb-in-everything-kicad-part-1/)。

 [https://www.youtube.com/embed/j8t5lDNcJZg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j8t5lDNcJZg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

