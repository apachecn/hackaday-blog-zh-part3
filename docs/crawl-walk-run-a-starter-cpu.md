# 爬行、行走、奔跑:启动 CPU

> 原文：<https://hackaday.com/2016/03/25/crawl-walk-run-a-starter-cpu/>

[上一次](http://hackaday.com/2016/03/16/crawl-walk-run-planning-your-first-cpu-design/)我谈到了在尝试处理更现代的架构之前，通过查看旧的设计来开始 CPU 设计。特别是，我推荐卡克斯顿·福斯特的蓝色，即使(或者可能因为)它是以示意图的形式。尽管原理图很容易理解，但 Blue 确实使用了一些过时的结构，您可能应该使用您选择的 VHDL 或 Verilog 来构建您的设计。

就我而言，我的选择是 Verilog。你可以在 Opencores.org 上找到我的[实现 Blue。我对福斯特的原始设计做了不少改动。例如，有了半导体存储器，我设法让所有指令在一个主周期(当然是 8 个次周期)内运行。我还更新了时钟生成，并添加了一些资源和指令。](http://opencores.org/project,blue)

## 说明

你可以在蓝色档案中找到我的整个指令集(在文件 blue-instructions.xls 中查找)。电子表格显示了助记符、操作码以及在八个子循环中的每一个中发生的操作。这里有一个例子:

[![bluei](img/848133c71cc32be4a4195f293aecc3c5.png)](https://hackaday.com/wp-content/uploads/2016/03/bluei1.png)

说到助记符，有一个用 Perl 写的简单汇编程序(用名为 asm 的 shell 脚本调用)。这本来是使用我的[通用汇编器](http://hackaday.com/2015/08/06/hacking-a-universal-assembler/)的好地方，但是我还没有写出来。

虽然看我版本的 Blue 很有用，但是你不应该跟得太紧。首先，我使用 Blue 作为我正在使用的工具的测试用例，所以有几个地方有替代代码，我在这些地方绘制了 Foster 的 gates，以查看工具如何处理它，而不是更多的间接构造。此外，你真正的目标应该是基于架构做自己的设计。尽管如此，当你陷入困境时，有一个工作实例可以参考并不总是一件坏事。

## 时钟生成

Top.v 中有蓝色的模块(不是最好的命名约定)。时钟发生器是 control.v 的一部分，如下所示:

```
reg [7:0] onehot;
reg wclks;
assign cp[1]=onehot[0] && (xrun|xdep|xexam);
assign cp[2]=onehot[1];
assign cp[3]=onehot[2];
assign cp[4]=onehot[3];
assign cp[5]=onehot[4];
assign cp[6]=onehot[5];
assign cp[7]=onehot[6];
assign cp[8]=onehot[7] && cycle;

always @(posedge clk or posedge reset) begin
  if (reset) onehot<=8'b1;
  else begin
    if (start || exam || deposit || abortcycle) onehot<=8'b10000000;
	 else if (xrun||xexam || xdep) onehot<={onehot[6:0], onehot[7]};
  end
 end

```

cp 信号是次要时钟周期。onehot 阵列是一个简单的移位寄存器，用于跟踪状态。其他位像开始，考试，和存款是我创建的自定义前面板的一部分(见下面的视频)。这不是福斯特最初设计的一部分，但它很好地利用了托管 CPU 的 [Digilent Spartan 3](http://store.digilentinc.com/spartan-3-board-retired/) 板。不幸的是，那块板已经退役了(不直接复制设计的另一个原因)。

如果你不想做前面板，我的版本 Blue 也有串口，我写了一个简单的 loader 读入一个更强大的监视器(见[上集](http://hackaday.com/2016/03/16/crawl-walk-run-planning-your-first-cpu-design/)的视频)。事实上，前面板在某些方面甚至比 CPU 更有趣。

演示板有四个 7 段显示器、几个 led、几个按钮和八个开关。这不足以处理 16 位处理器。我使用一个按钮来改变显示的含义，离散的 led 会提醒您显示处于哪种模式。在开关上输入一个字节会将前一个字节上移，这样您就可以在按下 enter 按钮之前输入 16 位。如果你犯了一个错误，你可以继续输入字节而不用按回车键。你可以在下面的视频中看到操作。

## 其他 CPU

还有其他的小型 CPU，有些比 Blue 更现代，还有许多具有更多功能。不过，我看到的一个问题是，一些非常小的 CPU 要么不够完整，不实用，要么很难理解。以 [J1](http://hackaday.com/2010/12/01/j1-a-small-fast-cpu-core-for-fpga/) 为例，只有 200 行左右的 Verilog。但这是一个不寻常的架构，可能不是最好的起点。 [MCPU](https://github.com/cpldcpu/MCPU) 是另一个非常小的处理器，甚至可以放入 CPLD。

不管你走哪条路，我认为你最好记住标题:爬，走，跑。先做好基础，然后再进行越来越复杂的设计。

 [https://www.youtube.com/embed/dt4zezZP8w8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dt4zezZP8w8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

