# Linux Fu:对 Bash 的一点帮助

> 原文：<https://hackaday.com/2018/02/02/linux-fu-a-little-help-for-bash/>

如今，程序员的编辑器为您提供关于您正在键入的内容的帮助并不罕见，从带有选择的弹出窗口到成熟的代码模板。如果你已经用这种语言写了一百万行代码，这甚至会让你烦恼。然而，如果你只是偶尔使用它，这些会很有帮助。我使用 Unix 和 Linux 很多年了，但是我意识到还有人不是每天都在使用它。随着 Raspberry Pi、Linux 服务器和 Windows 10 有了 bash shell，使用 shell 的人比以往任何时候都多。你需要一点帮助吗？如果是这样，你可以试试 [`bashelp`](https://github.com/wd5gnr/bashelp) :这是我在写 bash 完成时整理的一点东西。

有好消息和坏消息。好消息是 Unix 有一个内置的帮助命令— `man` —并且已经有一段时间了。坏消息是你需要停止你正在输入的东西，输入一个`man`命令来使用它。`Man`，顺便说一句，是手工的简称。

[![](img/b66662ca0c11b044aedfed4ecf259b27.png)](https://hackaday.com/wp-content/uploads/2018/01/man.png)`man`(像左边的`yelp`)有 GUI 前端，你甚至可以本地或远程使用网络浏览器。然而，这些都与你输入的内容无关。你必须转到另一个窗口，输入你的搜索词，然后继续输入。这让我开始思考如何为 bash 获得一种上下文敏感的内联帮助。

与 tab 补全一样，创建帮助函数需要考虑两个部分:获取帮助的 shell 函数，以及告诉`readline`调用该函数的方法。`bashelp.sh`脚本提供了这两者。然而，它只有在`$DISPLAY`被设置时才起作用，表明你正在使用一个 GUI 终端。顺便说一句，Mac 的 GUI 并不是这样，所以如果你想让它在 Mac 上工作，你需要在几个地方做些改变。如果你做到了，并且让它工作了，我希望看到一个拉请求或者一个分叉。

该脚本允许您设置一个“帮助”角色。我选择了 Control+Y，bind 命令认为它是“\C-Y”。您会在脚本的顶部附近找到它，如果您愿意，您可以更改它。还有一些配置项，因此您可以在新的终端中运行`man`或者运行图形化的`man`替换。有关配置的详细信息，请参见[自述文件](https://github.com/wd5gnr/bashelp/blob/master/readme.md)。

[![](img/b7b8e5ca3d178f3f505550df60e16151.png)](https://hackaday.com/wp-content/uploads/2014/06/tux.png) 这个功能相当简单。没有 X 就 bails(再来看`$DISPLAY`)。它还期望$READLINE_LINE 和$READLINE_POINT 中来自`readline`的行数据。如果没有线，脚本退出。然后，该函数将该行的第一个单词作为一个空格，然后解析所有选项以启动正确的`man`查看器。

当然，这只是你可以通过颠覆`readline`来做的一件事。如果您使用 bash 或为 bash 编写脚本，这是一个非常方便的技巧。

如果您想要更多的 bash 定制，您总是可以挑选出一个[新提示](https://hackaday.com/2009/09/05/take-command-of-your-bash-prompt/)。如果你想让你的帮助脚本将焦点弹回你原来的窗口，或者在某些情况下关闭，你可能想仔细阅读一下[命令 GUI 窗口](https://hackaday.com/2017/09/21/linux-fu-x-command/)。