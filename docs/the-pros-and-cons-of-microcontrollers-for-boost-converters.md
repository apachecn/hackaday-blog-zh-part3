# 升压转换器用微控制器的利弊

> 原文：<https://hackaday.com/2018/05/17/the-pros-and-cons-of-microcontrollers-for-boost-converters/>

它从未失败过——我们发布了一个使用微控制器的有点简单的项目，有人指出，如果使用 555 定时器或分立晶体管，甚至几个真空管，它可能会完成得更好。当然，我们欢迎批评；毕竟，周到的反馈是评论部分的重点。有时候反对 Arduino 的人群有一定道理，但是作为[伟大的斯科特！]用[演示了这款无微控制器升压转换器](https://www.youtube.com/watch?v=5R_QCurh_iM)，其他时候只需通过编码来解决问题。

主要是作为对反对者的反击，他最初的升压转换器电路依靠一个 ATtiny85，[伟大的斯科特！]不得不花费相当大的力气来重现他用微控制器轻松做到的事情。他从一个快速演示开始，使用 MOSFET 驱动器和来自函数发生器的 PWM 信号，它可以提高电压，但缺乏控制不同负载所需的反馈。

具有讽刺意味的是，他依赖于一个商用升压控制器芯片的框图，这可能是这项工作的“正确”工具，他将少量元件组装成最终电路。两个运算放大器构成振荡器，另一个用作差分放大器以监控输出电压，最后一个用作比较器以产生 PWM 信号来控制 MOSFET。当然，这是可行的，但这是以大量的努力、费用和性能为代价的。更糟糕的是，添加功能没有简单的途径，就像基于微控制器的设计一样。

当然也有微控制器毫无意义的电路，但是[伟大的斯科特！]如果你坚持狄莺，那么升压转换器不在其中是一个很好的理由。如果你在 DC-DC 转换器的基础知识上落后，不用担心——我们以前已经讨论过这个问题了。

 [https://www.youtube.com/embed/5R_QCurh_iM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5R_QCurh_iM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

