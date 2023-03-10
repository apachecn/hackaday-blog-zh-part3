# Hackaday 奖参赛作品:3D 打印机管理系统

> 原文：<https://hackaday.com/2017/06/24/hackaday-prize-entry-a-3d-printer-management-system/>

自从第一台桌面 3D 打印机问世以来，人们就一直试图找到一种方法来管理桌面 3D 打印机，并把它们变成小型自动化工厂。最早的努力之一是传送带构建板，MakerBot 成功地使用了它，直到它不再存在。Octoprint 对任何想要管理几台打印机的人来说都是一个福音，但这只是解决方案的一半。

为了他的 Hackaday 奖参赛作品，[Mike]提出了一个解决方案，将桌面 3D 打印机[变成完全自动化的工厂](https://hackaday.io/project/20960-3d-printer-w-auto-eject-sys-web-print-queue)。该项目不仅负责在打印完成后从床上移除零件，还管理基于网络的打印队列。这是我们见过的最简单的打印机管理方式，也是 Hackaday 奖的绝佳参赛作品。

首先，软件堆栈。[Mike]开发了基于网络的队列和切片软件，该软件可以接收 3D 模型并将代码输出到打印机。这真的不是什么新鲜事。Octoprint 做到了，Astroprint 做到了，甚至少数 3D 打印机也有这个能力。虽然这只是项目的一部分，但它更像是一个创客空间管理软件，而不仅仅是一个专用的 3D 打印机控制器。

然而，如果没有自动化的构建板，你就不可能有自动化的迷你工厂，在这里[Mike]提出了一些非常棒的东西。他的打印完成后分发的解决方案非常简单。你要做的就是把地板从指纹下面放下来。[Mike]的解决方案是活板门打印床。在打印开始时，喷墨打印机吐出一张纸，上面有几行文字，放在打印床上。打印完成后，步进电机会松开电缆，打印下方的活板门会打开。零件落入箱中，门关闭，下一张照片被载入队列。这非常简单。

休息过后，你可以看看[Mike]对这个系统的演示。这太棒了，而且非常简单，我们很惊讶以前没有人想到这一点。

 [https://www.youtube.com/embed/pEV_lTtuz6U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pEV_lTtuz6U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)