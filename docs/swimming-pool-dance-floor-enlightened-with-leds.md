# 发光二极管照明的游泳池舞池

> 原文：<https://hackaday.com/2015/10/24/swimming-pool-dance-floor-enlightened-with-leds/>

在一篇记录丰富的博客文章中，[Loren Bufanu]展示了一个项目，用 RGB 条照亮了覆盖游泳池的玻璃舞池。我们在一个黑客日链接中提到了他的项目的[视频，但没有任何背景信息。现在我们知道了。](http://hackaday.com/2015/08/16/hackaday-links-august-16-2015/)

![boards in box](img/bd24cbed480b04a95774bbed56fba032.png)该项目采用了大约 450 米长的 RGB 条纹，由[两个 Rainbowduinos](http://www.seeedstudio.com/wiki/Rainbowduino_v3.0) 控制，并由 64 个功率 Mosfets、64 个双极晶体管和一些其他组件驱动。从发光二极管产生白光需要 8 安培的电源。

Rainbowduino 是 ATmega328 Arduino 兼容板，带有两个 MY9221 控制器。每个控制器处理 12 个通道的自适应脉冲密度调制。换句话说，它使 led 闪烁得很好。[Loren]使用 Rainbowduino 而不是一些替代品，因为多个 R 'duinos 可以协调他们在 I2C 的活动。

项目的软件部分没有硬件部分好。灯光图案应该跟随正在播放的音乐。一个旨在驱动 R'duinos 的个人电脑软件包产生了一个烂摊子。一些杂牌，包括截屏(！)，被一批文件驯服了的肆意妄为所驱使。

已经有一段时间了，但是由克里斯·威廉姆森建造的一个类似的迪斯科舞厅引起了我们的注意。[克里斯]是恐怖技术中的一个原则，最近在 spark fun 上获得了[的提名。](https://www.sparkfun.com/news/1954)

休息后的视频幸运地没有引起大的轰动，但仍然令人震惊。

 [https://www.youtube.com/embed/T_f5dAWeeKg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T_f5dAWeeKg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

