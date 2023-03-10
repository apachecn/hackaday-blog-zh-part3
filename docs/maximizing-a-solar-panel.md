# 最大化太阳能电池板

> 原文：<https://hackaday.com/2015/10/04/maximizing-a-solar-panel/>

太阳能电池板看起来像简单的装置:光进来，电出去，对吗？如果你不关心效率，事情可能就这么简单，但一般来说，你确实关心效率。比方说，如果你正在给电池充电，你会希望把电池板的每一瓦电都用光。问题是，电池可能不会吸收所有可用的电流，基本上只剩下容量。

解决方案是一种叫做 MPPT(最大功率点跟踪)的技术。尽管听起来像是微软的演示插件，MPPT 使用直流到 DC 转换器向太阳能电池提供最大负载，同时向负载提供所需的电流和电压。MPPT 是[阿比德·贾马尔] [用来管理他的太阳能充电器](http://www.electronicslovers.com/2015/09/arduino-based-mppt-solar-charge.html)的。

除了太阳能电池板和直流-DC 转换器，[Abid]的项目还使用了一个 Arduino、一个 LCD、一些指示灯 led 和一些分立元件。他甚至包括一个 ESP8266 来提供无线数据记录。完成的项目驻留在性能板和生活在一个丙烯酸案件。

在 Hackaday 奖竞赛中有一个类似的 [MPPT 项目(事实上，下面的视频来自那个项目的创作者)，我们也看到过](http://hackaday.com/2015/05/23/hackaday-prize-entry-arduino-mppt-controller/)[其他 MPPT 建造](http://hackaday.com/2014/05/05/boost-peak-power-tracking-battery-charger/)。对比不同的设计可能会很有趣。

 [https://www.youtube.com/embed/QsbOs_BoMpU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QsbOs_BoMpU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

