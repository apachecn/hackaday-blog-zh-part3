# 解决黑客日的加密挑战

> 原文：<https://hackaday.com/2016/11/16/solving-hackadays-crypto-challenge/>

尽管在过去的几年里我参加过几次 DEF CONs，但我从来没有抽出时间来解决徽章问题。所有谜题的传奇地位让我有些畏惧。同样，我也还没有尝试过 DefCon DarkNet，这真的很遗憾，因为这种挑战的本质是“焊接你自己的徽章”,这正合我的胃口。

但在 Hackaday SuperCon，我终于尝试了由[Marko Antonic]创建的加密挑战。该挑战被内置到一个二级固件中，任何人都可以轻松地将其闪存到他们的会议徽章中(它列举了一个 USB 拇指驱动器，所以只需复制它)。这就把它变成了一个需要花两天时间解决的五个难题的挑战，而且非常成功。

如果你在展会上没有尝试过，现在是时候了([你不会是唯一一个迟到的人)。但是即使你没有，还是有乐趣的。](https://twitter.com/johnedgarpark/status/795511157306093568)

塔尔在下面洞若观火。我不会明确透露答案，但我会讨论每个谜题是如何呈现的，以及人们用来完成任务的不同方法。如果您想继续，请现在选择，或者等到您自己解决挑战后再选择。

### 1 小时解决:作弊！

首先，唯一的规则是:第一个把解决方案的截图通过电子邮件发给 badge@hackaday.com。在我看来，这意味着没有欺骗，只有实现目标的不同程度的聪明。

加密固件并没有在徽章上发布，而是作为一个预编译的十六进制文件发布(在挑战项目的文件部分可以找到)。更好的是，badge 设计师[Voja Antonic]用汇编语言手工编写了这一代码，因此它没有你在反编译通过 C 编译器运行的二进制文件时会看到的乱码。看看下面的视频，然后挑战自己，理解反编译的 hex。有些人觉得这种事情很有趣，其他人可能认为这是一种折磨。

你可以在挑战项目页面找到编译好的十六进制和汇编源代码[。[Sprite_TM]和[ThunderSqueak]都立即启动了它们的反编译程序，绕过了所有挑战，在不到一个小时的时间里就到达了最终屏幕。你能做得一样好吗？](https://hackaday.io/project/17953-superconference-challenge)

 [![benchoff-crypto-clues](img/93afda0b44fb07e9bb3e9f86eb726da4.png "benchoff-crypto-clues")](https://hackaday.com/2016/11/16/solving-hackadays-crypto-challenge/benchoff-crypto-clues/)  [![benchoff-crypto-red-herring](img/2299af319f781e7366c3482b4dbc473b.png "benchoff-crypto-red-herring")](https://hackaday.com/2016/11/16/solving-hackadays-crypto-challenge/benchoff-crypto-red-herring/) 

### 实际挑战:

[Marko]列出的挑战包括五个不同的回合。当[Brian Benchoff]的演讲(见上图)引发了这场竞赛时，我们得到了一些提示。其中一些是有价值的，而另一些则完全是转移注意力。然后，他将拇指驱动器扔向观众，这是在野外编译的妖术的第一个实例。

 [https://www.youtube.com/embed/MmmL28WOuhk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MmmL28WOuhk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 策划

第一个谜题是基于游戏策划。如果你没有立即认出它，它不应该用很长时间把它与[bench off]的线索联系起来。这个游戏的中心是猜测一个组合。每次猜中后，徽章会告诉你正确的地方有多少正确的值，长的地方有多少正确的值。

对我来说，花了很长时间的是弄清楚游戏是如何正常玩的，然后建立徽章版本在告诉我什么。每次猜中后，你都会得到正确的反馈，我花了半个多小时才弄明白什么是什么。在这种情况下，我试图很快变得非常擅长策划。这是愚蠢的。你有六次机会得到正确的组合，这是一个很高的标准。我建议你采取一种更数学化的方法来赢得胜利。

 [https://www.youtube.com/embed/XqFtaYe2Ebw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XqFtaYe2Ebw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



#### 眨眼，眨眼，眨眼

当面对一组四个 led 一起闪烁时，很容易判断出那里有某种类型的数据。

玩按钮显示字母数字输入是可能的。解码这个闪烁，输入正确的答案，你就可以获得这个挑战的密码。

 [https://www.youtube.com/embed/NBmFB-hYb90?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NBmFB-hYb90?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



#### 走吧。

这一次花了我最多的时间，尽管我作弊了。在会议前几天，[Voja]给我看了这个的 win 屏幕，仍然很难。

棋盘上写着开始。当你摆弄钥匙时，你会发现有四对柱可以上下移动。将它们对齐，你就解决了这个难题。

我知道我在寻找什么，所以我只是不断尝试。但我最初的想法是转录所有的专栏，并编写一个脚本，向我展示每个可能的迭代。我想，如果你一次在一页上放 40 张这样的照片，人眼奇妙的模式识别会让正确的一张跃然眼前——看起来[约翰·派克]也走了这条路。然而，每列大约有 50 行，总共有 6.25 米的组合。

所以不是蛮力的…你会怎么解决这个？

 [https://www.youtube.com/embed/8pGuQu4eFpw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8pGuQu4eFpw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



#### 小盒子

这个挑战向你展示了一个聪明的小旋转光标。摆弄它，你会发现你可以设置或清除 4×4 网格中的任何方框。没有其他指示或反馈。但是把徽章翻过来，你会注意到背面丝网印刷的是一组 4×4 网格的图标。

我认为每个人在这一点上都做了显而易见的事情。尝试输入每个图标。这没有任何作用，但是我和[[谁看见了什么](https://hackaday.io/whosawhatsis)]谈过，因为我知道他已经在做挑战 5 了。他给我的暗示是，这不取决于你进入的顺序。

接下来，我开始编写一些 Python 代码来处理基于字形的逻辑操作。[Voja]路过看到我在做这个。当我们交谈时，我提到我将尝试对每一行符号进行逻辑运算。他给了我一个提示，在那些测试中，你会希望不止使用一行。

有了这两次正确的推动，我很快就通过了这个挑战。

 [https://www.youtube.com/embed/nqALb8ALO9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nqALb8ALO9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



#### ？

最终屏幕！嗯，到那个屏幕本身就是一个技巧。**剧透:**徽章附带的股票固件有一个使用加速度计的滚珠轴承重力演示。当你猛烈摇晃徽章时，它还会掷骰子。我从来没有发现这一点，即使我有徽章在手几个月。这就是为什么如果 SuperCon 的人没有告诉我，我永远也不会发现通过摇动徽章暴露的第五块屏幕。

当你到达那里时，迎接你的是一个问号。玩键盘可以让你输入文本。每个挑战给了我一个代码，我一路写下来。我试着在这里输入，但我有 12 个字母，挑战 5 只需要 8 个字母。

在与[[Krux](https://hackaday.io/krux)谈论此事时，他暗示这可能是一种密码，并让我去找 Rumkin.com 的密码工具[。这是一个很棒的建议，它不仅让我了解了不同的密码，还为你提供了测试它们的工具。大约 20 分钟的闲荡，我受够了！](http://rumkin.com/tools/cipher/)

许多人成功地解决了挑战，但却迟迟没有登上榜首。这项荣誉属于乔纳森·达汗。当我们本周晚些时候报道徽章黑客事件时，我们将分享更多关于他的胜利。

### 新的挑战:仿真

所以，你没有徽章，但你还想玩？这是一种新的挑战。你有编译好的二进制文件，你也有源代码(都可以在挑战项目中找到)。谁将是第一个接受挑战的人，这样你就可以虚拟地玩游戏，而不需要硬件。

如果有帮助的话，我已经有了一个模拟器，它接受箭头输入并显示屏幕的图形表示。但是这使用了 SDL2 库，并且是为可移植的 C 代码准备的。你需要做一些工作来让[Voja 的]汇编代码在其他地方工作。但是如果你做到了，你就做了真正独特的事情，所以给 badge@hackaday.com 发邮件，让我们知道你的成就。在你的模拟器上贴上足够多的关于你是如何做到的细节，你可能会发现你自己已经上了黑客攻击的头版。

如果你正在破解密码挑战，我们想知道。请在推特上用[#超级](https://twitter.com/search?q=%23SuperCon&src=typd)标签发布你的进展 [@Hackaday](https://twitter.com/hackaday) 。