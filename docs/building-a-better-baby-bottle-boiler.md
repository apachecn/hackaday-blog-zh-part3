# 建造一个更好的奶瓶锅炉

> 原文：<https://hackaday.com/2017/07/08/building-a-better-baby-bottle-boiler/>

[Sebastian Foerster]有段时间没去他的博客了。他和妻子刚生了双胞胎，所以他一直忙着站着等配方奶或牛奶来暖暖身子。作为一个技术型的人，他看了看目前市场上做这件事的工具，分析了它们，然后决定自己做这件事。

[Sebastian]看着他的 Nespresso Aeroccino——一种牛奶起泡机，旨在为您提供热或冷的泡沫牛奶，作为您决定放在上面的任何饮料的顶部。这使得牛奶有点太热，60 摄氏度，但一旦达到这个温度，它就会关闭，所以如果[Sebastian]可以让它在更低的温度下关闭，他就找到了解决方案！

在拆开 Aeroccino 并检查电路后，它似乎是一个简单的设计，依赖于一个电阻器和连接到 [ATTiny44 微控制器](http://www.microchip.com/wwwproducts/en/ATtiny44)的 [NTC(负温度系数)热敏电阻](https://en.wikipedia.org/wiki/Thermistor#NTC_.28Negative_temperature_coefficient.29)。[Sebastian]不想对 ATTiny 重新编程，所以他查看了电阻和 NTC。电阻器和热敏电阻形成分压器，电压由微控制器通过模拟引脚读取。在查找热敏电阻的一些信息并用电位计替换该电阻后，[Sebastian]可以在用温度计测量的同时调整关闭温度。当他得到他喜欢的温度时，他读取电位计的值，然后用几个串联的电阻代替它。

现在[Sebastian]在大约 25 秒内将婴儿奶瓶从冰箱中取出并加热。当瓶子变热时，他不必担心盯着瓶子。我们确信，在一分钟之内准备好两瓶酒比等十分钟更让初为人父母的人紧张。为了获得更多关于热敏电阻的乐趣，看看我们关于由环境控制的[电阻的文章](https://hackaday.com/2016/09/27/variable-resistors-controlled-by-the-environment)或者看看这个[蓝牙烧烤温度计](https://hackaday.com/2015/10/21/bluetooth-thermometer-minds-your-meats/)！