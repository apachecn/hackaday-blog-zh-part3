# 需要汇编:子程序调用和 1K 挑战

> 原文：<https://hackaday.com/2016/12/07/assembly-required-subroutine-calls-and-the-1k-challenge/>

我个人拥有的第一台电脑有 256 字节的内存。字节。我的鼠标和键盘的处理器内存都比这个大。更多。诚然，256 字节有点极端，但即使是我当时作为工作的一部分构建的嵌入式系统，通常也只有 64K 字节内存的一小部分可以寻址。

有些人可能很高兴他们再也不用担心这样的事情了。我，有点怀念。试图从 EPROM 中多挤出 10 个字节来修复一个错误或增加一个新功能，这通常就像一个难题。我想随着 1K 挑战的进行，我可能会分享一些我们在那些日子里用来解决小内存问题的技巧。

## 我帮不了你…

不幸的是，这种级别的优化通常需要特定的解决方案，没有人能帮助你，除非他们确切地知道你在做什么。通常，节省内存的最佳方法包括改变算法或使用 CPU 特有的功能。例如，如果你存储了很多字符串，但不需要很多字符，也许你可以[打包你的字符串](https://hackaday.com/2016/11/22/squoze-your-data/)。在正确的 CPU 上，您可能要花两个字节来写:

```
MOV B,#0
```

这大概会清除假设的寄存器 B，并且通常需要两个字节的编码(一个字节用于 MOV，其位字段指示 B 寄存器，另一个字节用于文字零)。然而，如果可用，XOR 指令可能需要一个字节:

```
XOR B,B
```

这也将寄存器 B 置零，因为任何东西与其自身的异或都是零。如果可能的话，减法也可以做同样的事情。

不过，这些都是特定于您的项目和平台的。所以对于这类事情，你要靠自己。

## 但是，有些事情是普遍的

改变程序最简单的方法之一就是子程序。大多数 CPU 都有一些调用和返回的功能(虽然奇怪的是，我的 256 字节计算机没有)。第一条规则是使用它们。如果你有四到五条指令被重复，这是子程序的一个很好的选择。常识吧？但是还有一些涉及子程序的技巧要记住。

第一个想法是寻找可以移入子例程的项，即使它需要在代码中的某个地方做一点调整。为了说明这一点(以及其他一些想法)，我去了这个[在线汇编语言模拟器](https://schweigi.github.io/assembler-simulator/)。它有一个简单的汇编语言，类似于真正的 CPU。能够在 web 浏览器中单步调试代码的能力也很不错。当然，您必须将这些概念应用到您的特定 CPU 上。

下面是一个简单的程序，它读取一个表示十进制数的四字符 ASCII 字符串，并将其放入 16 位寄存器中。所以字符串“255”在寄存器中会变成 00FF。

```
; Simple example
; Convert decimal # at istring into 16-bits in B:C
   JMP start

start:
   CALL convert
; more interesting things happen here
   HLT
convert:
   MOV B,0
   MOV C,0  ; answer in B:C
   MOV D, istring    ; Point to var
   CALL decdig  ; convert each digit
   INC D
   CALL decdig
   INC D
   CALL decdig
   INC D
    CALL decdig
    RET

shift16:
   MOV A,0
   SHL C,1
   JNC shift16a
   INC A
shift16a:
   SHL B,1
   ADD B,A   ; output carry is meaningless
   RET

decdig:
   CALL shift16; *2
   PUSH B
   PUSH C
   CALL shift16; *4
   CALL shift16    ; *8
   POP A
   ADD C,A   ; 8X+2X=10X!
   JNC decdig0
   INC B

decdig0:
   POP A
   ADD B,A
   MOV A,[D]
   SUB A,'0'
   ADD C,A
   JNC xret
   INC B
xret:
   RET

istring: DB "1924" ; input
         DB 0 ; String terminator

end:
```

这汇编成 89 字节。不多，但我们可以做得更好。首先要注意的是 D 寄存器保存了字符串的地址。程序在开始时加载它，在每次调用数字转换子程序后，都有一个增量指向下一个字符。节省空间的一个显而易见的方法是将增量指令分解到子例程中。你可以把它放在末尾，或者——如果更有意义的话——加载地址减一(大多数汇编器在汇编时就能知道)。在这种情况下，这并不重要，但无论哪种方式都可以得到 85 字节。我将 POP D 指令放在 xret 标签之后，转换例程现在看起来像这样:

```
convert:
MOV B,0
MOV C,0 ; answer in B:C
MOV D, istring ; Point to var
CALL decdig ; convert each digit
CALL decdig
CALL decdig
CALL decdig
RET
```

注意最后两行。您可以通过将最后一个调用改为 JMP 来节省一个字节。decdig 结束时的返回将返回到最初的调用方。您可以通过重新排列代码来节省更多的空间，这样 decdig 就出现在那个位置:

```
CALL decdig
CALL decdig
CALL decdig
decdig: ...
```

你甚至可以更多地应用这一点。请注意，您对 decdig 进行了 4 次调用，这可以被视为两组调用。所以你可以写:

```
CALL decdig2
decdig2:
CALL decdig
decdig: ....
```

你可能需要考虑一下。第一个调用执行两个操作，返回到 decdig2，在那里再执行两个操作。最后，返回返回给最初的调用者。

## 可读性

我承认，这不太可读。评论是免费的，所以如果你不打算围绕代码写博客，你应该使用它们。特别是，任何时间代码都依赖于在特定的位置，您应该记录它:

```
CALL decdig2:
; **** FALL THROUGH
decdig2:
```

这可以防止您不小心移动它或插入代码并破坏东西。现在我们有 80 字节了。您可以用 shift16 子例程玩同样的把戏，但是因为它只被调用一次，所以在这种情况下没有真正的节省。

节省 9 个字节看起来不多，但大约是原代码的 10%。有时候这就是你所需要的。你也可以优化算法。

## 返回转换

在一些 CPU 上，你可以做条件返回(也就是说，像零或 RZ 返回)。但是在其他处理器上，只能对一个条件进行分支或跳转。这导致了这样的代码:

```
JNZ nextinst
RET
nextinst:
```

然而，您可能已经在代码中的某个地方有了一个返回(比如示例程序中的 xret 标签)。这意味着你可以写:

```
JZ xret
```

你又节省了一个字节。像便士一样，它们都是累加的。

## 轮到你了

你最喜欢的节省空间的招数是什么？在评论里分享吧，除非你想把它留作你参加 [1K 挑战](https://hackaday.io/contest/18215-the-1kb-challenge)的秘制酱。你必须在 1 月 5 日之前挤出这些额外的字节。