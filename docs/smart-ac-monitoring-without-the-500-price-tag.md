# 智能交流监控:没有 500 美元的价格标签

> 原文：<https://hackaday.com/2016/05/25/smart-ac-monitoring-without-the-500-price-tag/>

[Tisham Dhar]对交流电源监控很感兴趣，之前为 ADE7763 制作了分线板。他想找一些更便宜、更现代的东西。ATM90E26 符合要求。它可以通过 UART 或 SPI 通信，并具有多种计量模式。问题？Atmel 的评估模块价格约为 500 美元(而[Dhar]的价格为 800 澳元)，尽管该部件本身的散装价格不到 1 美元。(Atmel 甚至免费送了他三个样品。)

[Dhar]将参考设计中的低电压元件放在 PCB 上，将成本差异纳入囊中。到目前为止，他只测试了微小的低电压测量值。他计划很快做一个全面的测试。

测试设置使用 SPI 模式 3 与处理器通信。你可以在 [GitHub](https://github.com/whatnick/ATM90E26_Arduino) 上找到相关代码。

我们看到许多[能源监控项目被](http://hackaday.com/2012/07/18/monitoring-your-home-energy-use/)搁置。当然，在家用电线上工作是危险的，所以[在那里要小心](http://hackaday.com/2016/05/11/looking-mains-voltage-in-the-eye-and-surviving-part-1/)。