# 给 Linux 一个远程引导

> 原文：<https://hackaday.com/2017/02/14/giving-linux-the-remote-boot/>

很多嵌入式系统在 Raspberry Pi 这样的平台上运行 Linux。由于 Linux 可以从命令行完全运行，并且完全支持网络，因此可以运行您从未实际接触过的服务器。

不过，还是有一些问题。有时候你真的需要重启机器。你还需要在控制台前做一些事情，比如完全安装一个新的操作系统。还是你？在 GitHub 上，用户[marcan]有一个 C 程序和一个 shell 脚本，它允许你[接管一个正在运行的系统](https://github.com/marcan/takeover.sh)，而不需要在根文件系统上使用任何软件。它启动一个 ssh 服务器，你可以远程卸载主驱动器，做任何你想做的维护工作，并且——大概——重启到一个新的操作系统。

关键是创建一个临时文件系统(位于 RAM0 中)并将一个系统救援 CD 复制到其中。系统还必须使用 systemv 风格的 init，这样命令“telinit u”就会导致 init 重新运行。init 进程是引导装载程序真正执行的程序，并且总是有 PID 1。

然而，使用[marcan 的]脚本，文件系统被打乱，由接管脚本动态构建的脚本替换 init。因此，当 init 重新运行它自己时，它实际上执行了最终在包含的 fakeinit 中运行的脚本，它只是坐在那里等待。

通常，Linux 引导过程只是工作，您可能不知道它在进行什么。但如果你确实知道，你可以像这样耍花招。例如，Raspbian 派生自 Debian，因此您可以通过查看 [Debian 文档](https://www.debian.org/doc/manuals/debian-reference/ch03.en.html)来了解更多关于引导过程的信息。

当然，如果您的发行版已经切换到 systemd，您将不得不尝试不同的策略(不久前我们发布了一篇关于 Linux 内核的帖子，引发了许多关于 systemd 之战的评论)。理解 Linux 引导系统是 Linux 魔法的一个支柱。了解更多关于内核和[系统调用](https://hackaday.com/2016/06/14/linux-assembly-required/)是另外两个。