# Linux Fu:计数器旋转键！

> 原文：<https://hackaday.com/2018/06/01/linux-fu-counter-rotate-keys/>

如果你使用过现代 Linux 系统——包括 Raspberry Pi 的大多数变体——你可能知道 sudo。这通常允许授权用户提升自己的超级用户身份来做事情。

但是，有一个问题。如果您拥有 sudo 访问权限，那么您可以做任何事情——至少是 sudoers 文件允许您做的任何事情。但是极其关键的操作呢？我们都看过这样的电影，发射核导弹需要两个同时反向旋转的键和第三个发射键。对于 Linux 系统有没有对等的东西？

它并不完全是一个反转键，但是 Square 的预发布开源项目 [sudo_pair](https://github.com/square/sudo_pair) 给了你类似的东西。这个项目是 sudo 的一个插件，允许你让另一个用户授权一个 sudo 请求。他们不仅授权，而且可以看到发生了什么，如果有不好的事情发生，甚至可以中止它。

实际上，sudo 比大多数人想象的要复杂一些。如果你阅读了 sudo 手册，你可以授权某些用户或组拥有非常具体的访问权限，如果你知道如何设置的话。你只是不常看到有人这么做。例如，您可以允许某个特定的程序作为任何用户(或用户子集)的根用户运行，而不授予对所有内容的访问权限。这意味着 sudo-pair 不必用于完全根访问。您可以使用它来监控特定关键应用程序的使用情况。

要准确理解发生了什么，最简单的方法是观看下面的演示，其中显示了两个用户的屏幕。一个申请 sudo，另一个批准了(点击查看完整尺寸)。

[![](img/49431309d2906f7d3656187344f3a107.png)](https://hackaday.com/wp-content/uploads/2018/05/demo.gif)

该系统非常灵活，但是因为它是预发行版，所以有几个步骤来设置它，您可以在项目的自述文件中遵循。脚本会进行检查，以确保您没有试图批准自己的会话，并且可以进行其他自定义处理。这导致了一个先有鸡还是先有蛋的问题。你需要保护这个脚本，但是人们需要能够运行它。系统允许您的会话在没有配对的情况下执行脚本。还有其他方法可以免除某些事情。例如，随叫随到的管理员组可以被免除。注意 root 总是被豁免的，但是你真的不应该让很多人拥有完全的 root 权限，如果你处理的事情敏感到需要这样的话。

代码生锈了，还没有预构建任何东西。如果有多个用户管理重要的东西，这是一个非常有用的特性，但是对于生产环境来说，这还为时过早。特别是，正如该项目警告的那样，错误配置 sudo 会将您锁在机器之外，所以要小心行事，当然，您还有备份。对吗？

如果您正在运行一些关键的东西，那么您真的需要理解 sudo，并使用或不使用 sudo-pair 来配置它。可以在用户和组级别限制操作，实际上任何人都不应该拥有完全的 root 访问权限。即使你是你的 Raspberry Pi 上的唯一用户，如果它正在控制一些关键的东西，你应该迫使黑客至少破解多个密码才能通过。你甚至可以考虑[多因素认证](https://hackaday.com/2016/09/30/lock-up-your-raspberry-pi-with-help-from-google/)。奇怪的是，你甚至可以用一个 [Arduino](https://hackaday.com/2013/09/14/using-google-authenticator-with-an-arduino/) 来玩这个把戏。