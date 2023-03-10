# 冷静:这只是汇编语言

> 原文：<https://hackaday.com/2018/06/19/calm-down-its-only-assembly-language/>

基于【Ben Jojo】的标题——[x86 汇编不一定要吓人](https://blog.benjojo.co.uk/post/interactive-x86-bootloader-tutorial)——我们假设正常的程序员都害怕汇编。大多数黑客并不介意，但我们也并不经常有借口为台式电脑编写汇编程序。

事实上，这篇文章非常适合典型的黑客，因为它关注的是 x86 处理器启动后的真实模式。让本教程比通常的讲座更有趣的是，它有交互区域，在那里，一个 VM 在与 NASM 组装后在浏览器中运行你的代码。

我们真的很喜欢那种先读一点，然后在浏览器中玩一些代码的格式。看着一台虚拟电脑在你的浏览器中启动，有种超现实的感觉。是啊，我们以前见过，但它仍然让我们的眉毛向上一点点。

我们希望他将继续这个系列，因为现在它在谈论一些 BIOS 功能后停止。我们很乐意看到更多关于指令、索引、字符串前缀，甚至是运行在 Linux 或 Windows 下的代码。如果有一些关于设置本地环境的信息也是不错的。现在，如果你想做一个严肃的投资，并且你使用 Linux，[这本书](http://www.egr.unlv.edu/~ed/assembly64.pdf)很难读懂，但是会回答你的问题。

当然，有许多教程，但这是一个有趣的简单介绍。如果你想了解更多关于浏览器外的[汇编，我们已经讨论过了。如果你真的想给](https://hackaday.com/2016/06/14/linux-assembly-required/)[写一个真正的引导程序](https://hackaday.com/2017/10/23/write-your-own-x86-bootloader/)，这里也有帮助。