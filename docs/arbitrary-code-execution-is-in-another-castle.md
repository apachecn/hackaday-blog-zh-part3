# 任意代码执行在另一个城堡里！

> 原文：<https://hackaday.com/2017/04/23/arbitrary-code-execution-is-in-another-castle/>

当一个人买了一台计算机，他应该期望拥有者可以在上面运行他们想要的任何代码。然而，通常情况并非如此，因为大多数现代设备出售时都带有锁定的引导加载器，甚至更糟。然而，旧技术更容易处理，但在像最初的任天堂这样的东西上执行任意代码仍然需要大量的跑腿工作，正如[复古游戏力学解释]通过超级马里奥兄弟 3 的内部工作方式展示的那样。

虽然这种黑客行为不会永久性地修改任天堂本身，但它确实允许在游戏中执行任意代码，这主要是由 speedrunners 用来尽快到达结束演职员表场景。为此，通过仔细操作屏幕上的对象将值写入内存。一旦输入了正确的值，游戏中涉及管道的小故障就会被利用来作为指令执行被操纵的存储器。植入的指令最常被用来加载公主的密室并完成游戏，目前的记录徘徊在三分钟左右。

如果你觉得你以前见过类似的东西，你可能会想到[SNES 的超级马里奥世界漏洞，允许相同风格的任意代码执行](http://hackaday.com/2015/01/22/reprogramming-super-mario-world-from-inside-the-game/)。然而，《马里奥 3》的破解更容易实现。还值得看看下面的视频，因为[复古游戏力学解释]深入探讨了哪些值被写入内存，它们如何作为指令执行，以及游戏的所有其他内部工作方式，允许利用这一级别。

 [https://www.youtube.com/embed/fxZuzos7Auk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fxZuzos7Auk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

