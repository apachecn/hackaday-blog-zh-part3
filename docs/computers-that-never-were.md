# 从未有过的电脑

> 原文：<https://hackaday.com/2017/10/13/computers-that-never-were/>

今天学习如何给计算机编程比以往任何时候都容易。每个人都有一个(可能有几个)，并且有大量的可用资源。你甚至可以完全在你的网络浏览器中编程，避免安装编程语言和其他晦涩难懂的软件。但并不总是这样。在六七十年代，你通常在不存在的计算机上学习编程。我最近在思考那些从未真实存在过的计算机，并想知道如果每个新手都有一台计算机，我们是否会过得更好，或者这些虚构的计算设备在教育过程中是否有用。

过去，几乎没有人有电脑。即使你从事计算机行业，你拥有一台完全属于你的计算机的可能性几乎是闻所未闻的。在过去，电脑要花钱——很多钱。它们需要特殊的电力和冷却。他们需要一排人来操作它们。它们占据了很大的空间。让学生运行程序来学习的想法是可笑的。

## 答案

如果你看看那个时期的计算机书籍，它们并不是针对你可以购买的特定计算机的。乍一看，这可能令人惊讶，因为当时没有多少不同种类的计算机。相反，这些书关注的是一些虚构的计算机。这有两个原因。首先，它确保了尽可能多的人可以从这本书中受益——当时的市场比现在小得多。第二，虚构的计算机通常比当时真正的计算机更容易理解。

这最后一点很重要，因为无论如何你都不会被允许运行你的程序。你可以假装成电脑，手动计算出发生了什么，来测试你的想法。你的导师(或者更可能是研究生)会做同样的事情来判断你是否得到了正确的答案。试图模拟特定 CPU 的确切硬件没有多大意义。

然而，这些系统都有一个共同点。他们强迫你真正理解计算机在底层做什么。你不能写一行代码来打印两个数的和。您必须编写操作代码来加载数字，编写加法操作代码，然后理解结果的去向。你必须成为计算机。

你可能会说，其中一些只是学习汇编语言，或者至少是一种低级语言。然而，你会看到，因为对于大多数这些系统(至少在他们的时代)你是计算机，你必须真正了解处理器的工作流程。

## TUTAC

