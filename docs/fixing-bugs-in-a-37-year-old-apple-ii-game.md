# 修复 37 年前苹果二代游戏中的错误

> 原文：<https://hackaday.com/2017/01/15/fixing-bugs-in-a-37-year-old-apple-ii-game/>

模拟器是回忆过去游戏和软件的好方法。[Jorj Bauer]发现自己早在 2002 年就这样做了，当时他们决定为 Apple II 启动三里岛。它玩得很好，但由于某种原因，立即崩溃，如果你碰巧按下' 7 '键。这是一个问题——游戏需要几个小时才能玩完，而“7”是保存和恢复进度的关键。2002 年，[Jorj]满足于忍受这些。但是最后，受够了——Jorj 着手彻底修复三里岛的漏洞。

该项目分为三个部分——Jorj 如何开始玩三里岛并首先了解苹果 IIs 的历史，游戏的问题，以及最后找到解决方案的方法。在第一次发现问题后，[Jorj]在网上搜索，看看是否只是一个坏的磁盘映像导致了这个问题。但是他们找到的每一份都是一样的。除了二进制中的问题之外，别无它法。

![title-screen](img/ab8ad4e45b52c0aef6d1754eea33d9f1.png)

The revised title screen, with bugfix noted.

这是一个拆解和挖掘几十年历史的扫描文献的故事。错误的关键是在一份 1980 年 6 月的 [Micro 6502 日志中找到的。如果你不想破坏这个故事，就到此为止——当有人将苹果 DOS 3.1 版本的游戏复制到苹果 DOS 3.3 磁盘时，问题就出现了。磁盘格式不是向后兼容的，所以 3.3 磁盘版本只能在 DOS 3.3 机器上播放。然而，游戏的代码在保存例程中使用了字节码，这些字节码引用了在 DOS 3.3 中发生了变化的 DOS 3.1 函数。正是通过搜索这个字节码，该杂志在谷歌上弹出了一个提示。文章提到了 DOS 版本之间字节码的变化，给了[Jorj]他所需要的解开谜团的线索。](https://www.scribd.com/document/76024617/Micro-6502-Journal-June-1980)

最后，要让游戏在 DOS 3.3 下正常运行，所需要做的就是修改代码，指向 DOS 3.3 的正确寄存器。完成这些后，点睛之笔是一个经过修改的标题屏幕，突出了[Jorj]的辛勤工作。该表扬就表扬。

好心的，[Jorj]已经[上传了固定的游戏供世人欣赏](http://jorj.org/techno/tmi-fixed.dsk.gz)(。gz 文件下载)！看到人们仍然使用和享受这些旧系统总是很棒。[苹果 IIGS 甚至在 29 岁的时候升级了操作系统。](http://hackaday.com/2015/07/16/29-year-old-apple-computer-finally-gets-an-os-update/)