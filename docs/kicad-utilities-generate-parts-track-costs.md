# KiCad 实用程序生成零件；跟踪成本

> 原文：<https://hackaday.com/2015/12/05/kicad-utilities-generate-parts-track-costs/>

KiCad 越来越受欢迎，不仅有越来越多的人转向它并将其用于他们的项目，而且也有越来越多的人以库、脚本和实用程序的形式积极地为项目做出贡献，以改善工作流程。

### ipart

[Dave Vandenbout]又名[xesscorp]为 KiCad 编写了几个实用程序。当处理大型多引脚零件(如微控制器)时，使用传统的 KiCad 原理图库编辑器从头开始创建原理图符号可能会非常繁琐。 [KiPart](https://kipart.readthedocs.org/en/latest/) 是一个 python 脚本，它使用 CSV 表作为其输入来生成 KiCad 逻辑示意图符号，并能够创建多部分符号。用法相当简单。csv 文件的第一行需要一个零件名称。下一行包含标题。Pin 号和 Pin 名是最低要求。此外，您可以添加“单位”、“侧面”、“类型”和“样式”。定义多单位零件时使用单位。Side 决定了 pin 的位置，Type 决定了它的功能，而 Style 则是它的图形表示。运行 KiPart python 脚本会生成一个漂亮的 KiCad 逻辑示意图符号。此外，KiPart 可以专门为 Xilinx 7 系列 FPGAs 和 Cypress PSoC5LP 生成原理图符号。有一大堆选项可用于定制最终输出，例如根据引脚编号、引脚名称或引脚功能对引脚布局进行排序。源文件可以从【xess corp】[Github 资源库](https://github.com/xesscorp/KiPart)获得。

### KiCost

[xesscorp]的另一个有用的工具是 [KiCost](https://kicost.readthedocs.org/en/latest/) 。它旨在作为脚本运行，为使用 KiCad 开发的电路板生成零件成本电子表格。您需要添加到原理图零件中的一条信息是制造商零件号。KiCost Python 脚本随后处理 BOM XML 文件，读取制造商部件号，从几个流行分销商的网站上搜集价格和库存数据，并创建成本计算电子表格。你可以从 [KiCost Github 库](https://github.com/xesscorp/KiCost)获取源文件。

查看下面的两个视频，其中[Dave]介绍了这两个实用程序。

感谢[RoGeorge]通过评论我们最近报道的由[Dave]构建的[开源 FPGA Pi Hat](http://hackaday.com/2015/10/10/open-source-fpga-pi-hat/)来发送这个技巧。

 [https://www.youtube.com/embed/hX4l8i4TSWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hX4l8i4TSWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/AeccxROpDfY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AeccxROpDfY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

