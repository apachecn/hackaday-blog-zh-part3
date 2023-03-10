# 这不是你父亲的 FORTRAN

> 原文：<https://hackaday.com/2015/10/26/this-is-not-your-fathers-fortran/>

1968 年春天，我作为一名水利工程技术人员学习了 FORTRAN IV 编程。其中一位工程师知道我对计算机感兴趣，问我是否愿意学习 FORTRAN。他需要计算溪流中的生物需氧量，但对编程没有任何兴趣。我抓住了这个机会。

那是大铁时代，计算机一词指的是一间装满空调设备的房间。纽约州立大学布法罗分校有一台 IBM 704，但他们很快升级到了 CDC 6400。为了帮助支付费用，他们邀请人们参加一个关于 FORTRAN 的研讨会，这样他们就可以使用这个系统。我的工作是在纽约州的一个小办公室，让我参加的批准出奇的容易。

我去参加了为期 6 周的训练，每周一个晚上。我仍然有我的黑色“Fortran IV 编程指南”，作者是丹尼尔·麦克拉肯(Daniel McCracken)。多年来，这是 FORTRAN 圣经，通常被称为“麦克拉肯”。

编程进行得很顺利，在某处有一篇非常旧的论文，引用了它生成的关于流经纽约詹姆斯敦的 Chadakoin 河的结果。

这就是 FORTRAN 的强项——科学计算。它的名字就说明了这一点:公式翻译。

# 起源和 FORTRAN IV

约翰·w·巴克斯向 IBM 建议用一种语言来代替汇编语言。IBM 704 的开发始于 1953 年，该项目于 1957 年取得成果。它不仅是第一种通用高级语言，击败了 COBOL 和 LISP，而且它的编译器优化了代码，因为它需要与汇编语言正面竞争。在这方面，它是当时的 C 编译器。

这不是它获得成功的唯一原因。将一个程序所需的穿孔卡数量比汇编时减少了 20 倍，帮助很大。

在那些日子里，你需要用一个键打孔机来制作一副穿孔卡片。要真正做到这一点，你必须知道如何创建一张编程卡，让你跳过 FORTRAN 卡上的字段，或者如何编辑一张卡片，方法是复制它，并在你键入新字符时按住其中一张卡片。由于我对电脑的迷恋，我在高中时上过一门键盘打孔和自动化机器的课程，所以一切都准备好了。

FORTRAN 卡以 5 个字符的字段开始。如果第一个字符是“C ”,那么它就是一张注释卡。否则字符要么是空白的，要么是行号。行号提供了 GOTOs 的目的地。

