# Git Shell 旁路，少即是多

> 原文：<https://hackaday.com/2017/05/10/git-shell-bypass-less-is-more/>

我们一直是战争游戏的粉丝。不是电影(嗯，也是电影)，但我指的是黑客战争游戏。有几种格式，但通常你可以在某处访问一个初始 shell 帐户，这是 0 级，你必须利用系统中的一些缺陷来获得 1 级权限等等。几乎总是有一个层次，你必须利用一个合法的二进制文件(有一些可疑的许可)，它做的比普通用户想的更多。

在 [CVE-2017-8386 的情况下，`less`更多。](https://insinuator.net/2017/05/git-shell-bypass-by-abusing-less-cve-2017-8386/)

[Timo Schmid]详细介绍了如何滥用`git-shell`(一种受限制的 shell，旨在通过 ssh 隧道在 git 远程会话中用作上游对等体)来实现任意文件读取、目录列表和某种程度上受限制的文件写入。`git-shell`的基本思想是将 ssh 会话中允许的命令限制为 git 所需的命令(git-receive-pack、git-upload-pack、git-upload-archive)。研究人员意识到他可以向这些命令传递参数，比如 flag–help:

```
$ ssh git@remoteserver &quot;git-receive-pack '--help'&quot;

GIT-RECEIVE-PACK(1)            Git Manual             GIT-RECEIVE-PACK(1)

NAME
 git-receive-pack - Receive what is pushed into the repository
[...]
```

该标志的作用是让 git 命令打开 git 的手册页，该手册页被传递给一个分页程序，通常是`less`。这就是有趣地方。如果以交互方式运行,`less`命令，它可以做一些你期望的事情，比如搜索文本、转到行号、向下滚动等等。它还可以打开一个新文件(:e)，保存输入到一个文件(s)并执行命令(！).要使它交互运行，您必须在`ssh`中强制分配一个 PTY，如下所示:

```
$ ssh -t git@remoteserver &quot;git-receive-pack '--help'&quot;

GIT-RECEIVE-PACK(1) Git Manual GIT-RECEIVE-PACK(1)

NAME
 git-receive-pack - Receive what is pushed into the repository

 Manual page git-receive-pack(1) line 1 (press h for help or q to quit)

```

按 h 求助，玩得开心。一个警告是，通常的安装代码执行不会真正执行任意命令，因为当前运行的登录 shell 是`git-shell`，仅限于一些白名单中的命令。然而，在某些配置中可能会发生这种情况，比如将`bash`或`sh`作为登录 shell，并限制用户只能使用`git`(比如在没有 root 访问权限的共享环境中)。你可以在这里看到[这样的例子](https://asciinema.org/a/90lfyhow2rxrnikrl2i6sdhk1)。

最快的解决方案似乎是在`sshd`配置中启用`no-pty`标志服务器端。这阻止了客户端请求 PTY，因此`less`不会在交互模式下运行。

```
$ man less

LESS(1) General Commands Manual LESS(1)

NAME
less - opposite of more

```

很讽刺，不是吗？