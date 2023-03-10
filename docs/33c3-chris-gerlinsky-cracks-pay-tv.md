# 33C3:克里斯·格林斯基破解付费电视

> 原文：<https://hackaday.com/2016/12/27/33c3-chris-gerlinsky-cracks-pay-tv/>

在广泛的领域中具有令人难以置信的能力的人是罕见的，当他们展示他们的工作时，这可能看起来似乎很简单。[Chris Gerlinksy]关于破解卫星和有线付费电视机顶盒上使用的加密的[演讲是这样的。(](https://media.ccc.de/v/33c3-8127-how_do_i_crack_satellite_and_cable_pay_tv)[下载幻灯片](https://fahrplan.events.ccc.de/congress/2016/Fahrplan/system/event_attachments/attachments/000/003/101/original/33C3_-_How_Do_I_Crack_Satellite_and_Cable_Pay_TV_slides.pdf)，PDF 格式。)他工作的最终结果是，他可以在付费电视上观看任何东西，但观看免费的摔跤比赛几乎不是像这样的史诗级黑客的目的。

该演讲涵盖了机顶盒本身的硬件逆向工程、芯片去封装、可视 ROM 恢复、软件逆向分析、芯片故障、定制故障硬件的创建、几个级别的加密以及许多非常有教养的猜测。在此过程中，您将了解关于广播流如何加密和传送的所有知识。现在看这个演讲。

一些最酷的东西:

*   从显微镜下读出被掩盖的 ROM 总是让我们吃惊。
*   构建了一个定制的 chip-glitcher 装备，并在几次迭代中展示，最终在一个“花哨”的项目框中结束。但这是那种你可以在家里制作的东西:一个控制试验板上开关的微控制器。
*   编码器芯片将其存储在 RAM 中:[Chris]使用了一种漂亮的自制方法，将电源引脚脱焊，将它们连接到电池上，然后将芯片从电路板上脱焊，以供进一步分析。
*   芯片完全在 RAM 中运行，迫使[Chris]在芯片每次复位时都重新启动芯片并插入他的有效载荷代码。而且它重置了很多，因为设计者在想要的键的字节之间添加了重置向量。非常狡猾。
*   所有这些都是通过牺牲仅仅一卡车机顶盒来实现的。

[![](img/d903e3e29b548667ab60feb95c900b6f.png)](https://hackaday.com/mask-4/)

Looking at Mask ROM

[![](img/a1ddb4de53e18ce2eacd252288096c69.png)](https://hackaday.com/glitcher/)

Homebrew Glitcher

[![](img/b0992d22da154bc9c05c282e7d417d92.png)](https://hackaday.com/2016/12/27/33c3-chris-gerlinsky-cracks-pay-tv/pickup-4/)

A Pickup full of Set-Top Boxes

在这个演示过程中，我们的下巴不断地掉下来。现在就去看吧。