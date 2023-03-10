# 笨拙的文本文件

> 原文：<https://hackaday.com/2016/06/21/gawking-text-files/>

工具箱中的一些工具是多功能的。例如，你可以用螺丝刀作为撬棒来打开油漆罐。我甚至用螺丝刀把钉子敲了进去，尽管你可能不应该这么做。但是电锯并不是万能的。它只会切割。但人类确实能做到！

[![auk](img/ca5e5fecf9dcb9a2ef79b5fe412920ce.png) ](https://hackaday.com/wp-content/uploads/2016/06/auk.jpg) AWK 是一个用于逐行处理文本文件的电锯(而 GNU 版本被称为 GAWK)。这是很常见的情况。如果您从电子表格中生成一个文本文件或者处理其他类型的文本文件，这种情况会更常见。AWK 有一些严重的局限性，但电锯也是如此。它们还是超级有用的。虽然 AWK 听起来像企鹅一样的鸟(见右)，那是一只海雀。听起来一样，但是拼写不同。AWK 实际上是原作者名字的首字母缩写。

如果你懂 C 语言，并且会搜索正则表达式，那么你可以在 5 分钟内学会 AWK。如果你只知道 C，去[读完](http://www.regular-expressions.info/tutorial.html)[上的](http://gskinner.com/RegExr/)正则表达式再回来。五分钟后你就会知道 AWK 了。如果您运行的是 Linux，您可能已经安装了 GAWK，并且可以使用别名 AWK 运行它。如果你运行的是 Windows，你可能会考虑安装 [Cygwin](http://www.cygwin.com) ，尽管有[纯 Windows 版本](http://gnuwin32.sourceforge.net/packages/gawk/htm)可用。如果你只是想在浏览器里玩，试试 [webawk](http://crashcourse.housegordon.org/webawk) 。

## AWK 处理循环

每个 AWK 程序都内置了一个不可见的 main()。在准 C 代码中，它看起来像这样:

```
int main(int argc, char *argv[]) {
   process(BEGIN);
   for (i=1;i<argc;i++) {
      FILENAME=argv[i];
      for each line in FILENAME {
         process(line);
      }
   }
   process(END);
}

```

换句话说，AWK 从命令行读取每个文件，并处理它从命令行读取的每一行。一行是以`RS`变量中的任何内容结尾的一串字符(通常是换行符；`RS`=记录分隔符)。在它开始之前和完成之后，它为`BEGIN`和`END`做处理(不完全是你马上会看到的线)。

## 线路处理

有什么大不了的，对吧？诀窍在于生产线的处理。AWK 是这样做的:

*   它将整行放入一个名为`$0`的特殊变量中
*   它将该行分割成字段`$1`、`$2`、`$3`等。
*   变量`FS`设置用于拆分的正则表达式。缺省值是任何空格，但是你可以设置为逗号，逗号和空格，甚至是空行。
*   变量`NF`获取当前行的字段数。
*   该文件的行号在`FNR`中，总的行号在`NR`中。

现在，AWK 脚本负责处理这个过程。注释以`#`字符开始，所以忽略那些。他们走到队伍的尽头。第 1 列中的任何内容(大括号除外)都是匹配的。把它想成一个隐含的 if 语句。如果表达式为真，则执行与之关联的代码。当处理还没有开始时,`BEGIN`表达式为真，而`END`用于在其他事情都完成后进行处理。如果没有条件，代码总是执行。
举例:

```
BEGIN { # brace has to be on this line!
   count=0
}
    { 
    count++
    }
END {
    print count “ “ NR
    }

```

如果能让你感觉更好，你可以像在 C 语言中那样使用分号。也可以用括号(像`print(…)`)。这个例子是什么意思？嗯，在开始设置时`count=0`(变量是根据你的需要组成的，开始时是空的，这意味着我们并不真的需要它，因为如果像数字一样使用空变量，它将为零)。没有类型。一切都是字符串，但需要时也可以是数字。
中间设置的大括号无论如何都匹配每一行。它将计数增加 1。最后，我们打印应该匹配的计数变量和`NR`。当你在 AWK 写两个相邻的字符串(或字符串变量)时，它们会变成一个字符串。所以这实际上只是打印一个由`count`、一个空格和`NR`组成的字符串。

## 一些实际的东西

这里有一些更有趣的东西:

```
BEGIN { # brace has to be on this line!
  count=0
  }
count==10 {
   print “The first word on line 10 is “ $1
}
```

这将打印第 10 行输入的第一个单词(`$1`)。顺便说一下，如果你没有给出任何要打印的参数，它会打印`$0`。总的来说，这仍然不太令人兴奋。也许用`$1==”Title:”`之类的作为条件会更令人兴奋。但是真正的强大之处在于，你可以使用正则表达式作为条件。例如:

```
/[tT]itle:/ {
```

这一行将匹配任何包含 title:或 Title:的输入行。

```
/^[ \t]*[tT]itle:/ {
```

这将匹配相同的，但只有在一行的开头，前面有 0 个或更多的空白。
您也可以匹配字段:

```
$2 ~ /[mM]icrosoft/ # match Microsoft
$2 !~ /Linux[0-9]/ # must NOT match Linux0 Linux1 Linux2 etc.

```

## 功能

AWK 在代码中也有正则表达式的函数，如`sub`、`match`、`gsub`(参见[手册](http://www.gnu.org/software/gawk/manual/gawk.html#String-Functions))。您也可以定义自己的函数。所以:

```
/dog/ {
   gsub(/dog/,”cat”) # works on $0 by default
   print # print $0 by default
   next
}
{
   print
}

```

这会将包含 dog 的行转换为 cat(包括将 dogma 转换为 catma)。next 关键字让 AWK 停止处理这一行，转到输入文件的下一行。你可以通过省略第一次打印和下一次打印来缩短这个脚本。然后最后一个打印将完成所有的打印。

## 关联数组

关于 AWK 的另一个超级有用的事情是，它有一个隐藏在数组中的小数据库。这些是关联数组，就像带有字符串索引的 C 数组一样。下面是一个计算一个单词在文本中出现的次数的脚本:

```
  {
  for (i=1;i<=NF;i++) {
    gsub(/[-,.;:!@#$%^&*()+=]/,"",$i) # get rid of most punctuation
    word[$i]=word[$i]+1
     }
   }

END {
   for (w in word) {
     print w "-" word[w]
    }
}

```

别忘了你也可以使用数字，所以`foo[4]`也是一个数组。然而，你也可以混合搭配，即使你可能不应该这样做。也就是说`foo[4]=10`和`foo[“Hello”]=9`都是合法的，现在数组有两个元素，`4`和`“Hello”`！

另外注意:`$i`和`i`是两回事！在上述 for 循环的第一遍中，`i`等于`1`，`$i`是第一个字段的内容(因为`i`是`1`)。你经常会看到`$NF`被使用，比如。这不是字段的数量。它是最后一个字段的内容。`NF`是场数。
您可以使用以下命令运行该脚本:

```
awk –f word.awk
```

或者，如果您在一个类似 Unix 的系统上，您可以用“#！/bin/awk–f "并使其可执行。

## 黑客使用

你可以用 AWK 做很多其他的事情。您可以从文件中读取行，读取命令行变量，使用 shell 程序来过滤输入和输出，更改输出格式，等等。大部分 C 函数都可以(甚至`printf`)。你可以在线阅读[整个手册，你会发现](http://www.gnu.org/software/gawk/manual/gawk.html)[例子](http://www.linuxfocus.org/English/September1999/article103.html)无处不在。

你可能想知道为什么硬件黑客需要 AWK。下一次，我将向您展示一些实际应用，包括处理日志数据、读取 Intel hex 文件，甚至编译语言。同时，也许你想用[纵横字谜来学习正则表达式](https://hackaday.com/2016/01/31/crosswords-help-you-learn-regular-expressions/)。

图片来源:[迈克尔·哈弗坎普] CC BY-SA 3.0