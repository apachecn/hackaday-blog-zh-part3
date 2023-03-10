# 骗局

> 原文：<https://hackaday.com/2016/08/30/shell-game/>

我们很多人花大量时间在 Windows 和 Linux 之间切换。现在像 Raspberry Pi 这样的平台很受欢迎，这个数字可能每天都在增加。虽然我几乎在我所有的电脑上都运行 Linux(笔记本电脑除外)，但我的工作电脑大多运行 Windows。笔记本电脑也是 Windows 操作系统，因为我厌倦了试图让所有花哨的旋转传感器和笔功能在 Linux 下正常工作。

我最讨厌 Windows 的地方是很难看清引擎盖下发生了什么。我的惠普笔记本电脑使用廉价的戴尔有源手写笔。算是吧。这是伟大的，除了周围的屏幕边缘，它去野生。校准从来不起作用。在 Linux 上，如果我愿意，我可以深入到操作系统的最底层。对于 Windows，这很难。

## 战争是外壳

Linux 一直比 DOS 和 Windows 有优势的一个地方是 shell。Linux 下有很多变体，但是 bash 似乎是大多数人当前的选择。如果你想要更强大的功能，你可以转向其他选择，但是如果你学会了如何使用 bash，并且有了合适的外部程序，即使是 bash 也是非常强大的(如果你不相信，看看这个 web 服务器)。

在过去的 DOS 时代，我们中的一些人去了 4DOS，这很好，但没有 bash(显然演变成了 Windows Take 命令控制台软件。我见过少数人在 DOS 或 Windows 下用 Rexx 之类的东西做 shell，但一直是很少的少数。

## Windows 电源

微软最终解决了其默认命令解释器的缺点，首先引入了 Windows Scripting Host 来允许 Javascript 和 VBScript 批处理文件。最终，它被后来被称为 Windows PowerShell 的 Monad 所取代。

除了运行程序，PowerShell 还可以使用函数和 cmdlets(与 Shell 交互的程序)。虽然它与传统的 Linux shell 不兼容，但它有类似的功能，许多人——尤其是系统管理员——大量使用它来自动化任务。

## 炮弹冲击

最近发生的两件事让我很惊讶。首先，[微软将 bash 作为原生应用程序提供给 Windows 10 的](https://msdn.microsoft.com/en-us/commandline/wsl/about)(和其他 Linux 可执行文件)(你可以在网上找到[详细的安装说明](https://msdn.microsoft.com/commandline/wsl/install_guide))。令人惊讶的不是这是可能的。多年来，我一直使用 [Cygwin](http://cygwin.org/) 和 [UWIN](https://web.archive.org/web/20131104073434/http://www2.research.att.com/~astopen/download/) 在 Windows 下拥有一个非常全功能的 Linux 环境(在 DOS 下使用 [MKS](https://www.mkssoftware.com/) 也是如此)。令人惊讶的是，微软将“跨越溪流”,正式支持 Windows 上的 Linux/Unix 工具。当然，NT 曾经有一个残缺的 POSIX 子系统，但是它并不实用。这似乎是一个真正的尝试，将外壳放在 Windows 上(同样，这是唯一值得注意的，因为这是微软在做)。

第二个让我惊讶的消息是，你现在可以获得用于 Linux 的 [PowerShell 或 OS/X](https://github.com/PowerShell/PowerShell/tree/master/docs/learning-powershell) 。我不确定有多少 Linux 用户会急于使用. NET 工具，但这是使系统更相似的另一种方式，当你两者都使用时，这是很好的。

## 决定，决定…

所以现在你有几个选择来使用 Linux 和 Windows，而不用在两者之间疯狂切换:

*   运行 Linux，将 Windows 放在虚拟机中
*   运行 Windows，将 Linux 放在虚拟机中
*   随处使用 bash(使用 Cygwin 或微软产品)
*   到处使用 PowerShell

如果你不能忍受从微软拿软件，你可以看看 [PASH](https://github.com/Pash-Project/Pash) ，它本质上是使用 Mono 重写 PowerShell。我不确定它会保持多少势头，因为微软正在支持如此相似的东西。

如果你确实想了解更多关于 PowerShell 的知识，维基百科上的文章有一个很好的表格，将 PowerShell、cmd.exe 和 Linux shell 联系起来。还有一个视频，你可以在下面看。

 [https://www.youtube.com/embed/XiGGb5v8yAo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XiGGb5v8yAo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[rogeorge]关于 PowerShell 的提示。