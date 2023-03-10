# 一台旧的 68000 单板机又是新的了

> 原文：<https://hackaday.com/2017/02/27/an-old-68000-sbc-is-new-again/>

[杰夫·特兰特]已经完成了许多逆向计算项目。但是他想解决一些更实质性的问题。因此，他着手建造一台基于 68000 的单板计算机，名为 TS2，这是他在一本教科书中找到的。他在[的一系列博客文章](https://jefftranter.blogspot.ca/2017/02/building-68000-single-board-computer_26.html)(根据我们的统计，大约有 30 篇文章)和一个视频中对此进行了记录，你可以在下面看到。

68000 在当时有一个非常合理的架构。与其他类似的处理器相比，扁平的内存空间令人耳目一新，异步总线也使硬件设计更加容易。虽然那个时代的大多数 CPU 都认为总线设备可以在固定的时间内完成它们的服务，但 68000 使用与设备的握手来允许它们获得所需的时间。大多数其他 CPU 必须为慢速设备提供一种机制来停止总线，这很复杂，而且在许多情况下效率较低。

[Jeff]使用带有自动布线器的 KiCAD 来布置一些 PCB，他的所有文件都可以在 [GitHub](https://github.com/jefftranter/68000/tree/master/TS2/v2) 上找到。[Jeff]实际上是他的第二个版本，并且用更容易获得的替换物替换了一些难以找到的部分。帖子中的细节令人印象深刻，TS2 让人回想起无法将整个系统集成在一个 IC 封装中的时代。

你在这里听不到，但是很多 68000 带着一些影响非常特殊指令的缺陷逃到了野外。例如，如果你有一个，试着做一个长的快速加法(ADDQ。l)到任何间接地址寄存器。它可能工作，但有一个合理的机会，CPU 将神秘地挂起。那时候，也没有固件升级。

我们已经在[试验板上](https://hackaday.com/2014/11/08/breadboarding-a-68000-computer-in-under-a-week/)看到了 68000 个。我们甚至看到了由[和 Arduino](https://hackaday.com/2014/08/21/when-worlds-collide-68008-bootstrapped-by-an-arduino-uno/) 控制的 8 位版本。如果 68000 架构赢得了胜利，看看现代 PC 会是什么样子会很有趣。但我们永远不会知道。

 [https://www.youtube.com/embed/xA7M1OJUEUw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xA7M1OJUEUw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

