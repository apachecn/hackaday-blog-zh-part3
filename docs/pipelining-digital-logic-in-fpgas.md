# FPGAs 中的流水线数字逻辑

> 原文：<https://hackaday.com/2018/06/05/pipelining-digital-logic-in-fpgas/>

当你第一次学习数字逻辑时，它可能看起来很容易。你学习了与门和或门，发现这并不难。然而，从几个基本的门到像 CPU 或另一个复杂系统是一个完全不同的故事。就像从“你好，世界！”编写一个操作系统。在你做出这个飞跃之前，有很多东西需要理解。在这组文章中，我想讨论一种利用流水线技术组织更复杂的 FPGA 设计的方法，比如 CPU。

如今，复杂的数字逻辑系统很可能位于 FPGA 上。我们之所以会误以为数字很简单，部分原因是因为现代 FPGA 工具。他们对你隐藏了很多复杂性，这很好，直到他们不能做到你想要的，然后你就卡住了。一个很好的例子就是你试图达到某个时钟频率。如果不小心，工具会抱怨您不能满足时间约束。

发生这种情况有许多可能的原因，但最常见的可能是您试图在每个时钟周期做太多事情。虽然我们倾向于认为我们的电路是完美的，但事实并非如此。逻辑门速度很快——非常非常快——但它们并不是无限快。在更大的芯片上，甚至信号从芯片的一部分到达另一部分的时间也变得很长。

现代工具有很好的模型来预测每件事情在最坏的情况下需要多长时间，并通过找出事情不可靠的情况来帮助你。考虑这个电路:

![](img/fedb13e990d629303ce49fe492a2d197.png)

