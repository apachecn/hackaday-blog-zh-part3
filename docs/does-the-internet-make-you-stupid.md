# 网络让你变傻了吗？

> 原文：<https://hackaday.com/2015/12/08/does-the-internet-make-you-stupid/>

[Christian Heilmann] 最近发表的一篇[文章是我最近读到的几篇关于网站——尤其是堆栈溢出——如何孕育出一种新型开发者的文章之一。这种开发人员只是简单地复制和粘贴示例代码或原理图，并不真正了解发生了什么。他的结论是，不完全了解自己在做什么的开发人员会变得不感兴趣，筋疲力尽。他说的是软件开发人员，但是我认为你可以将这个论点扩展到所有类型的开发人员，包括硬件黑客。他总结道——至少在学习的时候——你会坚持旧的做事方式。](https://www.christianheilmann.com/2015/07/17/the-full-stackoverflow-developer/)

我很难不同意[克里斯蒂安]的细节，但我不同意结论。人们从其他来源抄袭作品已经有很长时间了。在互联网出现之前，我们都见过明显是从数据手册中撕下来的电路，甚至是从多个数据手册示例中粘在一起的电路。

今天有两件事略有不同:首先，每个人都可以很容易地获得大量的例子。你不必去找一本书(可能在图书馆)，搜索它，找到一两个例子。快速搜索一下谷歌就会发现几十或几百个例子。

第二个不同之处是，有些地方像堆栈溢出一样存在，你甚至不必去寻找。你可以简单的问“我怎么做 X？”你会从某人那里得到答案。它可能是错误的。你可能不明白。但你可能会得到某种答案。

我怀疑黑客社区比普通人做得少。我们想要创造自己的东西，即使有时候这并没有太大的意义。但即便如此，我们大多数人还是会在某处划清界限。你真的想开发一个 BSP 并把 Linux 移植到你构建的每块板上吗，或者你买一个 Raspberry PI 或者 BeagleBone？(是的，在你评论之前，我们知道你实际上用机器码为每个项目编写你自己的定制操作系统。)

然而，如果你没有那种黑客心态——今天并不是每个做硬件和软件开发的人都有——从架子上抓东西就是一个大胜利。特别是在工作场所，这是被鼓励的，尽管它并不总是最好的主意。我认为问题在于我们正处于转型期。互联网从根本上改变了我们的工作方式，但我们的教学方式还没有完全跟上。

几年前成为一名工程师、设计师或创造者意味着你必须知道如何解决棘手的问题。有时这需要研究，而这种技能的一部分是知道你在哪里很有可能找到某个特定主题的信息。当然，做一名精通研究的问题解决者(根据我们对这个词的定义，黑客几乎总是符合这个描述)仍然有价值。但是它不像以前那么值钱了。我们需要学习(并教授)一项新技能:使用互联网研究。现在，我认为这有几个关键部分:

*   制定相关的查询
*   询问相关、完整且合理的问题
*   评估你所发现的相对价值
*   根据你的具体问题调整你的发现

虽然有一些课程讲述如何进行搜索，但大多数都集中在第一个方面——查询。只有少数几个人(像来自伯克利的[这个](http://www.lib.berkeley.edu/TeachingLib/Guides/Internet/Handouts.html)或者来自英国的[这个](http://www.bristol.ac.uk/library/support/findinginfo/evaluation/))会考虑批判性地评估你的发现，但是如果你试图将一个原理图或者一段代码整合到一个工作设计中，即使这样也不够。

## 制定一个查询

我知道这看起来很愚蠢。但是一次又一次，有人问我一个问题，这个问题可以用谷歌搜索的第一个结果来回答。他们通常会尝试，但很明显，能想出正确搜索词的人(知道如何使用谷歌提供的高级操作符)和不能想出正确搜索词的人是有区别的。我努力克制让问我这种问题的人感到羞耻的冲动。

## 问问题

![Yes, of course someone actually asked this question](img/fc9ccba671efc9efb07c33dfaef43c12.png)

Yes, of course someone [actually asked this question](https://answers.yahoo.com/question/index?qid=20070216225736AAciATU)

我希望他们能在你高中毕业前要求上一堂提问课。去任何一个问答网站，你都会发现一些一般性的问题，比如:我如何制造一个机器人？在光谱的另一端，你有 42 页的问题，只有最无聊的人才会费心去阅读并内化，以提供一个合理的答案。网上有一个关于如何提出好问题的[好文件，值得一读。](http://www.catb.org/esr/faqs/smart-questions.html)

## 评估价值

![Yes, this gas can strapped into car seat instead of the baby actually happened.](img/0b4342193bff46e5d9b35408c947b959.png)

Yes, this gas can strapped into car seat instead of the baby [actually happened](http://latino.foxnews.com/latino/news/2012/06/06/what-wrong-here-gas-can-safely-fastened-toddler-on-lose/)

令人震惊的是，并非互联网上的一切都是正确的。即使事情是正确的，它们也可能不适用于你的情况。例如，如果我问你“最好的卡车是什么？”你可能会给我一个非常合理的答案，直到我透露我需要运输汽油。在过去，你认为任何印在书、杂志或供应商数据表上的东西都至少要经过作者以外的人的审查。这并不能确保它是正确的和高质量的，但它确实倾向于剔除最明显的不良内容。由此得出的推论是:要评估它，你必须理解它，而不仅仅是相信它。你需要考虑信息来源，并与你所知道的信息进行对比，以确定信息是否正确。

## 调整答案

没有一个答案有可能完全符合你的要求。事实上，当进行新的开发(或者使用不同的工具)更容易的时候，我经常看到人们很难做出合适的东西。重用通常是一件好事，但并不总是如此。理想的情况是，在你使用某样东西之前，你会完全理解它，这样你就可以根据你的具体情况来使用它。

## 禁止上网？

我喜欢认为我们大多数人都足够聪明，不会欺骗自己。你知道，如果你在一个类中作弊，你不会真正从中受益，我可以想象任何有足够动力自己构建项目的人都会花时间去理解他们重用了什么，这很好。当有外部实体(比如老板或老师)给你施压时，事情就变得更复杂了。

然而，我认为重用互联网上的东西是新景观的一部分，它不会消失。例如，人们很容易感叹计算器让学生的数学变得太容易了。但是答案并不是禁止计算器。你必须改变基础数学的教学方式。

所以当[Christian]谈到“全栈溢出开发者”时，我认为他没有抓住要点。能够有效地从互联网中挖掘可能的解决方案、评估它们并加以调整的开发者将会胜出。我们只需要让人们有这样的心态，停止盲目重复使用我们不理解的东西。我们应该教授如何处理基于互联网的重用，这是你需要掌握的另一个工具。