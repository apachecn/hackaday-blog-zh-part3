# 通过裸机编程的 Pi Zero 显卡

> 原文：<https://hackaday.com/2016/01/17/pi-zero-video-card-via-bare-metal-programming/>

推出自己的合成器可不是件容易的事，这正是[托马斯]在他的项目“Nerdsynth”中所做的。[Thomas]在他的网站上有大量数据，涵盖了项目的整体设计和进展，但这并没有激起我们的兴趣。[Thomas]有一个板载 TFT 显示屏来导航多功能 Nerdsynth 的菜单 [![nerdsynth-sketch](img/e46be3137a59b44cddd66559884f72a3.png)](https://hackaday.com/wp-content/uploads/2016/01/nerdsynth-sketch.png) ，但他想添加视频输出来进行一些视频排序。经过一些调查和对可用选项的研究，他决定处理另一个子项目(教科书范围蔓延)。

[Thomas]选择在 Pi Zero 上做一些[裸机编程，将它作为视频卡](http://nerdsynth.com/devblog/2016/01/13/researching-for-video-output/)用于视频输出。通过遵循来自 [Valvers](http://www.valvers.com/open-software/raspberry-pi/step01-bare-metal-programming-in-cpt1/) 的教程和修改来自[microelectroniki](https://microeletroniki.wordpress.com/2012/09/26/raspberry-pi-bare-metal-programming-spi-interface/)的 SPI 驱动程序，他能够在外部监视器上克隆视频。这是朝着正确方向迈出的一步，我们必须关注他的网站，了解外部显示器上视频序列的更新。

休息之后，你可以看看 Nerdsynth 最近的演示，遗憾的是，在[Thomas]发布另一个更新之前，你不得不满足于克隆屏幕的图片(如下)。

[![nerdsynth_tv-942x707](img/5c6f625f8fe0669d5a8c788d7407b085.png)](https://hackaday.com/wp-content/uploads/2016/01/nerdsynth_tv-942x707.jpg)

 [https://www.youtube.com/embed/Uy1dT0vTwQE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Uy1dT0vTwQE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你不熟悉“裸机编程”这个术语，它指的是编写直接在硬件上运行的代码。事实上，我们之前已经讨论过在 Pi 上的[裸机装配。所以把“裸机”想象成没有底层操作系统运行的代码，尽可能接近机器语言，不要用机器语言写程序*。下一个最接近的语言(已经 7 年多了，抱歉*](http://hackaday.com/2014/06/23/programming-pi-games-with-bare-metal-assembly/)*[生锈](http://hackaday.com/2015/12/18/programming-with-rust/))是汇编语言。汇编是你在数据表中已经注意到的代码，但是他们从来没有真正说过:“这些指令是用汇编语言写的”。另一个流行的选择是 C，如果你真的需要，它将允许内联汇编。*