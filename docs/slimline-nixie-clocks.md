# 细长的谢妮钟

> 原文：<https://hackaday.com/2017/07/16/slimline-nixie-clocks/>

每个人都需要在某个时候建造一个谢妮钟。这是一个极好的学习机会；你不仅可以摆弄高压和工具，还可以享受采购过时元件和搞清楚电子设计的机械方面的乐趣。[wouterdevinck]最近接受了建造谢妮钟的挑战。wouter 没有建造一个巨大底座、花哨的 RGB 发光二极管和其他不必要的装饰的时钟，而是建造一个极简主义的时钟。它很纤细，是一件艺术品。

这个谢妮时钟的电路或多或少是你在过去几年里设计的霓虹显示项目所期望的。微控制器是 ATMega328，由 Maxim DS3231 实时时钟提供时间。灯管是标准的俄罗斯 IN-14 Nixies，带有两个用于冒号的 IN-3 霓虹灯。驱动器是两个 HV5622 高压移位寄存器，电源是标准的现成 DC 到 DC 模块，可将 USB 连接器的 5 V 电压转换为显像管所需的 170 V DC。

这里的诀窍是设计。这款钟的电子设备被设计成可以安装在由竹胶合板制成的薄底座上。底座是由三张 3.2 毫米厚的胶合板和一张 1.6 毫米的在小型台式数控机床上加工而成的叠层。

不算腕表，这是我们见过的最薄的谢妮钟表之一，看起来绝对棒极了。你可以看看下面时钟运行的视频，或者在这里阅读[时钟的电路设计](https://circuitmaker.com/Projects/Details/Wouter-Devinck/Nixie)和[代码](https://github.com/wouterdevinck/nixie/)。

 [https://www.youtube.com/embed/FIVFWfgr9bQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FIVFWfgr9bQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

