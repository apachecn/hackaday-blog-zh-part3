# 晶体梯形带通滤波器的设计

> 原文：<https://hackaday.com/2016/03/13/designing-a-crystal-ladder-bandpass-filter/>

大多数爱好者使用晶体作为微控制器的外部时钟信号。一个不太常见的用途是为射频信号制作带通滤波器(BPF)。[Dan Watson]在他的博客上解释了[他的晶体阶梯设计，并链接了几个资源来理解理论和创建自己的晶体阶梯带通滤波器。如果你想要一套紫色的印刷电路板，你可以直接从紫色工厂](http://syncchannel.blogspot.com/2016/02/quick-pcb-crystal-ladder-filter.html)[订购。](https://oshpark.com/shared_projects/bY1EnFdp)

[![crystalfilterschematic](img/04c5342c0e38e23b5aac3b5da65dc014.png)](https://hackaday.com/wp-content/uploads/2016/03/crystalfilterschematic.png) 

【丹】的示意图

【丹】引用的来源之一是[【拉里·本科】的个人网站](http://www.w0qe.com/Projects/crystal_bandpass_filters.html)，该网站主要致力于业余无线电项目。你可以找到更多关于 xtal BPF 设计的深入信息。[Larry]详细介绍了他使用的软件以及晶体梯形滤波器的一些应用。[![BPF designed by [Larry]](img/aaa9f89b8426d08c859c5db65c0d2a6a.png)](https://hackaday.com/wp-content/uploads/2016/03/20m_xtalbp_s21close_7-23-2009.gif) 

BPF 由【拉里】

设计该过程包括测量单个 xtalss，以确定哪些 xtal 将为您的目标频率一起工作。[Larry]还将带您了解使用 LTSpice 的软件模拟过程。如果你不熟悉 Spice 模拟，你可以看看我们自己的[Al Williams]的 Spice 系列文章。

感谢[危险原型](http://dangerousprototypes.com/2016/02/08/crystal-ladder-filter/)的提示。