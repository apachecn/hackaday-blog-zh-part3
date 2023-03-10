# 使用…嗯…任何东西来破解你自己的 Lisp 语言

> 原文：<https://hackaday.com/2017/03/30/hack-your-own-lisp-language-using-well-anything/>

Lisp 是一种有趣的计算机语言，你要么喜欢，要么讨厌。但它确实经受住了时间的考验。在所有仍在实际使用的古代语言中，只有 FORTRAN 比它老，而且只老一岁。如果你曾经想学习 Lisp，[Kanaka]有一个有趣的方法:研究如何用你最喜欢的语言构建你自己的 Lisp。

如果你最喜欢的语言是晦涩难懂的东西怎么办？[Kanaka 的] GitHub 页面有不少于 64 种不同的 Mal (Make a Lisp)实现，每一种都使用不同的语言。不出所料，C 和 Python 都榜上有名。然而，Forth 和 Go 以及 Awk 也是如此。对你来说还不够奇怪吗？Make 怎么样？是，Make，就像你用来构建程序一样。Bash、Postscript 甚至 VHDL 都有条目，尽管——令人惊讶的是——没有 Verilog 我们不知道为什么。

Mal 的每个实现都被分成十一个增量的、独立的、可测试的步骤，这些步骤展示了 Lisp 的核心概念。最后一步实际上可以运行自身的副本——这是 Lisp 等令人费解的语言的典型特征。有一个[向导](https://github.com/kanaka/mal/blob/master/process/guide.md)以您选择的语言帮助您浏览整个流程。建议是在您自己编写代码之前，不要查看存储库中的代码。您可以在下面的视频中看到[Kanaka](也称为[Joel Martin])最近就 Mal 流程发表了讲话。

如果您没有使用过 Lisp，您可能会认为它代表“大量恼人的假括号”，而不是“列表处理”如果你用 emacs，你用 Lisp 已经很久了。据说至少 Reddit、Orbitz 和雅虎商店都使用 Lisp。我们甚至在[微控制器](https://hackaday.com/2016/09/13/microlisp-lisp-for-the-avr/)和[树莓 Pi 操作系统](https://hackaday.com/2015/09/23/old-lisp-languaged-used-for-new-raspberry-pi-os/)上见过 Lisp。

虽然通过构建来学习 Lisp 是一个崇高的目标，但我们不禁认为这个库对于那些只想比较编程语言的人来说可能是有用的。我们也不禁想到了 [JONESFORTH](https://hackaday.com/2017/01/04/browsing-forth/#more-237402) ，它通过构建一个 FORTH 解释器教会了很多人 Forth。

 [https://www.youtube.com/embed/jVhupfthTEk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jVhupfthTEk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/X5OQBMGpaTU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/X5OQBMGpaTU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