云表示一系列组合逻辑，如 AND 和 OR。甚至可以是一个查找表，这不重要。如果从盒子的输入到输出的延迟短于时钟脉冲，一切正常。但是，如果在时钟脉冲再次出现之前，右侧触发器 D 输入端的信号仍在传输中，就会出现不良行为。事实上，事情要比这复杂一点。信号实际上必须比时钟快触发器的建立时间，并在保持时间内保持稳定，这两件事软件都知道。在之前，我们已经[深入讨论过这个问题。但是就本文的目的而言，关键思想是我们的逻辑“云”的传输延迟必须短于时钟定时。](https://hackaday.com/2015/09/23/learn-flip-flops-with-simulation/)

比方说，您希望获得 100 MHz 的时钟，但工具告诉您无法实现。你的逻辑太慢了。你能做什么？一个答案是流水线。

## 逻辑交通堵塞

我经常想，在这种情况下，一个更好的管道术语应该是水桶大队。想法是每个时钟周期做一点工作，然后交给芯片的另一部分。你可以看到 CPU 一直在这样做。例如，典型的 8 位微芯片 PIC CPU 每四个时钟周期执行一条指令。但是一些 PIC 克隆产品(如老的 Ubicom SX)可以在每个时钟周期执行一条指令，时钟速度通常更快。

考虑一个假设的 CPU。它分四步执行指令:

1.  获取指令
2.  获取参数
3.  进行操作
4.  写入结果

我掩盖了一些事情，但对于许多 CPU 来说，这实际上非常接近准确。你有两个选择。你可以尝试在一个时钟周期内做所有的事情，但那将是一场噩梦。假设您正在执行第 2 步，其中一个参数是累加器，它需要 33 皮秒才能到达执行第 3 步操作的逻辑。但是寄存器参数需要 95 皮秒。那么执行逻辑需要一些时间。你什么时候做第 4 步？

处理这个问题的唯一方法是计算出第四步中的答案正确所需的绝对最长时间，并将你的时钟速度限制在这个范围内。不会很快。

更常见的方法是在一个时钟周期内完成一个步骤。然后在下一个时钟周期做下一步。这有效地将时钟除以 4，因为每个指令现在需要四个时钟周期，而不是一个。

你可以设置一个从 0 到 3 的计数器，这样你就知道你正在处理的是哪一部分。或者，你可以使用[一个一键方案](https://hackaday.com/2016/03/25/crawl-walk-run-a-starter-cpu/)，其中每个状态都有自己的触发器。然后，CPU 做它必须做的事情，只有那部分逻辑必须在时钟再次敲响之前完成。真的，这是和以前一样的问题，除了每次滴答的总时间更少，你必须保持你的时钟比最慢的部分慢。在某些情况下，非常慢的部分(如步骤 1)可能会引入等待状态，以便您在该步骤中停留更长时间，但您不会像过去那样看到内存更慢、动态 RAM 刷新周期更长的情况。

这很有效，是一种常见的做事方式。大概就是 PIC 里面发生的事情。但是如果你想一想，如果所有的步骤都需要相同数量的逻辑，那么 3/4 的设备在大多数时间里什么都不做。当步骤 2 发生时，其他步骤的所有逻辑基本上都处于空闲状态。

## 管道

这就是流水线的用武之地。想象一下，如果我们在每一步之间放置触发器，而不是激活四个步骤之一的计数器。考虑执行四条指令:A、B、C 和 CPU 资源如下所示:

[![](img/99b49aea750e6af324f59ef3b06391a2.png)](https://hackaday.com/wp-content/uploads/2018/05/test.gif)

看怎么像斗旅？每个部分做好自己的工作，然后移交给下一个部分。这使得所有的部分都可以一直工作。

总的想法是将逻辑分成独立的块。然后在所有输出端放置触发器。这使得每个部分在每个时钟周期产生一个结果，然后触发器为下一个块保存该结果。据推测，组块的速度明显快于整体处理。如果第三步的逻辑有 95%的时间延迟，你不会从这种技术中得到太多帮助。

具体如何做到这一点将取决于您想要什么，以及您希望如何在每个步骤中构建您的逻辑。下一次我将展示一个例子，其中每一步都需要一个时钟周期。然而，可以让块中的处理使用较高的时钟频率，然后为流水线使用较慢的时钟使能信号。在这种情况下，只有在时钟使能有效时，单步输出才会改变。

所有这些都假设每个阶段也需要同样长的时间。在某些情况下，您将在管道中添加“什么都不做”的阶段，以处理一个步骤需要多个时钟周期的情况。当然，无操作阶段先于慢速阶段。另一种方法是在各级之间放置一个 FIFO 缓冲器，这通常是设计环境中的现成模块。

您还可以设计每个阶段，以便它在有下一阶段的有效数据时发出信号。在复杂的情况下，您甚至可以像串行端口一样进行阶段握手。步骤 2 可以发信号通知步骤 1 它准备好接收更多数据，而步骤 1 可以发信号通知数据何时有效。如果你想让你的流水线超级复杂，这也可以结合 FIFO 缓冲器。

您可能还能设计出更多的方法，但原理是一样的。缓冲和握手的问题是，它进一步增加了逻辑复杂度，从而降低了速度并消耗了 FPGA 资源。您必须权衡额外复杂性的成本和收益。

## 没有免费的午餐

回到简单的流水线，现在我们每个时钟周期得到一条指令，处理块变小了，所以我们可以轻松拥有更快的时钟。这可能看起来像是不劳而获——嗯，反正是很少——但事实并非如此。如果你善于观察，你会注意到，虽然我们每个时钟获得一条指令，但从开始执行到指令 A 完成也有很大的延迟。当然，由于时钟更快，延迟实际上与非固定时钟速度差不多。

还有其他一些问题。显然，你增加了复杂性。对于 CPU 来说，还有其他被称为危险的问题。对危险的完整讨论必须从一些 CPU 设计基础开始，这超出了本文的范围，但是考虑一下:如果指令 B 的步骤 2 必须读取指令 A 编写的内容，那将如何工作？指令 A 还没有进行到第 4 步。在某些情况下，解决方案是停止管道。在其他情况下，有一种方法可以在早期从管道中窃取结果。

你可能知道的另一个复杂性是填充管道。在所有现代处理器中，进行条件分支是有代价的。比如，你想做一个零指令跳转。但是在你获取它之后，你在哪里获取下一条指令呢？如果你抓取下一条指令，有可能会发生跳转，而那条指令不会执行。如果你抓住跳转引用的那个，你仍然会有错的时候。不同的设计师做不同的事情。有些人试图预测分支。其他人只是挑选一个策略(通常得到下一个指令)并坚持下去。通常提供跳过指令，因为 CPU 可以使一条指令而不是整个流水线无效(当然，除非跳过的指令是跳转)。

您还必须确保在跳转时，跳转时在管道中间的任何指令不仅被丢弃，而且在转储之前对机器的状态没有影响。用 CPU 设计的行话来说，指令不会提交，直到你确定它真的被执行了。

我用过很多 CPU 的例子，因为它们很常见。但是这些问题是真实的，即使你做的不是传统的 CPU。你必须确保管道中充满了正确的指令，并且在你需要的时候数据是可用的。

## 下一站:工作示例

所有这些在理论上都很棒，但是一个实际的例子怎么样？我将使用 Verilog，它具有模拟电路延迟的强大功能。下一次，我将解释它是如何工作的，并向您展示一个在 FPGA 内部“计算”一个值并使用流水线技术使其更快的实际例子。您可以使用您选择的任何 Verilog 模拟器来玩这个例子，但是我将使用 [EDAPlayground](https://hackaday.com/2015/07/21/learn-fpgas-in-your-browser/) 。它非常适合运行小型测试或演示，并在浏览器中为您提供了广泛的工具。

顺便说一下，非流水线 CPU 的一个很好的例子是[蓝](https://hackaday.com/2016/03/16/crawl-walk-run-planning-your-first-cpu-design/)，我之前讲过。时钟发生器使用一键方案来产生 8 个时钟使能，控制指令执行的哪一部分正在进行。芯片每个时钟执行一部分，因此时钟速度基本上是时钟输入频率的 1/8。

下次见！