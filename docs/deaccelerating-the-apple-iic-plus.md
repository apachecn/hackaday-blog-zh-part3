# 苹果 IIc Plus 加速

> 原文：<https://hackaday.com/2016/02/13/deaccelerating-the-apple-iic-plus/>

从我的经验来看，Apple IIc Plus 可以说是有史以来最好的 Apple II 电脑。它是便携式的，比 IIe 更快，有更高容量的内置驱动器，由于 Plus 可以以 4MHz 运行，它比奇怪的 8 位*或*16 位苹果 IIGS 更快。最近，[Quinn]迷上了 IIc Plus，甚至制作了一个定制的游戏手柄，并将 IIc Plus 变成了一台笔记本电脑。现在，她[将她的注意力转向了苹果在 Apple IIc Plus](http://quinndunki.com/blondihacks/?p=2546) 上犯的几个错误——启动时发出嘟嘟声，每次启动时默认为 4MHz，而不是 Apple II、II Plus、IIe 和 IIc non-Plus 中使用的 Apple II 的标准 1MHz。

最初的苹果二代出奇的原始。除了写一个 nop 循环和计算周期之外，没有办法保持时间。没有时钟，没有计时器，没有滴答计数器，也没有中断。如果你正在为 Apple II 编写一个依赖于精确计时的游戏，你能做的最好的事情就是一个延迟循环。这在一段时间内是有效的，直到苹果 IIc Plus 以 4MHz 的默认时钟发布。对于 AppleWorks 和其他生产力应用程序来说，这是一个伟大的想法，但[奎因]正在做逆向计算，这意味着游戏。将 Apple IIc Plus 启动到 1MHz 模式意味着每次重启电脑时都要开机并按住 escape 键。这很烦人，但是一个让 IIc Plus 默认运行在 1MHz 的 mod 会让她成为目前最有成就的活跃的 Apple II 开发者之一。

引导进入 IIc Plus' 1MHz 模式的过程需要在重新启动计算机时按住 escape 键。这应该告诉你一些事情:改变速度的不是硬件开关。它在 ROM 中，这意味着要深入技术参考手册，查看 ROM 监视器中的列表，并弄清楚一切是如何工作的。

IIc Plus ROM 非常复杂——它是 32k 的手工汇编代码，到处都有跳转表。经过大量的研究，[Quinn]成功地对“按下 ESC 键时减速”程序进行了逆向工程，允许她在默认情况下以 1MHz 启动机器，如果按下 option 键进行软复位，则以 4MHz 启动机器。一切都很好，而且[Quinn] [有视频为证](https://www.youtube.com/watch?v=pQjzt_7IUUc)

这并不是[奎因]第一次试图侵入苹果 IIc Plus ROM 的最底层。因为 IIc Plus 默认运行在 4MHz，所以启动嘟嘟声是非常错误的。她修好了那个，用她腰带下面的两个非常有用的补丁，她用她的 ROM 补丁烧了一些新的芯片。总的来说，在新的 32k ROM 中只有几十个字节，但这足以让她成为当前 Apple II 平台的顶级固件开发者之一。