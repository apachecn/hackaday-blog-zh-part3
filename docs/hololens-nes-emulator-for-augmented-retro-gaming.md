# 增强复古游戏的 HoloLens NES 模拟器

> 原文：<https://hackaday.com/2016/08/24/hololens-nes-emulator-for-augmented-retro-gaming/>

[Andrew Peterson]正在寻找一种方式，以更现代的方式沉迷于他的复古游戏激情。他的 [3D NES 模拟器“N3S”为 Windows](http://n3s.io/) 带来了任天堂经典的全息透镜，将像素转化为体素，将超级马里奥转化为增强现实姜饼人。

为了在 HoloLens 上运行 NES 游戏，[Andrew 的]模拟器使用了 [Nestopia libretro 内核](http://wiki.libretro.com/index.php?title=Nestopia)。由于 AR 眼镜呼吁增强游戏本身，N3S 重新模仿了 NES 的图片处理单元(PPU)，使其能够在 3D 空间中解释任天堂游戏的图形。[Andrew]还整理了一份关于最初的任天堂 PPU 如何工作的[综合解释](http://n3s.io/index.php?title=How_It_Works)，以及他如何为 HoloLens 重新实现它。

当前版本的 N3S PPU 模拟器通过简单地从游戏的 rom 中挤出原始图案数据来自动生成体素，但[Andrew]正在考虑更多的功能。用户可以在一个内置的编辑器中塑造他们自己的原始图形元素的 3D 版本，然后模型集可以在一个在线数据库中使用。从那里，玩家只需下载他们最喜欢的游戏的 3D 模块，然后在 HoloLens 上玩。

根据[Andrew]的说法，模拟器达到了当前预生产版本的 HoloLens 可以流畅渲染的极限，因此这个项目的未来可能取决于未来的硬件代。然而，HoloLens 的截屏[Andrew]让我们渴望更多的增强复古游戏。享受视频！

 [https://www.youtube.com/embed/WEWcc-cF3g0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WEWcc-cF3g0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

