# FRDM-K22F 臂板没有 SD 卡插口？没那么快！

> 原文：<https://hackaday.com/2015/10/09/frdm-k22f-arm-board-doesnt-have-an-sd-card-socket-not-so-fast/>

飞思卡尔自由开发板有几种不同的口味和不同的价位。很明显，飞思卡尔一分一分地计算，以达到他们期望的目标价。例如，价格更高、处理器更大的主板(如价格约为 35 美元的 K64F)有插座来安装 Arduino 屏蔽或其他外部连接。许多便宜的电路板(如售价 13 美元的 KL25Z)只有 PCB 孔。如果你想增加插座，那是你的事。

30 美元的 K22F 板有插座，但它也省略了 PCB 上的一些元件。[Erich Styger]注意到电路板上有一个微型 SD 卡插槽，他想知道是否可以通过焊接插槽将 SD 卡添加到电路板上。[答案:是](http://mcuoneclipse.com/2015/10/07/added-micro-sd-card-socket-to-frdm-k22f/)！

其他电路板使用类似的插座，[Erich]将其识别为 Molex 的[SD-105027-001](http://www.molex.com/pdm_docs/sd/1050270001_sd.pdf)(PDF)——一美元部件。在板上焊接插座并不太难，因为焊盘上已经有一些焊料了。[Erich]使用了一些额外的焊膏，并注意到插座下的角落接地焊盘是最难接触到的。你需要一个细铁头。

该板将是一个不错的平台来构建[我们之前提到的使用 K64F 的信号发生器项目](http://hackaday.com/2015/09/15/how-to-build-a-pocket-sized-mbed-signal-generator/)。K22F 有 128K 的内存，512K 的闪存，可以运行在 120MHz。它甚至有一个浮点单元。30 美元还不错。

我们已经介绍了如何在 KL25Z 上开始使用 mbed[(也请参见下面的视频)，使用该板几乎完全相同。您只需选择 K22F 作为目标，并考虑任何 I/O 引脚差异。除了那个教程和信号发生器，我们还看了使用](http://hackaday.com/2015/08/11/getting-started-with-arm-using-mbed/)[一个类似的板作为鼠标](http://hackaday.com/2013/08/07/how-to-use-the-kenetis-kl25z-freedom-board-as-an-hid-mouse/)(巧合的是，【Erich】的另一个项目)。

 [https://www.youtube.com/embed/cKbMyXl3yBA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cKbMyXl3yBA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

