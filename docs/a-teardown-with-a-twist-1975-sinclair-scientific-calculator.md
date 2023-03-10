# 一拧就拆:1975 年辛克莱科学计算器

> 原文：<https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/>

当我最近写一篇关于反向波兰符号(RPN)的文章时，作为写作的一个挂钩，我从存储器中取出了我的辛克莱科学计算器。这是科学计算器起源中的一个重要模型，不是因为它是一个开拓者，甚至不是因为它特别好，而是因为它有趣的操作方式，以及它是第一个价格合理的科学计算器之一。

我在 20 世纪 80 年代的一次清仓大拍卖中买了这个计算器，修补了它坏掉的电池夹，让它活了起来，并在我的长凳上放了几年。即使在 20 世纪 90 年代初(即使你没有使用它)，在你的长凳上放一个复古计算器会给你一点街头信誉。但是当生活在我周围移动的时候，它进入了那个储存箱，直到 RPN 的那篇文章，它一直呆在那里。找到它是一项艰巨的任务，要在它已经存在了 20 年的储物盒中找到一块糖大小的东西，这是在满是类似盒子的略显混乱的一对架子中。

[![The Sinclair's clean design still looks good four decades later.](img/463740adf44766094b1a93f294db4c44.png)](https://hackaday.com/wp-content/uploads/2017/10/sinclair-scientific-angled-view.jpg)

The Sinclair’s clean design still looks good four decades later.

作为一个成年人来看它，很明显这是一个有趣的机器，值得更仔细的研究。接下来的事情不会是辛克莱科技公司在网上的唯一一次拆解，毕竟没有人能比得上[【肯·希尔里夫】对其芯片内部的检查](http://files.righto.com/calculator/sinclair_scientific_simulator.html)，但它应该会让人们深入了解计算器的构造，并为 20 世纪 70 年代消费电子产品的爱好者提供大量令人满意的图片。

辛克莱号被一个坚硬的黑色塑料外壳保护着，这意味着它已经完好地存活了几十年。在箱子里面是它的 RPN 语法和科学功能的一张复制表，当它执行任何计算的时候是一个无价的帮助。

它与早期的 Sinclair Cambridge 有着相同的外部设计，这是一个更不起眼的算术计算器，但 Cambridge 的塑料是黑色的，而 Scientific 是白色的。LED 显示屏位于紫色窗户后面，蓝黑键盘占据了前面板的三分之二。在 50 x 111 x 16 毫米，这是一个真正的袖珍计算器，其优雅的同时代人未能实现，这肯定是最先进的计算器无法比拟的。好的工业设计不会老化，虽然辛克莱的设计使它明显是 20 世纪 70 年代早期太空时代美学的产物，但它本身仍然是一个有吸引力的项目。

[![The Sinclair Scientific circuit board, component side.](img/8587e435795e8d0209bc567656a3565a.png)](https://hackaday.com/wp-content/uploads/2017/10/sinclair-scientific-board.jpg)

The Sinclair Scientific circuit board, component side.

在背面，只有电池盒的夹式盖子，位于键盘下方。打开它可以看到键盘 PCB 的底部，上面有一个标签，显示电池的方向和一组 4 节 AAA 电池的弹性电池夹。其中一个夹子被一个漏液的电池腐蚀了，当我拿到计算器时，夹子断了，需要在电池和夹子之间放一片铜箔来操作。标签推荐金霸王 AAA，在 20 世纪 70 年代中期并不便宜。在静止状态下，计算器从它们那里消耗 35 mA 电流，所以没有钱的所有者必须确保在计算后立即关闭它。

外壳的上半部分和下半部分用模制夹子固定在一起，这意味着只要小心就可以撬开它们，露出电路。在这个例子中，有一个夹子坏了，遗憾的是，我不记得这是否是由一个热情但无能的年轻的我造成的。移除后面板后，带有 1975 年 3 月日期代码的 TMS0805 计算器芯片的 28 引脚双列直插式封装以及两个驱动器芯片和 Bowmar LED 显示模块映入眼帘。最后一个元件与 PCB 齐平安装在铣成的凹槽中。有一些分立元件，包括一个电感和一组二极管，可能是一个简单的逆变器来产生电源轨。后来的 Sinclair 计算机的拥有者可能会发现这些反相器电路很熟悉。

[![The Sinclair Scientific, keyboard side.](img/4e2e159558294f396e46ced1887d5d38.png)](https://hackaday.com/wp-content/uploads/2017/10/sinclair-scientific-board-keyboard-side.jpg)

The Sinclair Scientific, keyboard side.

TMS0805 是这款计算器之所以有趣的根本原因，它是一款为更简单的算术计算器设计的芯片，由于一名出色的员工，Sinclair 在其上成功地放置了科学计算器的代码。按照 2017 年的标准，它的 28 引脚双列直插式封装似乎很大，但 Sinclair 在尽可能小的空间内包装它和它的辅助设备方面做得非常好。从线条来看，这显然是一块手工制作的木板。

这个计算器拆卸的其余照片在下面的画廊，应该为老式计算器爱好者提供大量的素材。然而，这并不是我的 Sinclair Scientific 的故事的结尾，因为它有一个非标准的功能，即文章标题中提到的扭曲。它的第一个主人在它的背上刮了他的签名，使它个性化，所以我能够找到他，并询问使用过这些机器的人它是什么样子的。

[![Turn it over, and there's the signature.](img/f2111f6b7afa1aa1d354cbe36d3d80f5.png)](https://hackaday.com/wp-content/uploads/2017/10/sinclair-scientific-signature.jpg)

Turn it over, and there’s the signature.

一个陌生人突然给你发电子邮件，询问你四十多年前拥有的一台计算器，这一定是一种奇怪的体验，但牛津大学纳菲尔德医学院的名誉教授约翰·斯特拉德林从容应对。毫无疑问，它是如何在我这个牛津的 80 年代少年身上找到的。

[斯特拉德林]教授现在已经退休，但仍是一名活跃的医学研究者和科学家。他作为一名初级医生购买了 Sinclair，并告诉我这在当时是“必须拥有”的配件，因为需要对药物或液体进行大量计算。他透露，数学不一定是许多医生的强项，教育系统选择学习生物学的学生，像辛克莱这样的计算器的出现对他们来说是一个福音。

我们今天认为计算器是理所当然的，它是智能手机上的一个应用程序，或者如果它是一个物理设备，它是一个轻量级和超薄的机器，功能远远超过 Sinclair 上的功能，它几乎不需要电力。因此，一瞥科学计算器的起源，并直接了解在计算尺时代拥有一台计算器意味着什么，是很有趣的。Sinclair Scientific 不是第一个袖珍科学计算器，也不是那个时代最好的。但是，使用一种从未打算用于这项工作的芯片来开发它的故事是一个迷人的故事，如果我们曾经见过一个真正的黑客。虽然今天它不会是你从 choice 中接触到的机器，但它仍然是一个在极其紧凑的外形中具有令人愉悦的美感的机器。你可能会很幸运地在今天的清仓大甩卖中找到一个，但是如果有一个出现在你面前，赶快抢购吧。同时，享受我们的辛克莱科学的内部画廊。

[![Comparison with a more modern calculator.](img/22dda06e78f8d63beedee91a526a9898.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171021_111858664_hdr/)

Comparison with a more modern calculator.

[![A compact hand-held form factor.](img/aaa532974f5d637d25520abf61f8b4f6.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_143341958_hdr/)

A compact hand-held form factor.

[![It lives!](img/91e885bd0f7cae040fa1f25dd5a5923f.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_143111579_hdr/)

It lives!

[![TMS0805 close-up.](img/0c60fb5aad5bb37f2d996dad818309d3.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_141236183_hdr/)

TMS0805 close-up.

[![Case halves, and PCB.](img/4e5fbdb5d6772ee9f1b01a71312ff355.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_141129834_hdr/)

Case halves, and PCB.

[![Circuit board, keyboard side.](img/95f19199e7a48e1f17787b725ff7dcbc.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_141149171_hdr/)

Circuit board, keyboard side.

[![Circuit board, component side.](img/209bceac9714e175f3941818194506b8.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_141026836_hdr/)

Circuit board, component side.

[![Top view.](img/ecf975a793b935243346d05ed81a8503.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_140515648_hdr-copy/)

Top view.

[![Battery compartment, with corroded connector.](img/7b932f2ea967b33cf7b668664b70f1fe.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_140757591_hdr/)

Battery compartment, with corroded connector.

[![Overview of the calculator.](img/6a0e816ab2985cf16f70a543f6a627b2.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_140616694_hdr/)

Overview of the calculator.

[![Close-up of the RPN crib sheet.](img/0dbf6589bfddd88537e42c68d325ed94.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_140450208_hdr/)

Close-up of the RPN crib sheet.

[![The case has an RPN crib sheet.](img/e4aec0469cf05e45bf5fe5cb44e59156.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_140428166_hdr/)

The case has an RPN crib sheet.

[![Back view, with batteries.](img/59868dab568629a56c2c2ddce74bdef3.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_143144312_hdr/)

Back view, with batteries.

[![First look inside the Sinclair Scientific.](img/a3c3889f138b6740f16f13d93df715b4.png)](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/img_20171015_140959873_hdr/)

First look inside the Sinclair Scientific.