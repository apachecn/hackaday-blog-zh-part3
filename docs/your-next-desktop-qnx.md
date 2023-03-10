# 你的下一个桌面… QNX？

> 原文：<https://hackaday.com/2017/05/03/your-next-desktop-qnx/>

作为嵌入式操作系统，QNX 有着漫长而曲折的历史。QNX 一直以其微内核架构的实时操作系统而闻名。也就是说，内核函数作为一组协调的任务运行，而不是作为一段单独的代码。最近发布的 QNX 7(见下面的视频)允许它在 64 位桌面计算机上运行，并且[elahav]决定着手将这个嵌入式 RTOS 转变为桌面操作系统。

这听起来可能有点牵强，但是 QNX 是一个 POSIX 兼容的系统，拥有你在 Linux 或 BSD 这样的系统中所期望的所有特性。它只是不针对桌面市场，因此没有很多运行桌面的工具。QNX 不是你在 Arduino 上看到的那种 RTOS。更常见于汽车系统之类的东西(比如运行通用汽车的 OnStar 系统)。

他从一个迷你 ITX 板开始，安装了 QNX。通常，你在一个工作站上为一个嵌入式系统开发，然后将代码发送到目标系统，但是[elahav]花时间让一个构建系统在目标系统上工作。有一个问题。按照现代标准，内置的 vi 编辑器是原始的。他通常是 emacs 用户，但即使是 vim 也比“股票”vi 要好。虽然 emacs 移植是可能的，但也需要移植大量的库，所以他的第一个项目是编译 vim 源代码。

结果并不像他希望的那么容易。构建系统期望某些尚未存在的 GNU 工具(尽管这些工具的标准版本，如 grep，确实存在)。所以他必须想办法交叉编译 vim。回想起来，[elahav]决定他应该首先移植 GNU 工具。他确实不得不从 vim 中删除一些针对旧版本 QNX 的旧代码。

其余的冒险进行得相当顺利。他在几场比赛中成功打造了 SDL 和波特。Qt 存在于 QNX 上，但是它的设置更倾向于嵌入式系统(例如，一切都全屏显示)。构建 Qt 应用是可能的，但是没有合适的窗口管理器，这仍然不是他想要的桌面体验。几周后，他管理了一个窗口管理器。请记住，QNX 的显示架构不是 X，所以抓取现有的一段代码是不太可能的选择。

实用吗？也许吧，虽然我们没有看到实际可用的代码。是否可取？可能不会，除非你已经在用 QNX 了，即使那样我们也不确定。然而，这是一个很好的故事，讲述了让一些与众不同的东西变得有用所涉及的困难，这个问题我们之前在[构建自己的 CPU](https://hackaday.com/2015/07/31/build-your-own-cpu-thats-the-easy-part/) 时已经提到过。当然，[elahav]从一个相当富裕的环境开始。如果你想看某人几乎所有的东西，请查看 A2Z[。如果你已经存在了一段时间，并认为你记得另一个 QNX 桌面环境，](https://hackaday.com/2017/01/13/fpga-computer-covers-a-to-z/)[，你没有错](http://toastytech.com/guis/qnxdemo.html)。

 [https://www.youtube.com/embed/ClxZCsYOe04?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ClxZCsYOe04?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

