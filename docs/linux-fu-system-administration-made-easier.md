# Linux Fu:系统管理变得更容易

> 原文：<https://hackaday.com/2017/11/09/linux-fu-system-administration-made-easier/>

Linux 可能有点人格分裂。如果你把它作为桌面操作系统使用，它有很多 GUI 工具，尽管有时候你仍然需要访问命令行。但是，如果您将它用作一个无头服务器，您可能应该非常了解命令行。如果您不想让 X 服务器和图形用户界面的其他特性弄脏您的硬盘(和 CPU ),这一点尤其正确。

就我个人而言，我喜欢命令行，但我很现实，知道不是每个人都有这种感觉。我也承认对于一些任务——尤其是那些你不常做的任务——有一些有用的按钮和菜单是很好的。有几个管理工具，您可能有兴趣用来处理 Linux 机器上的管理任务。我将介绍其中两种，您可能想尝试一下，它们都使用 Web 浏览器来提供界面。

为什么是两个？首先，在 Linux 传统中，做任何特定的事情都有不止一种方法。除此之外——这也是 Linux 的传统——每种工具都有其优缺点。Webmin 工具有大量的插件来管理很多很多不同的东西。然而，驾驶舱更现代，假设它支持你所需要的，可能更有用。

## 放弃

哦，顺便说一下。是的，有一些人认为这样的工具是令人厌恶的。我觉得这取决于你的目标。如果你正在为一个大公司管理一个高度安全的服务器，也许这些工具不应该是你的第一站。正如我提到的，我不介意命令行，但我使用 Webmin 只是因为它提供了 Usermin，让我可以向在我的机器上拥有帐户的朋友提供 GUI，这样他们就可以执行与其帐户相关的基本管理任务。我发现驾驶舱的系统监控很好，即使我没有用这个系统做太多的改变。

即使您喜欢使用这样的工具，您也应该真正熟悉命令行，至少对于常见的任务。不过，有个有趣的花絮。至少在某种程度上，这两个工具都允许您在浏览器中启动命令行。

## Webmin

Webmin 可能不会赢得任何用户界面奖项。它实际上是一系列具有公共用户界面和共享一些基础设施的 Perl 模块。好消息是，Webmin 有一个开放的接口，并且已经存在了足够长的时间，如果你想管理一些模糊的软件，有一个 Webmin 模块是一个公平的赌注。您也可以禁用任何不想要的模块。

[![](img/624dd986ec57662257c158333f0f2c32.png)](https://hackaday.com/wp-content/uploads/2017/10/webmin.png)

正如我提到的，您还可以设置 Usermin，它允许普通用户通过 GUI 做事情。当然，你可以控制他们能做什么，不能做什么。

尽管有点笨拙，但您可以发布命令，甚至使用一个奇怪的基于 Web 浏览器的终端。有一些东西需要 Java，而这在现代 Web 浏览器中越来越难找到。然而，大多数都有替代方案(例如，有一个 HTML 文件管理器和一个基于 Java 的文件管理器)。

根据您使用的发行版，您可以使用您的包管理器来安装 Webmin。在树莓 Pi 上安装 [Webmin 也有大量教程。你总能在](http://www.instructables.com/id/Adding-Webmin-to-manage-a-Raspberry-Pi/)[项目的网站](http://www.webmin.com/)上找到官方版本。

 [https://www.youtube.com/embed/xfJCGf2ks5I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xfJCGf2ks5I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 战场

驾驶舱来自 RedHat，当然是看起来更现代的工具。它有图表，非常灵敏。然而，你可以为 Webmin 得到的插件范围并不多。然而，如果你使用的是 [Docker](https://hackaday.com/2016/09/01/how-to-use-docker-to-cross-compile-for-raspberry-pi-and-more/) ，Cockpit 在管理容器方面有很好的集成。

正如您在下面看到的，您可以连接到一台机器，然后让它连接到其他机器并同时监控它们。图中显示了两个框，但是您可以添加更多的框。

[![](img/a9314d12bf2047cf908b7497b90a279f.png)](https://hackaday.com/wp-content/uploads/2017/10/pit1.png)

一旦深入到一个特定的框中，您就有了许多管理和监控选项，包括在浏览器中访问一个 shell。

[![](img/765bef264b58fccbcbf8a0c5a6526fd4.png)](https://hackaday.com/wp-content/uploads/2017/10/pit2.png)

有驾驶舱的[臂后端口可用，所以根据你运行 Pi 的分布，你应该可以很容易地让它运行。](https://github.com/cockpit-project/cockpit/issues/6560)

 [https://www.youtube.com/embed/IFO3mR2VB5U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IFO3mR2VB5U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 小费

为了充分利用 Cockpit，您需要以 root 用户身份登录。但是，现在很多系统根本没有 root 密码。当你登录时，你可以要求驾驶舱在必要时使用你的密码来提升权限。如果您不选中该框，那么某些操作(特别是添加新服务器)将会失败。

这在某种程度上否定了使用 sudo 的想法。整个想法是迫使你不时地重新认证。如果你让 Cockpit 向 sudo 提供你的密码，你实际上并没有给你自己那种保护。我的想法是，如果你不勾选这个框，Cockpit 应该像 sudo 一样提示你输入密码。然而，当添加新服务器时——至少——它不会。只是失败了。

解决方法是在您登录时选中该框，让它重复使用您的密码。请注意，这使得使用 sudo 进行特权访问变得毫无意义。

## 安全性

[![](img/ebc429f0a4405a97f5e484c071acde9b.png)](https://hackaday.com/wp-content/uploads/2017/10/padlock-2035052_640.png) 说到安全。这两个工具都包含自己的 SSL 服务器和自签名证书。大概，您知道您正在连接到您的机器，所以自签名部分不会打扰您—您只需要加密。然而，这确实意味着浏览器会给你一个关于证书不被信任的可怕警告。

当然，你可以更换证书。[让我们加密](https://hackaday.com/2016/03/20/anti-hack-free-automated-ssl-certificates/)是一个免费的“真实”证书的好来源。

然而，向外界开放这些接口是相当可怕的。毕竟，如果有人得到了它，他们可以做任何事情。您应该考虑更改端口号，使用双因素身份验证(两个工具都支持 [Google Authenticator](https://hackaday.com/2016/09/30/lock-up-your-raspberry-pi-with-help-from-google/) )，如果可能的话，让工具只监听您的网络，并使用 VPN 或 SSH 隧道来访问它。

## 最后

个人？我一直在等待整个 WIMP(窗口/图标/鼠标/指针)时尚消失，让我们按照自然的意图在命令行上工作。然而，这似乎不会发生，直到世界末日之后。说真的，对于一些晦涩难懂的任务，拥有一些菜单项和对话框会有很大的帮助。如果你不做太多的管理工作，这些工具可以成为很好的训练工具。就像我前面说过的，如果您的用户不熟悉 Linux，Usermin 特别有用。

此外，不管你喜不喜欢，Linux 关乎选择。我喜欢 KDE，但我很高兴想使用 Cinnamon 或其他桌面环境的人有这个选择。就此而言，当我在小型机器上运行时，有时我也很高兴有其他选择。