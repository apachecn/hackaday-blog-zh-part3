# 公主和硬盘:糟糕的设计选择

> 原文：<https://hackaday.com/2017/05/04/the-princess-and-the-hdd-poor-design-choices/>

你们都会记得我买一台复印机的大冒险。嗯，我告诉你，这真是一次过山车。虽然我仍然没有找到一个值得尝试的修改，我已经变得越来越沮丧。有时，我喜欢邀请我的朋友和家人来吃晚饭，谈话自然会转向墙上的艺术品、水族馆里的鱼，或者客厅里的复印机。现在，我非常喜欢与他人分享我的激情，所以当我去打印几份却发现机器无法启动时，我感到非常失望！是彻底解决这个问题的时候了。

通电后，复印机会在“请等待…”屏幕前停留很长时间，最终咳出一个错误代码——sc 990——和一个呼叫服务的指令。一堆其他的信息也会闪现出来；通讯录数据错误、硬盘数据错误等等。最后我意识到它们都围绕着数据存储。

![](img/c46f23ec21a71aae3af7fc026fbc81fb.png)

Pictured: the author, in his happy place, at peace with the copier.

现在，我已经尝试过一次进入服务菜单，并选择了格式化硬盘的选项。这导致问题消失了一段时间，但现在又回来了。这次再怎么敲键盘也没用。格式命令每次都简单地返回“失败”。下一步做什么？你猜对了，是时候拆了！

谢天谢地，复印机设计得很容易维修——有人为所有这些服务电话付费。几个螺丝和大型面板只是轻松地弹出；[与修车完全相反](http://hackaday.com/2017/04/25/different-differentials-the-pitfalls-of-the-easy-swap/)。发现硬盘很容易，它看起来像某种笔记本电脑的 IDE 装置。由于家里只有 SATA 笔记本电脑可以回收零件，我无法找到可以替换的东西。

一点研究(并阅读标签)告诉我，驱动器是东芝 MK2023GAS/HDD2187。易贝上有替代品，但如果我等两个星期，我可能会被其他一些废弃的设备缠住。它必须在晚上被分类。用[AvE]的话说，如果你修不好……好吧，你知道它是怎么回事。我猛拉驱动器，瞧，复印机直接启动了！为了确保我没有产生幻觉，我粗制滥造了几份，除了继续卡在全黑的页面上，一切都很好。实际上，让复印机启动所要做的就是把有问题的驱动器取出来。可以说，我有点目瞪口呆。

![](img/18325f2790de82b5e101e58695d30359.png)

The hard drive a.k.a. the villain of the piece.

我很高兴取得胜利，但我不得不在这里提出理光设计的问题。这台复印机显然没有硬盘也能很好地运转。它将放弃它的文档服务器和地址簿功能，但它仍然可以毫无问题地进行复印和打印。

然而，当复印机的驱动器发生故障时，该装置就会完全失灵并拒绝工作。对于普通用户来说，这需要一个服务电话才能让任何事情再次发生——导致大量工作和生产力损失。在我看来，一个更好的设计应该是让复印机通知用户由于驱动器故障而失去的功能，并需要呼叫服务，但让他们复印！任何 IT 管理员都会知道，相对于一屋子无所事事、焦虑不安的 40 名员工而言，让公司艰难度日的繁重工作有多重要。很遗憾理光选择彻底关闭复印机，而不是勇敢地继续工作。

欢迎在评论中分享你自己的导致完全关机的小故障故事。休息下的视频。

 [https://www.youtube.com/embed/mv6WX6_hIV4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mv6WX6_hIV4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

