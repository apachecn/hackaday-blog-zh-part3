# 走向更自动化的打印机

> 原文：<https://hackaday.com/2018/04/29/towards-more-automated-printers/>

3D 打印机可以用于制造业。这可能会让那些已经等了几个小时的廉价口袋妖怪打印品的人感到惊讶，但对于低产量的塑料零件，你实际上可以用几台 3D 打印机来运行生产线。3D 打印机的问题是打印完成后要剥离。要是有一种传送带解决方案能让 MakerBot 不会忘记床就好了。

[Swaleh]可能有办法解决非自动化 3D 打印机的问题。他正在设计一款名为 WorkHorse 3D 的打印机，这款打印机使用传送带作为床。打印完成后，传送带向前滚动，将打印好的零件放入箱子中。这是真正自动化印刷的解决方案。

使用传送带来自动化一批 3D 打印并不是一个新想法。很久以前， [MakerBot 发布了自动化构建平台](https://www.thingiverse.com/thing:4056)，并在生产中使用它来打印出用于物联网的部件。由于某种原因，这种开放的硬件被遗弃了，去年，一种新型的基于传送带的打印机被发明了，[【比尔·斯蒂尔】的无限容量打印机](https://hackaday.com/2017/03/25/mrrf-17-the-infinite-build-volume-printer/)(因为没有更好的名字)。这台打印机将打印床倾斜 45 度，理论上允许打印无限长的内容。这个想法变成了 [Printrbot Printrbelt](https://hackaday.com/2017/06/30/printrbot-teases-infinite-build-volume-printer/) ，大约在同一时间 [Blackbelt 3D 打印机](https://hackaday.com/2017/05/12/another-printer-with-an-infinite-build-volume/)被公之于众。

[Swaleh]的打印机不属于无限生产量类型。大部分工程工作并没有专注于制造长光束，而是致力于制造一台只用于打印的打印机。传送带床是平的——可能不幸侵犯了 MakerBot 的专利——但如果你想要一台像非常慢的注塑机一样倾倒零件的打印机，这就是你想要的设计。

这个项目的打印队列应用程序只是一个简单的桌面应用程序，用作 g 代码文件的缓冲区。该应用程序将一个 g 代码文件发送到打印机，向前滚动床，并排队等待下一个零件。这很简单，是的，但现在没有太多的东西这样做，因为没有太多的打印机被建成工厂。令人印象深刻，你可以在下面看看这台打印机的几个视频。

 [https://www.youtube.com/embed/b-P3RYLnlww?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/b-P3RYLnlww?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/-25e5qcELvw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-25e5qcELvw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)