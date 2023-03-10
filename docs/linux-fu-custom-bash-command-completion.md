# Linux Fu:定制 Bash 命令完成

> 原文：<https://hackaday.com/2018/01/19/linux-fu-custom-bash-command-completion/>

如果您不是 Linux 用户，并且您看到有人知道他们在使用 Bash——流行的命令行解释器——做什么，您可能会得到他们打字比实际速度快得多的印象。这是因为有经验的 Linux 用户知道，按 tab 键会完成他们正在键入的内容，所以您可以只键入几个字符，然后得到一行更长的文本。这个功能非常智能，所以你可能没有意识到，但它知道你可以输入什么。例如，如果您尝试解压缩一个文件，它知道预期的文件名可能有. zip 扩展名。

[![](img/29ecb8e84c6e619d56dbfab73728136c.png)](https://hackaday.com/wp-content/uploads/2018/01/tab.png) 怎么会这样？起初，你可能会想，“谁在乎它是如何发生的？”问题是当你写一个 shell 脚本或者一个运行在 Linux 上的程序时，完成变得很笨拙。必须有人让 Bash 在每个命令行程序上变得聪明，如果你是作者，那么这个人就是你。

## 命令完成的剖析

原来完成依赖于一个叫做`readline`的特定 GNU 库。它为许多不同的程序读取文本，包括 Bash，您可以使用主目录中的`.inputrc`文件来配置它。比如，这是我的`.inputrc`:

```
"\e[A": history-search-backward
"\e[B": history-search-forward
$if Bash
Space: magic-space
$endif
set match-hidden-files off
set completion-ignore-case on
set visible-stats on
set show-all-if-ambiguous on
```

这看起来不太像，但是在`/etc/inputrc`有一个系统范围的配置，这要实际得多。您还可以发出某些命令来动态修改配置。例如，Bash 内置的“`bind`”可以进行设置，还可以显示一长串已经设置好的内容。如果您执行此命令:

```
bind -p
```

您将看到一长串输出。有趣的是下面几行:

```
"\C-i": complete
"\e\e": complete
"\e!": complete-command
"\e/": complete-filename
"\e@": complete-hostname
"\e{": complete-into-braces
"\e~": complete-username
"\e$": complete-variable
```

[![](img/079fded64f2ee12e3ce0d9d97ddb0009.png)](https://hackaday.com/wp-content/uploads/2018/01/bash1.png)

您的可能会有所不同，但本质上这意味着当 tab 键或双 escape 出现时，执行一个完成操作。也有一些以转义开始的特殊完成。

## 但是它是如何工作的呢？

有三个内置的 shell 命令协作管理完成。它们是:

*   `complete`–配置完成
*   `compgen`–生成可能的完成
*   `compopt`–修改完成选项

我不会深入所有可能的选项，尽管如果你好奇的话，你可以阅读一下 [Bash 手册](https://www.gnu.org/software/bash/manual/html_node/Programmable-Completion-Builtins.html)。就我们的目的而言，您只需要几个，而且所有三个命令都采用相同的参数。

让我们尝试用`compgen`做一些事情，因为 bash 最终调用它来获得完成。假设您在命令行输入`ls`并按 tab 键。Bash 将进行以下调用:

```
compgen -c ls
```

您将看到所有以`ls`开头的命令的一堆输出(取决于您安装了什么)，例如`ls`本身、`lsusb`、`lspci`等。你也可以使用更现代的“`-A command`”语法来得到同样的结果。 [![](img/07e0c54dff653319300de22efbbf4602.png)](https://hackaday.com/wp-content/uploads/2018/01/bash2.png)

试试这个:

```
compgen -d /e
```

同样，如果你愿意，你可以使用`-A directory`。显然，这会输出目录。这很好，但是 Bash 如何知道将哪些选项传递给`compgen`？这就是`complete`命令的用武之地。`complete`命令可以告诉 Bash 调用 shell 函数或命令来响应某个命令的完成。它还可以为空命令或没有匹配规则的命令设置一个规则。对于常见情况，也有很好的快捷方式。

考虑一个叫做`burnhex`的脚本。如果您键入`burnhex`、一个空格和一个制表符，Bash(通过`readline`)将为您提供当前目录中的所有文件。但是，您可以猜测您只想要以`.hex`结尾的文件。你可以用`complete`轻松做到这一点:

```
complete -G "*.hex" burnhex
```

现在只有以`.hex`结尾的文件才会显示。

为了查看更复杂的完成，让我们从一个简单的 shell 函数开始。按照惯例，它们以下划线开头，尽管这不是技术要求:

```
function _hackaday {
   COMPREPLY=( "hackaday.com" "hackaday.io" )
   return 0
}
```

这告诉系统我们有两个完成。让我们假设我们有一个名为“`gohackaday`”的脚本或程序，我们希望这是它的完成(这个命令不一定要存在才能工作):

```
complete -F _hackaday gohackaday
```

现在如果你输入:

```
gohackaday<SPACE><TAB>
```

你会看到你的行动完成。系统足够聪明，知道它可以填写“黑客日”。部分，因为两种选择都是从那开始的。如果你输入一个“c”或“I ”,然后再按 tab 键，它会自动选择正确的选项。

顺便说一下，这个函数有三个我们没有用到的参数。第一个参数($1)是活动命令的名称，第二个是正在完成的单词，第三个是当前单词之前的单词。例如，考虑下面的行和后面的三个参数:

```
ls -l /foo
$1=ls
$2=/foo
$3=-l
```

如果您想要提取整行或确定用户如何调用补全，还可以设置几个环境变量。对于简单的情况，你可能不需要这些。

[![](img/3cf50a119054cc3a9876268c0a4e5a6f.png)](https://hackaday.com/wp-content/uploads/2017/02/tuxwiz.png) 当然，这是一个简单的例子。对于超出函数处理能力的事情，您也可以使用`-C`而不是`-F`来运行一个完整的命令。命令获得相同的参数和大部分相同的环境变量。

除此之外，还记得`compgen`的`-c`和`-d`选项吗？他们也在这里工作。因此，如果您有一个名为 foobar 的命令，它需要一个目录名作为参数，您可以说:

```
complete -d foobar
```

您甚至可以在函数或命令中调用`compgen`来直接生成数据，或者在代码中进行进一步的过滤和扩充。这可能会变得相当复杂，如果你看看一些内置的，你就会明白我的意思。

一般来说，很多完成脚本都位于/etc/bash_completion.d 或/usr/share/bash-completions 中。是的，其中一个是下划线，一个是破折号。Linux 的乐趣之一是每个系统都有一点点不同。

## 一个更典型的例子

考虑一下`ftp`命令。您可以通过键入以下命令来查找完成的内容:

```
complete -p | grep ftp
```

结果将会是这样的:

```
complete -F _known_hosts ftp
```

这意味着有一个名为`_known_hosts`的 shell 函数。如果您想看看它是什么样子，请尝试:

```
declare -f _known_hosts
```

您应该会看到类似这样的内容:

```
_known_hosts () 
{ 
 local cur prev words cword;
 _init_completion -n : || return;
 local options;
 [[ "$1" == -a || "$2" == -a ]] && options=-a;
 [[ "$1" == -c || "$2" == -c ]] && options+=" -c";
 _known_hosts_real $options -- "$cur"
}
```

显然，真正的工作正在`_known_hosts_real`中进行，你可以用同样的方式转储它。它很复杂，但你可以猜到它会转储计算机知道的主机名。还有其他类似`_init_completion`的辅助函数。重点不在于它们是如何工作的，而在于它们的存在，你可以像使用`ftp`完成设置一样使用它们。

[![](img/0cabdcaf240b9497e6c21ec2f94b815c.png)](https://hackaday.com/wp-content/uploads/2018/01/bash-icon.png) 这只是一个快速的概述。如果你想要所有血淋淋的细节， [Bash 手册](https://www.gnu.org/software/bash/manual/html_node/Programmable-Completion.html#Programmable-Completion)是有帮助的。在[Bash Completion](https://github.com/scop/bash-completion)project GitHub 页面也可以找到很多有用的文档。顺便说一下，Bash 不是镇上唯一的游戏。如果对您来说这还不够，Zsh 有一个非常强大的(不同的)完成机制。

一旦您理解了 Bash 如何读取命令行，您就可以玩很多有趣的把戏了。下次给你看我最喜欢的。在那之前，我希望这能帮助你少打字，多做事。