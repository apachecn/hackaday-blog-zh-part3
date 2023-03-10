# 用于 ESP8266 的智能开关板

> 原文：<https://hackaday.com/2017/04/17/a-smart-switch-board-for-the-esp8266/>

随着大量物联网项目和廉价的商用智能灯具和电源开关的出现，你可能会认为在这个拥挤的市场上再提供一种产品是多余的。但是在任何领域都有改进的空间，在这个特殊的领域，Xose Pérez 已经通过他的 Espurna 董事会做到了这一点。

该板是一个非常好的执行 ESP8266 电源继电器，具有板载电源和电源监控。它是根据他的定制固件设计的，该固件支持 Alexa、Domoticz、Home Assistant 和任何支持 MQTT 或 HTTP REST APIs 的东西。

最棒的是，它是一个开源硬件，所以你可以从他的 GitHub 库下载你需要的一切[来创建你自己的。为了最大的方便，你甚至可以](https://github.com/xoseperez/espurna-board)[从奥什公园](https://oshpark.com/shared_projects/CrcD9Wsy)订购现成的印刷电路板。

作为 Espurna 板在实际应用中的演示，他制作了[一个智能插座项目](http://tinkerman.cat/espurna-smart-socket/)整齐地封装在一个壁式盒子中，内置欧式插头和插座。

我们在 Hackaday 之前已经多次介绍过[Xose]的工作，他是一位物联网奇才。最近有[他与 Alexa 和 ESP8266](http://hackaday.com/2016/11/23/alexa-make-my-esp8266-do-something/) 的合作，但在此之前是他的 [MQTT LED 阵列](http://hackaday.com/2016/10/11/64x16-led-mqtt-laundry-display/)用于他的[洗衣监视器](http://hackaday.com/2016/08/01/your-laundry-is-done/)。