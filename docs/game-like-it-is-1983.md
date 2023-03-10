# 像 1983 年一样的游戏

> 原文：<https://hackaday.com/2017/07/12/game-like-it-is-1983/>

我见过的第一台计算机——我想——是 IBM System/3。你可能不记得他们了。它们是无法证明大型主机合理性的商业计算机。它们是“中档”不要介意这个东西可能有我鼠标内部 CPU 的内存和处理速度。随着时间的推移，IBM 转向了 System/3x(例如 System/32)。接下来是 AS/400，最后是仍在生产的 IBM i。不过，这里有一个秘密，我见过的在 IBM i 上运行的大多数代码至少可以追溯到 System/3 天前，甚至可能更早。

如果你对历史感兴趣，或者对中型计算机感兴趣(它们的操作类似于大型机)，你可能想实际上玩一玩真的机器。快速浏览一下易贝，我知道你可能花 1000 美元左右就能找到工作。也许吧。那有点多了。如果你能得到免费的时间呢？事实证明，你可以。

## 云选项

前往[PUB400.com](http://pub400.com/)注册一个账户。这不会很快——我的花了一两天。该系统是出于教育目的，所以态度好一点，不要用于商业目的。你得到 150MB 的存储空间(实际上，有些文档说是 250MB，我没有测试过)。当你在等待你的账户时，你需要拿起一个 5250 终端模拟器，调整你的思维，除非你是一个彻头彻尾的 IBM 人。

尽管 IBM i 看起来像是 20 世纪 70 年代的中端产品，但其硬件非常现代，具有 64 位 CPU(架构可以处理 128 位)和众所周知的稳定性。然而，界面是，嗯，怀旧。

## 准备好了…

根据您的主机，有几种 IBM 5250 终端程序可用。他们推荐使用 Java 的 [tn5250](https://sourceforge.net/projects/tn5250/) 或 [tn5250j](http://tn5250j.sourceforge.net/) 。然而，我在我的 Chrome 浏览器中安装了 [Mochasoft 的](https://chrome.google.com/webstore/detail/mocha-tn5250/jfmhmcdjmeoihgkcnjgjopofgeadjhnf?hl=en-US)模拟器。这是一个 30 天的免费试用期，但我想 30 天后我会结束的。

请记住，IBM 喜欢面向屏幕的终端(惠普也喜欢，很多年了)。与我所认为的普通终端不同。所以你在屏幕上移动光标，填满屏幕。当你按下回车键(或某些其他键)时，整个屏幕立刻转到远程计算机。这给了软件应用独特的非交互感觉。在惠普终端上，你可以强迫他们发送击键，你可能在 5250 上可以，但这是不寻常的。普通程序是面向屏幕的。

## 稳住…

例如，大多数情况下，你会通过一些简单的菜单与计算机进行交互(见下文)。你按一个数字，然后回车。整个系统的设置主要是使用神秘的命令运行批处理作业——尽管对于外行来说不比 ls 和 df 更神秘。

当您等待您的帐户时，您可以做一些准备工作。有一份[欢迎文件](https://docs.google.com/viewer?url=http%3A%2F%2Fpub400.com%2Fwelcome.pdf)你会在你的欢迎邮件中收到，你现在就可以开始阅读。您可能需要完成一些针对每个用户的设置，所以请务必阅读这些内容。

也可以看一些教程视频。YouTube 上的 as 400 教程频道有很多，包括一个基本教程，你可以在下面找到。

 [https://www.youtube.com/embed/7980eoVjz08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7980eoVjz08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 走吧。

登录后，按照欢迎文档中的说明进行设置，就可以开始了。去哪里？取决于你想做什么。然而，要了解 20 世纪 70 年代的交互式计算是什么样的，一个好方法是发出以下命令:

PUB400SYS/GAMES

实际上，您可以省略 PUB400SYS/这会把你带到一个菜单，在那里你可以玩当今最先进的电脑游戏。

[![](img/0575665686edbc54e2d798708c967e51.png)](https://hackaday.com/wp-content/uploads/2017/06/gamesbg.png)

如果你想编辑一个文件，试试 EDTF。QSH 有一个类似 Linux 的外壳。不要太激动。我在非常自由的意义上使用类似 Linux 的东西。用“help”代替 man，看看你能做什么。有一个 FTP 客户端，谁知道还有什么。DSPLIBL 命令将帮助您找到库，如果您想尝试，DSPLIB 将列出库中的内容。

随便逛逛，貌似有 Java，RPG，Cobol，C，C++的设施。我肯定 Rexx 也在上面。

## 记忆车道

这些有用吗？我不知道。仍然有很多这样的东西在那里突突作响。我想你可以学一门工作技能。但对我来说，这似乎是一个你不太了解的老计算领域。在“小型”电脑爆炸之前，这些东西无处不在。

请记住，如果您获得了一个帐户，您将使用的 IBM i 是真正的交易。但是如果你想玩一些旧的硬件，并且不介意它是虚拟的，有大量的浏览器选项。你也可以使用 SimH，如果你愿意，甚至可以围绕构建一些[硬件。](https://hackaday.com/2015/03/26/hackaday-retro-edition-remaking-the-pdp-8i-with-a-raspberry-pi/)