我第一次接触这种技术是在 20 世纪 70 年代从当地图书馆得到的一本书上。即使在那时，这也是一本旧书(1962 年)。事实上，这本书有几个版本的标题略有不同，但我读的是[Theodore Scott]的《基础计算机编程》(计算机编程技术是后来一个版本的标题)。请记住，这是在计算机语言基础出现之前的几年，所以标题仅仅意味着“初级”这是一本不寻常的书，因为它是一本“TutorText”或者我们现在称之为编程文本——就像计算机编程的[“选择你自己的冒险](https://en.wikipedia.org/wiki/Choose_Your_Own_Adventure)。

[![](img/82037007745eac166445e37a4e06a826.png)](https://hackaday.com/wp-content/uploads/2017/10/tutac.png)

如你所见，你读了一小段文字，看了一个问题，然后根据你的答案，跳到另一页。如果你错了，这个页面会向你解释你做错了什么，通常还会提供另一个问题来看看你是否已经解决了。如果你是对的，你会进入一个新的领域。你可以在线阅读整本书，令人惊讶的是，如果你想从零开始学习编程，我会强烈推荐这本书。当然，有些内容已经过时了，但是概念是可靠的。编程文本可能最好放在纸上，所以这可能是你打印出来的 pdf 文件之一。或者找到这本书的纸质版本，这也不是不可能的。

[![](img/d4f6bcb730d8285c05b9ae0b4e70cf90.png)](https://hackaday.com/wp-content/uploads/2017/09/tutor.png) 这本书的内页描述了神话中的机器，TUTAC。它有许多在计算机时代早期变得不常见的功能。例如，TUTAC 使用十进制数。索引是通过让程序重写程序中其他指令的目标地址来实现的。在包含索引寄存器之前，这种情况很常见。幸运的是，这本书的扫描确实扫描了里面的封面，所以如果你真的想看 PDF 格式的书，你已经准备好了。

如果你是少数听说过 TUTAC 的人之一，Python 中有一个[模拟器。坦白地说，我很惊讶还有人记得这个，但显然至少有两个人！](https://github.com/mvanmoer/TUTAC)

## 混合

[![](img/06c4178fa416bb6082a4923f60c43904.png)](https://hackaday.com/wp-content/uploads/2017/09/art.png) 
【唐纳德·克努特】为当时有抱负的程序员写下了后来成为*的*系列书籍。1968 年的第一卷介绍了 [MIX](https://en.wikipedia.org/wiki/MIX) ，一种比 TUTAC 更现代的人造机器。因为这是一本被广泛使用的书，所以很多人学习了 Mix。现在有不少 Mix 模拟器，包括一个 [GNU 程序](https://www.gnu.org/software/mdk/)。

[Knuth]实际上是想在这个系列中写更多，但他一开始只完成了三卷。第四卷的一部分出现在 2011 年，计划有七本。第四卷其他部分的一些草稿可以下载。

混合建筑更现代一点，但还不够现代。[Knuth]建议 MMIX 采用现代 RISC 架构。除了仿真器，至少还有一个 MMIX 的当代 [FPGA 实现，所以真的没资格上这个榜。](https://github.com/tommythorn/fpgammix)

MIX 可以使用二进制或十进制数字，但没有使用完整的 8 位字节，这意味着可以在二进制或十进制中工作的代码不能在一个字节中存储大于 63 的数字。有九个寄存器和一个相当小的指令集。像 TUTAC 一样，MIX 程序经常修改自己，特别是从子程序返回，因为这个架构不包括堆栈。

作为一个有趣的琐事，MIX 不是一个缩写，而是一个罗马数字。MIX 是 1009，[Knuth]对当时常见计算机的型号进行了平均，得出了这个数字。

## 蓝色

我们之前已经讨论过蓝色。它的用途与 TUTAC 和 Mix 略有不同。作为[CAX ton Foster]1970 年关于 CPU 设计的书的一部分，它实际上是如何用逻辑门构建 CPU 的模型。然而，它确实需要被编程，并且有一个让人想起那个时代的 DEC 或 HP 机器的指令集。

至少有一个 Blue 的软件版本和我自己在 FPGA 中的[实现。我特别喜欢前面板设计(见视频)。](https://hackaday.com/2016/03/25/crawl-walk-run-a-starter-cpu/)

 [https://www.youtube.com/embed/dt4zezZP8w8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dt4zezZP8w8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我的蓝色版本在几个重要方面得到了增强。默认情况下，指令集是非常初级的，机器周期考虑了像将数据写回核心内存这样的事情；阅读核心是破坏性的，所以这是必要的。据我所知，在这本书被普遍使用的时候，没有人构建 Blue，因为在原理图中至少有一个错误，并且有几个很容易实现的优化。

蓝色也不是首字母缩略词，而是以不存在的电脑所在的假想柜子的颜色命名的。

## 小人电脑

另一台 60 年代中期的虚拟电脑是“小人电脑”。Stuart Madnick 博士]命名它是因为 CPU 是一个邮件室，里面有一个小人在采取某些行动。今天有相当多的[模拟器](https://peterhigginson.co.uk/LMC/)，甚至有一个[使用电子表格](http://www.engineers-excel.com/Apps/LMC/Description.htm)。

[![](img/941c0728d358fc5c0df4dae8cafe35a3.png)](https://hackaday.com/wp-content/uploads/2017/09/lmc.png)

如果你是一个彻头彻尾的计算机型的人，你很难记得曾经有一段时间你不明白数据是如何从内存传递到执行单元再到算术单元，然后再到更多的存储空间。小人的类比很有帮助，许多现代模拟器将数据流动画化，这非常有帮助。

指令集非常小——在大多数变体中只有 10 条指令——但是你可以编写一些重要的程序。下面的视频是一系列教程中的第一个。

 [https://www.youtube.com/embed/6cbJWV4AGmk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6cbJWV4AGmk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 心脏的

![](img/5fa1a8ed195dd5fa5fd0a6f6c76d543b.png)

贝尔实验室的 CARDIAC(辅助计算的纸板)是这个列表中最不虚构的计算机。20 世纪 60 年代末， [CARDIAC 是一款由纸板制成的电脑](https://hackaday.com/2014/10/14/a-clever-cardboard-computer/)。你把它组装起来，用一支铅笔来执行程序，从不同的寄存器中移动数据。像小个子一样，心脏只有十个指令。

我也做过[一个 FPGA 版的 CARDIAC](https://opencores.org/project,vtach) ，有仿真器包括[离线版](http://www.kaleberg.com/software/cardiac/)和这个[在线版](https://www.cs.drexel.edu/~bls96/museum/cardsim.html)。我甚至写了一个心脏的[电子表格版本，灵感来自一个类似的小人项目。](http://www.drdobbs.com/embedded-systems/cpu-design-on-paper/240153480)

CARDIAC 是高度简化的，更像 TUTAC，带有十进制数字和其他帮助人类解释其程序的东西。比如只有十条指令。你可以在视频中看到心脏的概述。

 [https://www.youtube.com/embed/CW96m7R0u-s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CW96m7R0u-s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



有时你可以从新老库存中购买心脏，或者你可以使用这些扫描图或 T2 再造版打印出你自己的心脏。

## 今天呢？

除了回忆往事，这一切还有什么价值？我认为 Hackaday 的读者可能有点厌倦了。我想几乎所有定期阅读 Hackaday 的读者都相当了解计算机内部的情况。但是如果你刚刚开始学习，这通常是很难理解的。但是如果你在这些类型的计算机上学习或者在低水平上使用真正的计算机，你必须弄清楚或者放弃。

今天，你可以创造出各种各样的好东西，只要把高级组件串在一起，然后用语言把它们粘在一起，这些语言把你从细枝末节中隔离出来，比如计算机如何存储数字、做索引、计算有效地址、处理呼叫和返回。对于生产力来说，这是一件好事。

在电影《空手道小子》(老原那部；我还没有看到新的)，教练让学生做看似平凡的任务，后来转化为武术技能。“上蜡……脱蜡。”也许努力伪装成一台电脑应该是每个人学习经历的一部分。

照片致谢:

计算机编程艺术[Chris Sammis] CC BY-SA 2.0