# 愚蠢的饭桶把戏

> 原文：<https://hackaday.com/2017/05/23/stupid-git-tricks/>

如果你说的是标准英语，我很抱歉，因为这个头衔对你来说可能和我想的完全不同。其实我说的是 Git，版本控制系统。上次我讲了这个程序是如何产生的，并给了你们一些指导。如果你是一个彻头彻尾的软件开发人员，你可能不需要被说服就可以使用 Git。但是即使你不是，你也可以用 Git 做很多不符合常规的事情。

## 跟踪文档

[![](img/decd35bc6df99e71da8f9c3b7017a480.png) ](https://hackaday.com/wp-content/uploads/2017/04/diagram.jpg) Git 真的很擅长跟踪文档的变化。如果你写的是纯文本文件、Markdown 或 TeX 文件，那你就是在做生意。但是，如果您使用 Word、OpenOffice 或许多其他文字处理程序，有一个技巧可以使用。好处是，你甚至可以使用不同的程序与他人协作。

在这篇文章和[这篇文章](https://github.com/vigente/gerardus/wiki/Integrate-git-diffs-with-word-docx-files)中描述的诀窍是配置 Git 使用一个名为 Pandoc 的程序将你的输入文件转换成 Markdown。Git 程序可以存储这两者，您可以向它解释 Markdown 文件中的差异对应于文档文件中的差异。

Pandoc 是一个值得了解的工具。它可以在多种令人眼花缭乱的格式之间转换。如果你想让自己头疼，你可以从他们的网站上展开图形，并尝试追踪所有的线条。

我们已经看到这种事情在合作教科书中发挥作用，甚至用于跟踪频繁变化的文件，如追溯到拿破仑时代的法国法典。

## 在网站上工作

您可以轻松地将跟踪文档的想法扩展到跟踪网站的 HTML 页面。你可以在创建时使用它，然后像平常一样上传文件。您也可以使用专门的[工作流程](http://www.mattboldt.com/using-git-for-websites/)。即使你是网站的唯一创建者，能够倒回网站上周或上个月的样子通常是意想不到的有用。

## 管理您的 Bash 配置文件或/等

如果您使用 Linux，您有许多配置您的环境的文件。像你的`.bashrc`、`.emacs`之类的东西，如果使用多台机器，很难保持一致。当然，你可以`rsync`他们，但如果他们曾经搞砸了，可能很难回去弄清楚发生了什么。这就是为什么我用 Git 写了一个[管理这个问题的系统。一旦它被配置好，你的机器将自动获取你推送到远程主机的任何更改(我把我的保存在 GitLab 上)。该系统足够灵活，允许对每台机器进行定制配置，甚至只需一点设置就可以让随机文件保持同步。](https://github.com/wd5gnr/bashrc)

有一个类似的名为 [etckeeper](https://etckeeper.branchable.com/) 的包，用于跟踪你在`/etc`目录中的系统配置。你可能会说配置文件本质上只是代码，但目的不是编码，而是保持版本控制和机器之间的同步。此外，在 etckeeper 的情况下，有一些修改，所以 Git 将存储一些对该应用程序很重要的元数据。

 [https://www.youtube.com/embed/MDLBeedl-1c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MDLBeedl-1c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## Git 作为数据库或 Bug 跟踪器

如果你使用 Git 进行开发，那么你也可以用它来跟踪 bug。事实上，您可以将 Git 用作一个简单的[数据库](https://www.kenneth-truyers.net/2016/10/13/git-nosql-database/)。不要期望运行 SQL 查询——这只是显示了一个名称-值对系统(众所周知的 NoSQL 数据库)。

当然，您可以在 Git 中存储 SQLite 数据库(或其他任何东西)。如果你这样做了，你可以[玩一些技巧](https://ongardie.net/blog/sqlite-in-git/)比如 Pandoc 的技巧来帮助 Git 更好地理解你的数据库。

## 推特(是的，推特)

曾经想要一个分布式 Twitter 实现吗？检查一下[马多克斯](https://github.com/technoweenie/madrox)。我们真的不知道为什么我们想要这个，但是我们想要。

## 基于文本的幻灯片显示

你曾经想要像幻灯片一样显示一系列的文本屏幕吗？也许不是，但是如果你做了， [Git 也可以做那件事](https://github.com/gelisam/git-slides)。不过，它需要 vim 的一点帮助。

[![](img/aa7d78109b40703103ff7446d81bd991.png)](https://hackaday.com/wp-content/uploads/2017/04/demo.gif)

## 所以…

即使您从来不需要这些技巧，一些用来诱使 Git 做一些不寻常的事情的方法可能会激发您去想别的事情。一个显而易见的想法是为 Gerbers 或一些其他印刷电路板文件格式的差异程序。能够看到 PC 板的几个版本之间的变化将非常有用。显然，能够追踪图表也会很有用。香料模特应该没什么问题。

有什么有用的 Git 技巧吗？请在评论中留下链接。