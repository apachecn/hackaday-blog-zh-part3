# 环法自行车赛电池黑客

> 原文：<https://hackaday.com/2016/09/03/tour-de-force-battery-hacking/>

锂离子电池是非常挑剔的小动物。它们不可能被过度充电、过度放电、过热，甚至看起来滑稽可笑而不起火。在任何笔记本电脑电池组中，电池充电控制器都会监视所有的小电池，防止它们受到损坏。

当然，任何“智能”设备有时都会做出错误的选择，然后就要靠我们去挖掘它的大脑内部并修复它了。当[Viktor]得到一个带有拒绝给电池充电的控制器的完美电池组时，他开始了将成为史诗般的电池控制器之旅，结果不仅仅是一个固定的电池，而是一个控制器重新编程工具、软件和迄今为止的三个反向控制器芯片。

[![devb](img/944b6c9701e222a203617c6099639a8d.png)](https://hackaday.com/wp-content/uploads/2016/09/devb.jpg) 电池控制器芯片讲 SMBus，【维克多】从[打造 USB-SMBus 工具](http://www.karosium.com/p/smbusb.html)开始。这是对 Cypress CY7C68013A USB 微控制器的廉价易贝开发板的巧妙使用。用[Viktor]的[固件](https://github.com/karosium/smbusb)刷新并在主机上运行他的软件，SMBus 扫描简直是小菜一碟。

故事的其余部分是很好的老式黑客:寻找数据表，阅读行业 powerpoints，胡乱猜测，谷歌搜索密码，并在启动控制器时切换无连接引脚。我们不打算对结果进行争论:bq8030 、 [R2J240](http://www.karosium.com/2016/08/hacking-r2j240-lgc.html) 和 [M37512](http://www.karosium.com/2016/08/adding-m37512-with-panasonicibm-firmware.html) 控制器都已经放弃了他们的秘密，对它们进行编程的工具已经集成到了【Viktor】的 SMBusb 工具中。

简而言之，这是我们最近看到的最好的核心黑客之一。荣誉[维克多]！感谢 SMBus 工具。