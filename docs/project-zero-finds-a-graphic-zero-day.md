# 零项目找到一个图形零日

> 原文：<https://hackaday.com/2017/02/20/project-zero-finds-a-graphic-zero-day/>

在发现臭名昭著的 Heartbleed 漏洞以及其他各种零日之后，谷歌决定组建一个全职团队，专门寻找类似的漏洞。这个被称为 Project Zero 的团队刚刚发布了一个新的漏洞，这个漏洞特别生动，由 Windows Nvidia 驱动程序中的一组缺陷组成。

发现的大多数漏洞是由于糟糕的编程技术造成的。从盲目写入用户提供的指针，到不正确的边界检查，大多数漏洞都是由 Nvidia 快速修复的简单错误造成的。正如作者所说，Nvidia 的“驱动程序包含了很多可能不应该出现在内核中的代码，而且发现的大多数错误都是非常基本的错误。”

当我们的老鼠都不安全的时候，一个安全的系统似乎是不可实现的。然而，隧道的尽头有光明。虽然发现的漏洞表明 Nvidia 还有很多工作要做，但他们对谷歌的回应是“迅速和积极的”大多数 bug 都在截止日期前被[很好地修复了，谷歌报告称 Nvidia 已经自己发现了一些 bug。Nvidia 似乎也在为了安全而重新构建他们的内核驱动程序。这不是](http://nvidia.custhelp.com/app/answers/detail/a_id/4278/~/security-bulletin%3A-multiple-vulnerabilities-in-the-nvidia-windows-gpu-display)[第一次听到谷歌的 Project Zero](http://hackaday.com/tag/project-zero/) 的消息，老实说，这可能也不会是最后一次。