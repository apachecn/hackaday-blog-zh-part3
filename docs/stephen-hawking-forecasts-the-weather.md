# 斯蒂芬·霍金预测天气

> 原文：<https://hackaday.com/2017/03/08/stephen-hawking-forecasts-the-weather/>

斯蒂芬·霍金虽然不能自己说话，但他的声音是通过计算机和声音模拟器提供的，人们很快就能辨认出他的声音。可能会让一些人感到惊讶的是，这个语音模拟器，Emic2，已经被许多人使用，并且今天仍然存在，可以用于您正在进行的任何文本到语音转换项目。作为这方面的一个很好的例子，[tegwyntmmffat]已经[建立了一个天气预报站，使用 Emic2 语音模块](https://hackaday.io/project/20081-ai-weather-presenter-stephenhawking)来提供可听的天气警报。

除了独特的声音，天气中心本身也是一个高质量的建筑。配备有 [GPRS 模块](https://en.wikipedia.org/wiki/GPRS)的 Arduino Mega 2560 能够每小时获取一次天气信息。在构建语音模块之后(这看起来就像是一个项目本身),将 Arduino 的信息传递给该模块并让它开始播报天气是相对简单的。它甚至可以被编程为给你唱天气预报！

如果你对构建自己的 Emic2 语音系统感兴趣，可以在项目网站上找到[tegwyntmmffat]用来构建这个系统的所有代码。同样值得注意的是，几乎任何人都可以使用 GPRS，这是一个相对简单的系统，开始使用它来做一些事情，如获取天气信息，但你也可以使用它来推出你自己的私人手机网络，只要有合适的设备和许可。