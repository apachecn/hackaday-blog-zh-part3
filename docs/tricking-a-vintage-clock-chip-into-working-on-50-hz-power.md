# 骗一个老式时钟芯片工作在 50 赫兹的功率

> 原文：<https://hackaday.com/2018/06/11/tricking-a-vintage-clock-chip-into-working-on-50-hz-power/>

由于微控制器、RTC 模块和大量廉价有趣的显示选项，数字时钟项目变得相当容易。然而，选择基于一个 70 年代后期的日期代码的芯片构建时钟，你的构建肯定不仅仅是普通的。

这是[弗兰·布兰奇]发现自己在进行一个正在进行的项目的船上。问题中的芯片是 Mostek MK50250 数字闹钟芯片，她的第一个障碍是找到一种方法，用北美 60 赫兹的功率运行 50 赫兹的时钟。这是因为工程师在设计过程中有时不得不做出妥协，这有时会导致错误的假设。似乎 Mostek 的设计者认为只有在线路频率为 50 赫兹的地方才需要 24 小时显示。然而[Fran]想要 60 Hz 的军用时间，所以她想出了一个欺骗芯片的电路。它使用 4017 十进制计数器将 60Hz 信号除以 10，并使用 6Hz 输出来开启晶体管，将 60Hz 输出拉低一个脉冲。结果是每六个脉冲中就有一个被丢弃，这给了 Mostek 所需要的 50 赫兹信号。当然，脉冲链是不对称的，但芯片不会在意，而且[弗兰]得到了她想要的时钟。相当聪明。

[Fran]已经研究这个时钟有一段时间了，我们很想看看它是什么样子的。我们希望她会使用[这些超大的不完全是光导管的 LED 显示屏](https://hackaday.com/2018/03/18/this-big-bright-seven-segment-display-is-3d-printable/)或类似的东西。

 [https://www.youtube.com/embed/4Om4yvI5KP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4Om4yvI5KP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

