# 简易合成孔径雷达

> 原文：<https://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/>

[亨里克]又来了。另一个详细的雷达项目出现在他的博客上。这次【Henrik】对他之前自制的雷达进行了一些重大改进，在他之前的调频连续波(FMCW)系统上增加了合成孔径雷达(SAR)。

[Henrik 的]新设计使用恩智浦 LPC4320，它独特地结合了 ARM Cortex-M4 MCU 和 Cortex-M0 协处理器。HackRF 也使用这种微处理器，因为它有一些特定的功能可以在这里利用，如串行 GPIO (SGPIO ),可以繁琐地配置和高速 USB，单个价格约为 8 美元。混合信号设计在两块板中完成，一个 4 层 RF 板和一个 2 层数字板。

像他这样的绅士一样，[Henrik]在他的 github repo 中包含了原理图、电路板文件和他从 HackRF 项目修改的源代码。在他的帖子中有太多的信息，无法在这里总结，如果你需要即时的满足感，请在休息后查看图片。

如果你没有看到我们对他的[单板 Linux 计算机](http://hackaday.com/2014/07/11/an-amazing-diy-single-board-arm-computer-with-bga/)或[他以前的雷达设计](http://hackaday.com/2014/12/03/extremely-detailed-fmcw-radar-build/)的报道，那么[他的个人博客](http://hforsten.com/)上的报道令人印象深刻，值得一看。

[![](img/85e9665b2f48e9c5f5bb3ed7d68dc6eb.png)](https://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/block_radar/)[![](img/4277f3cba93d3804d58f778f855c98ac.png)](https://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/sar_map/)[![](img/0d14bea44b31d532d18b327f36f0c1d5.png)](https://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/stuffed_purple/)[![](img/c90b55f9fe124cfc8ac79244b3947496.png)](https://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/walk-2/)[![](img/f157a3838e6f032eaf7a6aafc205354f.png)](https://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/xjump_wire-jpg-pagespeed-ic-ogmw1eni1z/)[![](img/e9e86a1870c0c87f160074cd7edaaeb9.png)](https://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/xmcu-jpg-pagespeed-ic-ux1xrtwtu3/)[![](img/a914e58027eb3c4c55b4f8130e38399c.png)](https://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/xmcu_leds-jpg-pagespeed-ic-c1pu0jdahl/)[![](img/0db77866af18f29efa5260b901b0edb1.png)](https://hackaday.com/2015/10/25/an-improvised-synthetic-aperture-radar/xrf_pcb-png-pagespeed-ic-q7cl9zokq5/)