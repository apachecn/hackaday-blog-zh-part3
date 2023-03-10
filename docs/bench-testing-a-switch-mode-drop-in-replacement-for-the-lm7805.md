# 替代 LM7805 的开关模式跌落基准测试

> 原文：<https://hackaday.com/2016/02/15/bench-testing-a-switch-mode-drop-in-replacement-for-the-lm7805/>

在我们的项目中使用像 LM7805 这样的 5V 稳压器可能会成为习惯，毕竟它们非常便宜，电路也非常基本，因为它们只有两个外部元件，一个输入和输出电容。对于我们大多数 5V 电路来说，这是一个足够好的解决方案，如果我们不注意，就会遇到一些问题。线性调节器在需要散热器和/或主动冷却之前，只能以热的形式消耗这么多功率。即使它们可以产生更清洁的输出，在嵌入式系统中，热量造成的大功率损耗至少也是不理想的。

[【Daniel】需要一种高效的解决方案来代替 LM7805](http://danielelectronics.com/2016/02/09/testing-a-dc-dc-converter-module/) ，在 Adafruit 网站上看到可用的嵌入式替代开关解决方案后，他前往 DigiKey 购买一种类似且更便宜的器件。[Daniel]收集了一些数据，发现稳压器在 12V 输入下的效率为 92%,虽然没有声称的 97%,但仍然是一个很好的解决方案。

[开关电压调节器](http://hackaday.com/2010/08/29/make-switched-mode-power-supplies-do-your-bidding/)并不是什么新东西，所以不要表现得好像我们刚刚赶上了这种开关模式潮流！但是稍微考虑一下你的电源是值得的。当你有心情的时候，让[对 LM7805](http://hackaday.com/2014/09/08/a-detailed-look-at-the-7805-voltage-regulator/) 进行一次极其彻底的检查。