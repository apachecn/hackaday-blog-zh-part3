# LiteBSD 为 PIC32 带来 4.4BSD

> 原文：<https://hackaday.com/2016/01/04/litebsd-brings-4-4bsd-to-pic32/>

几年前，[塞尔日·瓦库伦科]开始了 RetroBSD 项目——将旧的 2.11BSD 操作系统的 16 位端口移植到微芯片 PIC32 微控制器。这令人印象深刻，但是对大多数人来说，BSD 的第 2 版已经是旧闻了，与现代的 BSD 和 Linux 操作系统相比，有点难以使用。

[Serge]再次尝试，现在在 PIC32MZ 上运行 4.4 BSD-[lite BSD](https://github.com/sergev/LiteBSD/wiki)端口。根据[Alexandru Voica]的说法,[在基本版本中有大约 20 万的用户空间内存](http://blog.imgtec.com/mips-processors/can-it-run-bsd-the-story-of-a-mips-based-pic32-microcontroller),通过删除一些操作系统功能，您可以将这个数字增加一倍或两倍。

如果您不熟悉 BSD，它是 Berkeley Unix 的衍生物。与 Linux(它是 Unix 功能的重写)不同，BSD 派生了最初的 Unix 源代码并添加了一些特性。BSD 的第 4 版增加了几个关键特性，包括 TCP/IP 网络，LiteBSD 包括一个 IPV4 堆栈和一个以太网驱动程序(WiFi 驱动程序正在开发中)。你可以从下面的【Kirk McKusick】([BSD](https://en.wikipedia.org/wiki/Marshall_Kirk_McKusick)背后的主要人物之一)那里查看一个关于 BSD 历史的报告。

我们以前在 micros 上见过 [RetroBSD，但是由于 2.11BSD 的传统，RetroBSD 没有 LiteBSD 的潜力。有趣的是，驱动程序结构是兼容的，因此两个项目可以很容易地共享驱动程序源代码。](http://hackaday.com/2015/05/21/unix-on-your-breadboard/)[也许【雅罗米尔】会升级他的笔记本电脑](http://hackaday.com/2014/06/27/hacklet-5/)。

 [https://www.youtube.com/embed/ds77e3aO9nA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ds77e3aO9nA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示。PIC32 图表由微芯片提供。