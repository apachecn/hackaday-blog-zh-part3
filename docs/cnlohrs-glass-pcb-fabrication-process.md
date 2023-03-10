# [CNLohr]的玻璃 PCB 制造工艺

> 原文：<https://hackaday.com/2016/07/18/cnlohrs-glass-pcb-fabrication-process/>

[CNLohr]更大的名气之一是他制造玻璃印刷电路板的工艺。它们与常规的玻璃纤维基 PCB 非常相似，但[CNLohr]是在显微镜载玻片上构建电路。我们已经看到他制作了[一个玻璃 PCB LED 时钟](https://hackaday.com/2012/07/16/glass-pcb-led-clock/)和一个 [Linux《我的世界》以太网东西](https://hackaday.com/2013/02/18/cnlohrs-microscope-slide-linux-avr-minecraft-thing/)，但是直到现在，[CNLohr]制作这些玻璃 PCB 的过程还没有深入到复制这些项目所需的深度。

上周末，[CNLohr] [制作了一系列视频](https://www.youtube.com/watch?v=vlrccFVsQXA)，讲述他如何将微小的玻璃片变成功能电路。

从最高层次的理解来看，[CNLohr]的玻璃 PCB 与传统的自制覆铜板 PCB 没有任何不同。有一个基板和一层铜膜，铜膜被蚀刻掉以产生迹线和电路。细节决定成败，这个版本有很多细节。让我们深入了解一下。

为了将铜粘合到载玻片上，[CNLohr]首先通过用丙酮脱脂，并用钢丝绒摩擦铜来准备材料。胶水是 Loctite 3301，一种低粘度的光固化胶水，可以在铜和玻璃之间刮擦，然后用生长灯曝光。

这足以在玻璃上获得铜，但离电路板只有几步之遥。为了蚀刻铜，[CNLohr]正在使用 Riston 薄膜光刻胶。这是通过用几滴水将其漂浮在铜上，并将其通过层压机来应用的。激光打印机光掩模用一些三合一油浮在 Riston 上，光刻曝光，然后去除。

接下来的几个步骤——洗掉未固化的光刻，蚀刻铜，洗掉固化的光刻——是这个过程中给[CNLohr]带来最大困难的部分。他需要使用不影响玻璃和铜之间结合的化学物质。他发现碳酸钠可以很好地去除未固化的光掩模，氯化铁可以很好地蚀刻铜(尽管我们在氯化铜和过氧化物方面有很好的经验)，氢氧化钾可以去除固化的光掩模。去掉固化的光掩模，【CNLohr】就有了一个完美的玻璃电路板。

当然，如果不将元件焊接到玻璃 PCB 上，制作玻璃 PCB 是没有用的。为此，[CNLohr]正在使用铋焊膏进行低温热板焊接。如果你只是做单面 SMD 工作，这是一个伟大的方式来生产美丽的玻璃电路板，但现在我们想知道一个足够小的金刚石钻头是否允许双面结构。

 [https://www.youtube.com/embed/vlrccFVsQXA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vlrccFVsQXA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/rj4qe6bdu7k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rj4qe6bdu7k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/s_r8QfjhWlo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/s_r8QfjhWlo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

