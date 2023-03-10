# 混合模式 PSU 提供高性能

> 原文：<https://hackaday.com/2017/06/18/mixed-mode-bench-psu-delivers-high-performance/>

如果你有一个电子工作台，那么你就需要某种形式的工作台电源。虽然许多电源采用固定电压，但可以肯定地说，最有用的台式电源具有可变电压和可变限流器。这些产品有各种尺寸和质量，可以从通常的网上供应商那里买到，价格低得惊人。

然而，廉价的台式电源存在一个问题。它们总是开关模式设计，其输出通常会有噪声。昂贵的线性电源提供更无噪声的输出，但在调节高压降时会损失过多的热量。

一种解决方案是混合模式设计，其中开关模式电源承担大部分降低电压的艰巨工作，线性调节器降低最后几伏电压，以提供无噪声输出。[Andrei] [向我们展示了他为这种混合模式电源](http://www.instructables.com/id/High-Performance-Adjustable-Power-Supply-50-With-O/)设计的产品，您也可以自己动手制作。

他的主要电源是一个现成的开关，将交流电源转换成 24 伏 DC。然后馈入一个 [LTC1624](http://www.linear.com/product/LTC1624) 降压转换器，将电压降低到高于最终输出电压约 1.2 V，然后馈入一对并联的 [LT3081](http://www.linear.com/product/LT3081) 线性调节器，提供最终无噪声输出。有一个 [INA260](http://www.ti.com/product/INA260) 用于电压和电流测量，还有一个带 LCD 显示屏的 Arduino 作为用户界面。他的原型已经用一个四层 PCB 很好地构建了，尽管他建议可以用适当的 SMD 适配器在条形板上制作。不过，他使用的纸板底盘看起来有点吓人。

这些年来，我们在 Hackaday 讨论了[许多台式电源](http://hackaday.com/tag/power-supply/)。如果你正在寻找作者的最爱，[看看 723](http://hackaday.com/2016/12/02/get-to-know-voltage-regulators-with-a-723/) 。