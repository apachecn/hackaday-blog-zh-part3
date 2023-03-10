# 带 FPGA 的显示端口

> 原文：<https://hackaday.com/2015/09/23/displayport-with-an-fpga/>

显示技术面临的挑战之一是，自从 LCD 面板取代阴极射线管以来，带宽大幅增加。低端笔记本电脑有 100 万像素，UHD(“4K”)显示器有 800 万像素，最新的全超高清(“8k”)显示器有 3300 多万像素。更新所有这些像素需要大量的带宽——以 60 Hz 的刷新率更新 4k 显示器需要接近每秒 10 亿字节。80 亿位——这是一个很大的数字！这就是为什么 VGA 端口甚至 DVI 端口开始消失，而代之以 HDMI 和 DisplayPort 等标准。

HDMI 的当前版本是 2.0，并通过 NDA 和许可费进行严格许可。创建了 DisplayPort 标准的 VESA 表示，该标准的实施是免版税的，但自 2010 年 1 月起，VESA 发布的所有与 DisplayPort 相关的新标准不再对非成员可用。

因此，在收到新的 Digilent Nexys 视频 FPGA 开发板后，hack aday regular[仓鼠]购买了一台 UHD 显示器，在互联网上搜索旧的 DisplayPort 1.1 标准，并开始黑客攻击。

几个月和 10，000 行 VHDL 代码之后，可能是第一个工作的开源显示端口
[实现](https://github.com/hamsternz/FPGA_DisplayPort)可用了。该设计包括一个 16 位扰频器、一个 8b/10b 编码器和多通道支持。

我们已经注意到[Eli Billauer]做过类似的事情，但是据我们所知，他的来源并没有公布(尽管他有一些关于他所发现的的有趣笔记)。虽然[仓鼠]是第一个承认它还没有准备好生产，但这为其他人无疑会跟随奠定了基础。没有什么比参考实现更容易比较了！

下面的视频是来自 VESA 标准委员会成员[CraigWiley]的关于 DisplayPort 1.3 的演讲，其中包括对技术细节的高度概括。如果你正在寻找其他 Displayport 技巧，你可以[从 iPad](http://hackaday.com/2014/03/12/an-open-source-ipad-display-adapter/) 驱动外部显示器，甚至[从任何 Displayport 输出驱动视网膜显示器。](http://hackaday.com/2013/07/05/macbook-pro-retina-display-with-a-normal-computer/)

 [https://www.youtube.com/embed/p9bW5GggSDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p9bW5GggSDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[显示端口插头[图片由 Belkin](http://By Belkin [GFDL (http://www.gnu.org/copyleft/fdl.html) or CC-BY-SA-3.0 (http://creativecommons.org/licenses/by-sa/3.0/)], via Wikimedia Commons) CC-BY-SA 提供]