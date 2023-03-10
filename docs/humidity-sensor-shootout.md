# 湿度传感器枪战

> 原文：<https://hackaday.com/2017/01/03/humidity-sensor-shootout/>

如果你想在你正在制造的设备中测量湿度(和温度，甚至可能是气压)，看看这个包含七个不同选项的[综合测试](http://www.kandrsmith.org/RJS/Misc/Hygrometers/calib_many.html)。我们将在这里总结结果，但是你真的想阅读一下[测试方法论](http://www.kandrsmith.org/RJS/Misc/Hygrometers/calib_dht22.html)——这是伟大的科学黑客。您知道如何使用饱和盐溶液来产生恒定的校准湿度吗？我们没有。

易贝黑客最喜欢的，所谓的 DHT22 模块，表现并不太好，[罗伯特]测试的六个模块中有一个基本上很糟糕，其中三个在使用两年内就坏了。然而，运行良好的那个是相当好的。觉得幸运吗？

博世 BME280 看起来很棒。作为裸部件，它的成本要高一点，当它安装在友好的模块上时，成本会高出几倍，但它似乎非常可靠。你会得到一个额外工作的气压计。事实上，它表现得如此之好，以至于 Hackaday 的贡献者[Nava Whiteford]将该部件[放在扫描电子显微镜](http://41j.com/blog/2016/10/throwing-the-bme280-combined-pressurehumidity-sensor-in-a-sem/)下，以弄清楚发生了什么。

其他传感器都很好，HTU21D 和 SHT71 因其超快速的响应而脱颖而出。详情请点击顶部的链接。去年刚刚在我们的房子里安装了 DHT22s 的六重奏，我们留下了一种沮丧的感觉，我们可能已经得到了我们所付出的，这并不多。至少他们都还在跑。

感谢[Dodutils]和[mac012345]通过[另一个线程](http://hackaday.com/2017/01/01/sst-is-a-very-tidy-esp8266-smart-thermostat)中的注释。