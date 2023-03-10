# 易趣 K40 激光雕刻机的嵌入式控制器获得结果

> 原文：<https://hackaday.com/2017/06/10/drop-in-controller-for-ebay-k40-laser-engraver-gets-results/>

[保罗·德·格鲁特]写信告诉我们他为易贝随处可见的经济型 K40 激光雕刻机设计的[嵌入式控制器替代品](http://awesome.tech/cheap-chinese-k40-ebay-laser/)。通过更换控制器，可以大大改善雕刻效果，同时简化工具链。用专有软件和笨重的安全加密狗换 Inkscape 和几个插件！[Paul]认为他完成的工作太好了，不能独享，正在考虑小规模生产。

激光雕刻机在许多方面并不是特别复杂的设备；运动控制器在 x 和 y 方向移动头部，需要时打开或关闭激光器。但是，当然，魔鬼在细节中，在你的屏幕上有一个设计和在机器上切割或雕刻之间，可能有惊人数量的*东西*。在 Inkscape 进行设计，出口到 DXF，进口 DXF 到专有软件(需要 USB 安全加密狗才能运行)，清理任何 DXF 进口的小故障，然后最终裁员，这并不罕见。和复杂的抖动雕刻图像？硬件也许可以，但是股票软件和控制器呢？没有那么多。很容易理解为什么用开源解决方案取代专有控制器和软件的项目越来越多。

廉价的激光雕刻机可能带有专有的控制器和软件，但它们不需要一直这样。我们在这一领域看到的其他努力包括 [LaserWeb](http://hackaday.com/2016/07/17/open-source-laser-cutter-software-gets-major-update-new-features/) ，它为 Grbl 或 Smoothieware 等各种开源运动控制器提供了基于浏览器的界面。如果你正在考虑激光雕刻师，花几分钟时间[从其他人的错误中学习](https://hackaday.com/2016/05/31/how-to-fail-at-laser-cutting/)。