# 在比赛中跑平衡木

> 原文：<https://hackaday.com/2018/03/08/racing-the-beam-on-an-attiny/>

在过去三十年左右的时间里，demoscene 社区一直在通过精心制作的汇编和怪异的图形技巧来扩展计算机系统的可能性。更令人印象深刻的是手工制作的汇编代码，拓展了使用微控制器的可能性。尤其是*小*微控制器。在可能是我们见过的使用这种特殊芯片的最令人印象深刻的演示中，[AtomicZombie]是[在一个 85 号](https://www.avrfreaks.net/forum/impossible-graphics-power-atiny85)上弹跳沸腾的球。这是令人印象深刻的组装工作，[这个视频是我们在这么小的微控制器上见过的最令人印象深刻的东西。](https://www.youtube.com/watch?v=j8apFDjGUTQ)

第一，硬件。这大概是你用 ATtiny85 可以构建的最简单的电路。有一个 ISP 接头，一个带有几个电阻的 VGA 端口，一个由晶体管驱动的 1/8”音频插孔，最重要的是，一个 40MHz 晶体。是的，这款 ATtiny 的运行速度比官方规格允许的速度要快得多，但它确实有效。

这个版本的固件完全是汇编的，但令人惊讶的是没有那么多汇编。如果你把沸腾球的一百多行定义排除在外，那就更少了。

生成的代码以 204×240 的分辨率和每秒 60 帧的速度输出 VGA。这是八种颜色的精灵，有 Alpha，还有四个声道的声音。据我们所知，这是 ATtiny 所能做的极限，也是一个很好的例子，说明如果你认真编写一些非常紧凑的程序集，你能做些什么。

 [https://www.youtube.com/embed/j8apFDjGUTQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j8apFDjGUTQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

