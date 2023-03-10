# RadiantBee 是一个飞行微波天线校准系统

> 原文：<https://hackaday.com/2017/04/10/radiantbee-is-a-flying-microwave-antenna-calibration-system/>

我们在 Hackaday 链接到的许多项目都有大量的报道，有你可能需要的所有细节的页面。有时，虽然我们偶然发现一个只有简短描述的项目，但它的技术使它值得停下来仔细查看周围的信息网。

这样一个项目就是[F4GKR]和[f5eo]的 [RadiantBee](https://github.com/f4gkr/RadiantBee) ，尝试使用多旋翼上的信标发射机作为天线校准平台。(更多图片见[这条推特](https://twitter.com/sylvain_azarian)。)在这种情况下，多旋翼有一个全球定位系统和一个发射 250 毫秒啁啾声的 10 GHz 信标，接收器可以据此计算信噪比并绘制天线的空间响应。

发射器使用 Raspberry Pi 馈入 HackRF SDR 和 10 GHz 上变频器，而接收器使用 RTL-SDR 馈入 10 GHz 至 144 MHz 下变频器。他们正在测试的天线是直截了当的波导喇叭，但同样的原理可以应用于几乎任何天线。

曾经有一段时间，业余无线电爱好者水平的天线设计需要大量的现场测试，用场强计在大范围内进行物理测量，进行数字关联和性能计算。但是随着计算机模拟的出现，这个领域已经变成了一个更加实验室化的场景，所以看到有人制作真实世界的模拟装置是相当令人耳目一新的。如果你有机会通过实际测量来评估天线，请用双手握住它。你会学到很多东西。

我们已经讨论了很少的实际天线测试，但是在[中提到了一个足球场上的雷达天线测试](http://hackaday.com/2015/03/22/building-a-horn-antenna-for-radar/)。

经由[南门弧](http://southgatearc.org/news/2017/april/ham-radio-10-ghz-beacon-on-a-drone.htm)。