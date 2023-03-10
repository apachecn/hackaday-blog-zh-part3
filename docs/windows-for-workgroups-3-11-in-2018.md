# 2018 年面向工作组的 windows 3.11

> 原文：<https://hackaday.com/2018/05/15/windows-for-workgroups-3-11-in-2018/>

距离微软发布 Windows for Workgroups 3.11 已经过去了 25 年。为了回到 16 位操作系统时代的末期，[Yeo Kheng Meng]让 WFW 3.11 在现代 Thinkpad 上运行。

让事情变得困难的是，这个项目设定了几个目标。显然，这在虚拟机中没什么意思，所以这些被禁止了。需要一个视频驱动程序，因为 WFW 3.11 在软件中只支持高达 640×480 的分辨率。对声音的一些基本支持将是可取的。最后，TCP/IP 网络在 WFW 3.11 中是可能的，因此网络硬件将允许访问现代互联网。

[Yeo Kheng Meng]在 2009 年的 Thinkpad T400 上完成了所有这些目标，并全面记录了整个过程。需要一些有趣的技巧，包括基于 [Covox 语音东西](https://en.wikipedia.org/wiki/Covox_Speech_Thing)的定制并行端口声卡的设计。访问 HTTPS 的 web 服务器需要一个中间人攻击来剥离 SSL，因为 WFW 3.11 上的 SSL 支持是古老的，并且被今天的大多数 web 服务器所阻止。

如果你想要一台自己的 WFW 3.11 笔记本电脑，详细的说明会让你如愿以偿。[Yeo Kheng Meng]还提供了声卡的硬件设计。休息之后你可以看一个关于这个过程的报告。

 [https://www.youtube.com/embed/pqicQYPeS-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pqicQYPeS-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

