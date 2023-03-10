# TI 99/4A 气象站

> 原文：<https://hackaday.com/2017/04/30/ti-994a-weather-station/>

如果你仍然有一抽屉上世纪 90 年代的手镯，因为你知道，它们可能会回来，那么你会欣赏[涡旋]的最新项目。当然，我们看到许多气象站，但是这个是由 TI 99/4A 电脑控制的。这台 20 世纪 80 年代的家用电脑实际上是领先于其 16 位处理器的。

传感器使用 Xbee 模块和 Arduino Uno。当然，Uno 比 TI 的计算机有更大的能力，但这不是重点，对吗？他制作了一系列视频详细介绍了这一构造(你可以在下面看到第一个，但目前为止有五个)。

通常，与 Arduino 进行串行通信需要 TI 计算机上的汇编语言。然而，TI hacker [Rich Gilbertson]已经解决了这个问题。他创建了 Rich Extended BASIC (RxB ),它有一个调用 IO 语句，非常适合[vortex on]的需求。

TMS9900 CPU 有一个新颖的特性，子例程调用导致寄存器移位，因此每个子例程都有一些与其调用者共有的寄存器和一些私有的寄存器。这在理论上听起来不错，但随着处理器速度的提高(这台计算机中的 9900 只运行在 3 MHz)，驻留在主存储器中的寄存器是一个死刑判决。它还有一个基于 sprite 的图形处理器，在游戏中效果很好。

不管多么不切实际，我们喜欢这些古老的复古项目。即使在 20 世纪 80 年代 TI 99/4A 的新主人会对你现在一顿美餐的费用可以买到多少计算能力感到震惊，TI 仍然能够在它的一天产生一些令人印象深刻的输出。虽然它可能无法玩《毁灭战士》或《使命召唤》，但它可以应付[和](https://hackaday.com/2014/04/08/vcf-east-old-computers-new-games/)。

 [https://www.youtube.com/embed/-9D0889Mks0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-9D0889Mks0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

