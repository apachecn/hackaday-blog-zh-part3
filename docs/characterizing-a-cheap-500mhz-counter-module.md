# 表征廉价的 500MHz 计数器模块

> 原文：<https://hackaday.com/2016/11/16/characterizing-a-cheap-500mhz-counter-module/>

过去几年一个令人兴奋的发展是非常便宜的仪器模块的出现，这些模块很容易在网上买到，通常从中国运来。他们中的一些人对他们的价格有非常令人印象深刻的纸张规格，这是其中一个引起了[Carol Milazzo，KP4MD]的注意。一个频率计数器，在你最喜欢的网上零售商那里售价不到 14 美元，声称频率范围为 500 兆赫。这本身可能是一种有用的仪器，其范围远远超过不久前昂贵得多的试验台测试设备的能力。

然而，它到底有多好，它能兑现承诺吗？ [[Carol]展示了她从设备](https://photos.google.com/share/AF1QipP1euFHGxNkvoEtaH80y8sURWg1Uzgs1VQoHdTxBcrajAl-Kb7_leDCmqgZRRIoWw?key=bUQ4dFV5cm5WNTVqb2piZWtYM0ViVkVkWmFtN21n)上获得的测量值，这样你们就可以亲眼看到了。她首先根据 GPS 规定的标准检查其校准，并使用板载微调器进行微调，然后在很宽的范围内考察了灵敏度、VSWR 和输入阻抗。

就灵敏度而言，它有点聋，10 MHz 时锁定需要 0.11 Vrms。与此同时，它的输入阻抗从量程下限的 600 欧姆下降到 200 MHz 时的 80 欧姆，VSWR 也有相应的变化。因此，它永远无法与高端台式乐器相媲美，因为您期望它具有更高的灵敏度和更稳定的阻抗，但就价格而言，我们相信这是您可以解决的问题。与此同时，值得注意的是，从她发布的图片来看，该板没有用于 SPI 接口接头的空间，这使得它有可能被用作测井仪器。

我们认为有必要尽可能多地了解此类元件的信息，既要了解市场的新进入者，也要了解它们的真实性能。所以如果你对那些便宜的频率计数器模块感到好奇，现在多亏了[Carol]你对它们能做什么有了一些概念。

虽然购买像这样的计数器模块很方便，但当然没有什么可以阻止您构建自己的模块。多年来，我们已经推出了许多产品，例如这款使用 74 系列预分频器的 100MHz 产品或这款提供 T3 的 [ATtiny 产品，或者这款使用 Android UI 的](http://hackaday.com/2016/07/02/hackaday-prize-entry-a-minimal-attiny-voltage-and-frequency-counter/)[非常出色的产品](http://hackaday.com/2016/03/29/nanocounter-frequency-counter-with-an-android-ui/)怎么样？