# Linux Fu:文件别名、链接和映射

> 原文：<https://hackaday.com/2018/03/16/linux-fu-file-aliases-links-and-mappings/>

你听说过 Linux 里的一切都是文件吗？这在很大程度上是正确的，这就是为什么操作文件的能力对于掌握 Linux Fu 至关重要。

使 Linux 文件系统如此通用的一个原因是一个文件能够同时存在于许多地方。归结起来就是把文件保存在一个地方，但在另一个地方使用。这对于快速访问磁盘、修改正在运行的系统，或者仅仅是按照适合您的需要的方式来组织事物是很方便的。

有几个关键特性有助于实现这种多功能性:链接、绑定挂载和用户空间文件系统立即浮现在脑海中。让我们来看看这些是如何工作的，以及你将如何经常看到他们被使用。

## 链接

[![](img/5fa3ba698024ec07f64691f4e0ec7bcb.png)](https://hackaday.com/wp-content/uploads/2017/09/link.jpg) 有两种联系:硬性的和软性的(或象征性的)。硬链接仅适用于单个文件系统(即单个磁盘驱动器)，本质上是为现有文件创建别名:

```
ln /home/hackaday/foo /tmp/bar
```

如果发出这个命令，那么/home/hackaday/foo(原始文件)中的文件和/tmp/bar 文件将是相同的。不是复制品。如果你改变一个，另一个也会改变。这是有意义的，因为数据只有一个副本。您只需要两个相同的目录条目。注意参数的顺序就像复制命令一样。foo 文件是原始文件，您正在创建的新链接称为 bar。

这些并不是非常有用，因为它们要求文件在同一个文件系统中。它们也很难维护，因为内部发生的事情并不总是显而易见的。在 ls 命令中使用-l 选项(小写的 L)显示了特定文件的链接数量。通常，这是一个，虽然目录会有更多，因为每个..子目录中的引用将被视为链接以及实际条目(。)和父目录中的条目。如果您想找到所有相同的硬链接，您需要搜索文件系统(使用 find 并检查-samefile 选项)。

符号链接更有用，因为它们可以跨越文件系统。本质上，符号链接或符号链接只是一个包含另一个文件名称的文件。文件系统知道，当您使用该文件时，您实际上是指被引用的文件。要创建的命令是相同的，只是增加了一个选项:

```
ln -s /home/hackaday/foo /tmp/bar
```

一个完整的目录列表非常清楚地显示了符号链接。有几件事你必须注意。首先，您可以创建循环链接，即使工具试图检测并阻止它。换句话说，fileA 可能引用 fileB，而 fileB 又引用 fileC，fileC 又引用 fileA。Linux 最终会在一定数量的间接访问后停止，以防止这种情况发生。

另一个问题是目标文件可能不存在。例如，当您删除原始文件时，可能会发生这种情况。找到所有的符号链接需要搜索文件系统，就像硬链接一样，所以不容易找到这些断开的链接。

有什么好处？假设您有一个 PCB 路由器的工作目录。在该工作目录中有一个名为 scratch 的临时目录。您会注意到对暂存目录的磁盘 I/O 消耗了程序的大部分执行时间。您可以使用符号链接轻松地将暂存目录指向 RAM 磁盘或固态磁盘驱动器，以提高性能。

[![](img/c1c084d93deb0212538d5826c2cdfe8f.png)](https://hackaday.com/wp-content/uploads/2017/09/1024px-disk_pack.jpg)

Image Source: [Disk Pack](https://commons.wikimedia.org/wiki/File:Disk_Pack.jpg) by Steve Parker CC-BY 2.0

## 绑定安装

许多 Linux 文件系统支持绑定挂载的思想。这允许您在文件系统的其他地方挂载一个目录。这类似于对一个目录进行符号链接，但具体内容略有不同。首先，挂载是暂时的，而符号链接就像它所在的文件系统一样是永久的。另一方面，挂载点可以在不破坏现有目录的情况下替换它(包括使用 chroot 命令成为新的根目录)。

事实上，chroot 可能是绑定挂载最常用的。您想为一个系统(可能是一个远程系统)准备一个新的根目录，而您仍然在旧的根目录下引导。伪造东西的一个简单方法是将挂载“特殊”文件系统(如/dev 和/proc)绑定到新的根目录，然后 chroot 运行 grub 之类的东西。

对于 Linux，通常使用 mount 命令创建绑定挂载:

```
mount -o bind /dev /home/hackaday/bootimage/dev
```

这个命令将/dev 复制到 bootimage 目录中。

BSD 提供了一个可以完成同样事情的 nullfs。还有一个名为 bindfs 的用户文件系统也可以完成类似的任务。

除了构建假的根文件系统，您还可以使用绑定挂载来揭示隐藏在常规挂载后面的目录。例如，假设您想为/tmp 目录创建一个 RAM 驱动器:

```
mount -t tmpfs -o size=512M tmpfs /tmp
```

任何在/tmp 中的东西现在都被隐藏了。但是，请考虑以下命令:

```
mount -o bind /tmp /oldtmp
```

现在/oldtmp 将在 RAM 驱动器挂载之前拥有/tmp 的内容。

如果你想复习一般的装裱，看看下面的视频。它谈到了常规挂载和循环挂载(用于挂载文件，如 ISO 文件，而不是设备)。

 [https://www.youtube.com/embed/A8ITr5ZpzvA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/A8ITr5ZpzvA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 用户空间文件系统

历史上，添加文件系统意味着编写内核代码(通常是内核模块)。然而，使用用户空间中的文件系统——称为 FUSE——任何人都可以编写看起来像文件系统的代码。事实上，如果您想在不直接使用绑定挂载的情况下构建沙盒，请查看 [sandboxfs](https://github.com/bazelbuild/sandboxfs/) 。

有许多用户文件系统来处理各种任务。有些对文件做了特殊的处理，比如将归档文件作为目录挂载。其他人将其他类型的数据作为文件公开(例如，远程网站上的博客文章)。有些文件系统可以标记真实文件，动态转换文件类型，甚至在空间耗尽时删除旧文件。我发现 [sshfs](https://github.com/libfuse/sshfs) 特别有用，因为它可以挂载一个远程目录，而无需远程端的特殊软件。

编写自己的 FUSE 模块相当简单。外面有几个好的教程。如果你使用 C++，你可以得到一个[非常简单的实现](https://github.com/thawkins/fuse-examplefs)。如果你有兴趣看看 Python 是如何工作的，请看下面的视频。

 [https://www.youtube.com/embed/DpvdOuTzOU0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DpvdOuTzOU0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 包裹

在传统的基于 Unix 的系统中，一切都是文件。不管是好是坏，这种哲学已经不像过去那样普遍了。尽管如此，文件和类似文件的东西仍然是 Linux 的重要组成部分，知道如何操作链接、挂载目录和使用 FUSE 文件系统对于管理和设置从 PC 到 Raspberry Pi 的任何基于 Linux 的系统都有很大的帮助。