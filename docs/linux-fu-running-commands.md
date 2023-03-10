# Linux-Fu:运行命令

> 原文：<https://hackaday.com/2017/07/07/linux-fu-running-commands/>

使 Linux 和类 Unix 系统既强大又令人沮丧的一个原因是，有许多方法可以实现任何特定的目标。举一个简单的例子，比如按顺序运行一串命令。显而易见的方法是编写一个 shell 脚本，它提供了极大的灵活性。但是如果您只想运行一些命令集呢？这听起来很简单，但是有很多种方法可以发出一系列命令，从直接输入到调度，再到像大型计算机监控批处理作业那样监控它们。

让我们来看看从 bash(和许多其他 Linux shells)执行序列的几种方法。这包括了`cron`和`at`命令以及一个叫做任务假脱机程序的批处理系统。像 Linux 中的大多数东西一样，这甚至不是一个完整的列表，但是它应该给你一些控制执行序列的方法。

## 从壳里

最简单但可能最不令人满意的运行一堆命令的方法是直接从 bash shell 中运行。只需在命令之间放置分号:

```
date ; df ; free
```

这适用于许多看起来或多或少像 bash 的 shells。对于这样一组简单的命令来说，这很好。每一个都按顺序运行。然而，如果你有这个呢:

![Bad example of bash code. We've made this an image to prevent copy/paste.](img/21c12182c6def77cfe04c513c2fe0d39.png)

你想删除 foo 中的所有文件(但不是子目录；为此你需要-r)。但是如果`cd`失败了呢？然后你会删除你所在目录中的所有文件。这是个坏主意，违反了最小惊讶定律。

解决方法是使用&&运算符。就像在 C 中一样，这是一个`AND`操作符。几乎所有的 Linux 程序都返回 0 错误状态为真，其他的为假。允许程序员返回一个失败的错误代码，它就变成了 false。所以考虑一下这个:

```
cd /foo && ls   # not rm so we don't do anything bad by mistake
```

如果/foo 存在，`cd`命令将返回为真的 0。这意味着`AND`的结果可能为真，因此用`ls`继续执行。但是，如果`cd`失败，结果将为假。如果一个`AND`函数的任何输入为假，其他值就无关紧要了。因此，只要有任何东西返回 false，整个过程就会停止。所以如果没有/foo，`ls`命令根本不会执行。

您可以使用多组这样的运算符，例如:

![Bad example of bash code. We've made this an image to prevent copy/paste.](img/7d93934ac6ddfb7465e406c3d8ec1838.png)

还有一个`OR`操作符(`||`)，一旦返回 true，它就会退出。例如:

```
grep "alw" /etc/passwd || echo No such user
```

[![](img/9533b44f2bc54af3c7e6143e912d27f6.png)](https://hackaday.com/wp-content/uploads/2017/06/term.png) 试试你的用户 ID 而不是 alw，然后再试试一个不好的(肯定你没有叫 alw 的用户)。如果`grep`成功，回声不会发生。如果你愿意，你甚至可以混合操作符。如果您有许多需要长时间运行的命令，这可能不是最佳答案。在这种情况下，请看下面的假脱机。

您可能知道可以通过按 Control+Z 将正在运行的命令推到后台。在那里，您可以使用`fg`(移到前台)、`bg`(在后台运行)和`kill`命令来操纵它。所有这些技术也适用于链式命令。

## 时机

有时，您希望在预定的时间间隔或特定时间运行命令。管理定时执行的经典方法是`cron`。许多发行版提供了预定义的目录，这些目录每小时、每分钟等等运行一些东西。然而，最好的方法是简单地编辑您的 crontab。通常，您会创建一个脚本，然后在 crontab 中使用该脚本，尽管这并不总是必要的。

crontab 是一个必须用`crontab`命令编辑的文件(执行`crontab -e`)。不是注释的每一行都指定了要运行的程序。该行的第一部分告诉您何时运行，最后一部分告诉您运行什么。例如，这里有一个运行 [duckdns](http://duckdns.org) 更新程序的条目:

```
*/5 * * * * ~/duckdns/duck.sh >/dev/null 2>&1
```

这些字段指定分钟、小时、月中的日、月和星期几。`*/5`表示每 5 分钟一次，其他`*`表示任意一次。你可以使用很多特殊的语法，但是如果你想要一些简单的东西，试试这个在线的 [crontab 编辑器](https://crontab.guru)(见图)。

[![](img/d67c8f33c728196048514fee0def5a71.png)](https://hackaday.com/wp-content/uploads/2017/06/cron.png)

cron 的一个问题是，它假设您的计算机全天候运行。如果您将作业设置为在夜间运行，而计算机在夜间关闭，则该作业不会运行。Anacron 试图解决这个问题。虽然它像 chron 一样工作(有局限性)，但如果计算机在应该运行的时候关闭了，它会“赶上”的。

有时候，你只想在特定的时间运行一次。您可以使用 at 命令来实现这一点:

```
at now + 10 minutes
```

您将看到一个简单的提示，在这里您可以发出命令。这些命令将在 10 分钟内运行。当然，您也可以指定绝对时间。你也可以把下午 4 点称为“下午茶时间”(说真的)。如果您改变主意，`atq`命令将显示待执行的命令，而`atrm`命令将取消待执行的命令。如果您使用命令的批处理形式，当系统有空闲时间时，系统将执行您的命令。

如果您阅读 at 的手册页，您会看到默认情况下，它使用“a”队列处理普通作业，使用“b”队列处理批处理作业。但是，您可以分配队列 a-z 和 A-Z，每个队列都有一个较低的优先级(从技术上讲，一个较高的 nice 值)。

一个重要的注意事项:在大多数系统上，所有这些排队的进程都将在系统默认 shell(如/bin/sh)上运行，而不一定是 bash。您可能希望在默认 shell 下显式启动 bash 或测试您的命令，以确保它们能够工作。如果您只是启动一个将 bash 命名为解释器的脚本(例如，`#!/usr/bin/bash`)，那么您不会注意到这一点。

## 假脱机

虽然`at`命令有批处理别名，但它不是一个完整的批处理系统。然而，有几个用于 Linux 的批处理系统具有不同的属性。一个有趣的选择是 Task Spooler(Ubuntu 仓库中的 task-spooler)。在一些系统上，这个命令是`ts`，但是因为这在 Debian 上有冲突，所以您将使用`tsp`来代替。

这个想法是使用`tsp`后跟一个命令行。返回值是一个任务编号，您可以使用该任务编号来建立任务之间的依赖关系。这在功能上与`at`相似，但功率大得多。想想这个抄本:

```
alw@enterprise:~$ tsp wget http://www.hackaday.com
0
alw@enterprise:~$ tsp
ID State Output E-Level Times(r/u/s) Command [run=0/1]
0 finished /tmp/ts-out.TpAPIV 0 0.22/0.00/0.00 wget http://www.hackaday.com
alw@enterprise:~$ tsp -i 0
Exit status: died with exit code 0
Command: wget http://www.hackaday.com
Slots required: 1
Enqueue time: Fri Jun 9 21:07:53 2017
Start time: Fri Jun 9 21:07:53 2017
End time: Fri Jun 9 21:07:53 2017
Time run: 0.223674s
alw@enterprise:~$ tsp -c 0
--2017-06-09 21:07:53-- http://www.hackaday.com/
Resolving www.hackaday.com (www.hackaday.com)... 192.0.79.32, 192.0.79.33
Connecting to www.hackaday.com (www.hackaday.com)|192.0.79.32|:80... connected.
HTTP request sent, awaiting response... 301 Moved Permanently
Location: http://hackaday.com/ [following]
--2017-06-09 21:07:53-- http://hackaday.com/
Resolving hackaday.com (hackaday.com)... 192.0.79.33, 192.0.79.32
Reusing existing connection to www.hackaday.com:80.
HTTP request sent, awaiting response... 200 OK
Length: unspecified 
Saving to: ‘index.html’

0K .......... .......... .......... .......... .......... 1.12M
 50K .......... .......... .......... ... 6.17M=0.05s

2017-06-09 21:07:53 (1.68 MB/s) - ‘index.html’ saved [85720]
```

第一个命令将`wget`程序作为任务启动(实际上是任务 0)。运行`tsp`显示队列中的所有作业(在这种情况下，只有一个作业，它就完成了)。-i 选项显示关于指定任务的信息，而-c 转储输出。把-c 看作是一个`cat`选项，把-t 看作是一个`tail -f`选项。您还可以使用-m 选项通过邮件发送输出。

通常，任务假脱机程序一次运行一个任务，但是您可以使用-S 选项增加这个限制。您可以使用-d 选项让一个任务等待前一个任务。您还可以使用-w 让一个任务等待另一个任意任务。

如果你看一下[手册页](http://manpages.ubuntu.com/manpages/xenial/man1/tsp.1.html)，你会发现还有很多其他选项。请记住，在您的系统上，ts 程序可能是 tsp(反之亦然)。你也可以在[项目的主页](http://vicerveza.homeunix.net/~viric/soft/ts/article_linux_com.html)上找到例子。看看下面的视频，了解任务假脱机系统的一些常见用法。

像 Linux 中的大多数东西一样，您可以组合许多这些技术。例如，可以让 cron 启动一个假脱机任务。该任务可以使用脚本，这些脚本使用`&&`和`||`操作符来控制内部工作方式。过度杀戮？也许吧。就像我之前说的，你可以硬着头皮写个剧本。然而，如果您选择使用其中的任何一个或全部，已经有很多功能可用了。

 [https://www.youtube.com/embed/wv8D8wT20ZY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wv8D8wT20ZY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

