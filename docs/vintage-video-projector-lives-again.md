# 老式视频投影仪再次复活

> 原文：<https://hackaday.com/2015/12/10/vintage-video-projector-lives-again/>

投影仪现在越来越便宜了，因为中国大量生产微型投影仪。但是你知道吗，把一台旧的幻灯机转换成数码的并不难。[Alec Smecher] [向我们展示了如何使用 1950 年的 LaBelle 75 幻灯机](http://cassettepunk.com/blog/2015/12/06/diy-projector-conversion/)，结果非常棒。

[![dmd_chip](img/986d18d386e6c94836981fb051311e51.png)](https://hackaday.com/wp-content/uploads/2015/12/dmd_chip.jpg) 数字投影仪可以使用几种不同的技术来工作。最好、最亮的是德州仪器的 DLP(数字光处理)——这是高端、高流明数字投影的全球标准。它的工作原理是从三个 DMD(数字微镜器件)反射红、绿、蓝光，这三个 DMD 有一个微小的 2 位置反射镜阵列，每个反射镜代表一个像素。

较老的技术之一是 LCD，它更容易理解。你通过彩色液晶显示器发出白光，这就是你的投影。那么，一台投影仪只需要一个液晶显示器、一个光源和一点光学元件。

由于幻灯机已经有了光学系统，这样的转换就像用 LCD 替换幻灯片支架一样简单(你必须[移除背光使其透明](http://hackaday.com/2013/12/31/case-modder-builds-lcd-window-causes-lsd-flashbacks/))，如果你愿意，还可以将昂贵的灯升级为 LED。

[Alec]使用 2.2 英寸的 LCD，一个树莓 Pi 向它提供视频信号，一个 10W 的 LED 为整个系统供电。由于所有这些组件都非常小，所以将所有组件放入原始投影仪的外壳并不困难。不幸的是，他使用的液晶显示器只有 320 x 240 的分辨率，尽管我们认为他可以升级它，如果他想的话。

不管分辨率如何，最终的结果是一个华丽的古董投影仪，带有数字扭曲。

 [https://www.youtube.com/embed/7yg2WddIhZE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7yg2WddIhZE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这些年来，我们已经分享了许多 [DIY 投影仪构建](http://hackaday.com/2010/03/04/diy-projector-collection/)。如果你正在寻找一个更高分辨率的构建，[只需使用一个桌面液晶显示器！](http://hackaday.com/2013/12/10/diy-3d-projector-from-an-lcd/)