[![fortran card](img/35920cef743bbf80bbbd3caba1687917.png)](https://hackaday.com/wp-content/uploads/2015/10/fortran-card.jpg) 第六个字符可以是除“0”以外的任何字符，这意味着该卡是前一张卡的延续。一个好的做法是按顺序使用字符，这样你就可以知道连续的顺序。

第 7 列到第 72 列是程序语句。其余的，从 73 到 80，没有被编译器使用。这样做的目的是在这些卡片中加入序列号，这样当这副牌不可避免地掉落或者被读卡器吃掉时，你就可以重新将卡片按正确的顺序分类。一盒卡片包含 2000 张卡片，托盘约 5000 张。我见过程序员真的哭了，当一个卡片或托盘掉在没有排序的卡片上。我在布法罗的 SUNY 医院当操作员，操作 CDC 6400，加载跨越多个卡片托盘的程序和数据。

FORTRAN 的字符集是:

```

A .. Z 0 .. 9 = + - * / ( ) , . $

```

有趣的是，空格不是字符。他们完全被忽视了。名为 XYZ 的变量在这种形式下是有效的，如 X YZ 或 XY Z

变量名限于 6 个字符，并且必须以字母开头。作为第一个字母的字母 I-N 隐含地表示变量是一个整数。所有其他字母表示一个实数。这可以通过显式键入名称来覆盖:

```

INTEGER ABC, XYZ
REAL IMREAL
LOGICAL TRUE, FALSE

```

其他数据类型有复杂型、字符型和双精度型。

数组是用 DIMENSION 语句声明的:

```

DIMENSION XY(100), AB(2000, 3) 

```

数据初始化使用的数据:

```

DATA A, B, C, D, E, F /0, 1, 2, 5*3/

```

有趣的控制结构之一是算术 IF 语句。测试语句中的值是否大于、等于或小于零。根据结果，语句跳转到语句后面的三个行号之一:

```

IF (NONZERO) 100, 200, 300 

```

有一个 IF 语句测试结果为. TRUE，因为 FORTRAN 认为这是一个值。IF 语句不能嵌套。

只有一个循环语句 DO 可以嵌套:

```

DO 200 I = 0, 10, 3
C do some calculations, I starts at zero,
C increments by 3, and exits when it exceeds 10
C The next line is the end of the loop
200 CONTINUE

```

FORTRAN IV 确实有使用 CALL 语句进入并返回退出的子例程和函数。

以下是 FORTRAN IV 中允许的其他程序语句的列表:

```

EQUIVALENCE
GOTO, GOTO, ASSIGN, assigned GOTO
DO
FORMAT
READ, READ INPUT TAPE, WRITE, WRITE OUTPUT TAPE, PRINT, and PUNCH
READ TAPE, READ DRUM, WRITE TAPE, and WRITE DRUM
LOGICAL
END FILE
REWIND
BACKSPACE
PAUSE
STOP
FREQUENCY
END
COMMON

```

看看你能否破解这个计算三角形面积的 FORTRAN IV 程序。

```

C AREA OF A TRIANGLE - HERON'S FORMULA
C INPUT - CARD READER UNIT 5, INTEGER INPUT, ONE BLANK CARD FOR END-OF-DATA
C OUTPUT - LINE PRINTER UNIT 6, REAL OUTPUT
C INPUT ERROR DISPAY ERROR MESSAGE ON OUTPUT
 501 FORMAT(3I5)
 601 FORMAT(4H A= ,I5,5H B= ,I5,5H C= ,I5,8H AREA= ,F10.2,12HSQUARE UNITS)
 602 FORMAT(10HNORMAL END)
 603 FORMAT(23HINPUT ERROR, ZERO VALUE)
     INTEGER A,B,C
  10 READ(5,501) A,B,C
     IF(A.EQ.0 .AND. B.EQ.0 .AND. C.EQ.0) GO TO 50
     IF(A.EQ.0 .OR. B.EQ.0 .OR. C.EQ.0) GO TO 90
     S = (A + B + C) / 2.0
     AREA = SQRT( S * (S - A) * (S - B) * (S - C) )
     WRITE(6,601) A,B,C,AREA
     GO TO 10
  50 WRITE(6,602)
     STOP
  90 WRITE(6,603)
     STOP
     END

```

来自[https://en.wikibooks.org/wiki/Fortran/Fortran_examples](https://en.wikibooks.org/wiki/Fortran/Fortran_examples)的代码。

# 走向未来

尽管年代久远，Fortran(现在被称为 Fortran)仍继续存在，甚至可能在科学和工程计算方面取得成功。诚然，C++现在正在取得进展，但要成为计算之王，它还有很长的路要走。

Fortran 表现出色的一个原因是它收集了前几十年遗留下来的大量代码。你不会重写那些花了几十年才生产出来的、经过调试的、众所周知运行良好的代码。甚至开源社区也认识到了这一点，因为通常以 C 和 C++闻名的 GNU 编译器套件包括了一个现代的 Fortran 编译器。这并不奇怪，因为在编译的第一阶段完成后，机器码的生成对于所有套件的语言都是通用的。这些第一阶段是容易的部分。

该语言已经被标准委员会定期更新，包括 ANSI 标准组，一旦它成立。FORTRAN IV 于 1962 年问世。随后是 66 年、77 年、90 年、95 年、2003 年和 2008 年的更新。Fortran 2015 的工作目前正在进行中，将于 2018 年发布。

一路走来，它失去了固定的格式，变得像其他现代语言一样自由。它也丢失了行号。算术如果遇到了它的灭亡。

今天，这种语言拥有你所期望的大多数特性:do-while、递归、select-case(等价于 switch-case)、动态内存分配，甚至是面向对象的能力。

增加的一个功能是处理矩阵运算的能力。考虑到它在科学计算中的用途，这是明智的。然而，今天的 Fortran 越来越依赖于用 C/C++编写的库，以至于规范中包含了使用这些语言的兼容性指南。

# 它没死，吉姆

这种语言并没有消亡，尽管它没有出现在流行排行榜上。在 LinkedIn 上快速搜索发现，休斯顿有 9 份工作，美国各地还有很多工作要求懂 Fortran。大多数人还想要 C/C++，这反映了这三种语言是如何融合的。我想大多数使用 Fortran 的人不会用它来进行黑客攻击，所以 GitHub 不会看到很多上传，这似乎是受欢迎程度的主要衡量标准。

此外，Fortran 是一种利基语言，我指的是积极的意义。在使用 Fortran 的地方，它就是要使用的语言。那当然是高性能和科学计算。一些细节是天气预报、气候建模、计算物理、天文学、化学和经济学。它被投资公司用于金融建模。根据 Adam Fabio 的说法，基于 Fortran 的空气控制系统仍在使用。下次你坐飞机的时候想想这个。

Fortran 是推荐给你大学年龄的孩子或朋友的职业道路吗？大概不会。尽管他们可能需要学习它来从事上述领域的职业。它不太可能作为一种用于 Arduinos 的语言出现，但是你可以安装在 Raspberry Pi 上。

Fortran 仍然在做它最擅长的事情:处理数字。

这是一个承诺。我会写下第一个在举报热线上通知 Hackaday 他们创建了一个 Fortduino 的黑客。