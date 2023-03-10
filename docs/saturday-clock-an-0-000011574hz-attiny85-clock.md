# 星期六时钟:一个 0.000011574 赫兹的 85 时钟

> 原文：<https://hackaday.com/2017/03/21/saturday-clock-an-0-000011574hz-attiny85-clock/>

当我们试图通过向 CPU 添加更多内核并寻求 GPU 的帮助来挤出额外的时钟周期时，【Ido Gendel】认为反其道而行之会很有趣，[为 ATtiny85 提供一个每天只循环一次的时钟](http://www.idogendel.com/en/archives/579)，或者 0.000011574Hz。这有什么应用呢？好吧，如果他能在七条指令或更少的指令内做到，那么在周五傍晚日落时打开 LED，以指示犹太安息日(周六)的开始，并在周六傍晚日落时再次关闭它，怎么样？

注意微妙之处。一个每天循环一次的时钟意味着你每天最多可以执行一条指令。幸运的是，在 AVR 微控制器上，他需要的指令可以在一个周期内执行。这当然意味着深入汇编代码。[Ido]不是一个汇编向导，所以为了找到指令，他编译 C 代码并检查最终的汇编，直到找到他需要的东西。一个指令打开 LED，紧接着的指令再次关闭 LED，这通常会使其发生得太快，人眼无法察觉。但是打开它的指令在星期五晚上运行，而下一个指令，关闭它的指令，直到星期六晚上才运行。你是否觉得自己置身于科幻故事中，看着时间变慢？怪异。几个 nop 和循环跳转占用了本周剩余的五个周期。

对于时钟源，他选择使用 LDR 来检测一天结束时光线水平下降的时间。他立即遇到的问题是，云、鸟影等等也会导致亮度下降。他找到的解决方案是通过增加一个 [TLV3702](http://www.ti.com/product/TLV3702) 推挽输出比较器和一些电阻来拓宽明暗范围。【Ido】休息后给出视频中电路的详细说明。

我们自己的[埃利奥特·威廉姆斯]研究了 AVR 微控制器，写了这篇关于 AVR 微控制器时钟的精彩文章。

 [https://www.youtube.com/embed/fQeSMwEnRCU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fQeSMwEnRCU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

