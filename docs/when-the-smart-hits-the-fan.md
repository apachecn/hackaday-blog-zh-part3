# 当智能击中风扇时

> 原文：<https://hackaday.com/2016/05/10/when-the-smart-hits-the-fan/>

风扇曾经是一个简单的装置——马达转动叶片，空气流动，如果你觉得新奇，也许整个东西都会振动。现在风扇有恒温器、定时器和红外遥控器。那么，为什么不通过使[成为具有物联网接口](https://community.smartthings.com/t/make-a-dumb-fan-smart-using-cheapo-esp8266-board-controllable-via-st-universal-ir-remote/47212)的智能风扇来增加复杂性呢？

[Casper]的项目看起来更像是一个概念验证或学习平台，而不是家庭自动化的一次认真尝试。他的构建日志提到了基于 Raspberry Pi 的早期迭代。但 ESP8266 是一个更好的选择，并成为最终的构建，它使用红外 LED 来模拟来自遥控器的信号，以便支持风扇的所有股票模式。整个东西是电池供电的，位于风扇顶部的试验板上，但我们敢打赌，一个小手术可以植入接口，并从内部窃取电力。至于界面，你可以选择——通过 [SmartThings](https://www.smartthings.com/) 家庭自动化平台的 iOS 应用，通过他们的 [SmartTiles](http://www.smarttiles.click/) 网络客户端，或者使用亚马逊 Echo。【Casper】提到也在调查 MQTT，但是有些困惑；我们建议他查看一下 [【埃利奥特·威廉姆斯】“MQTT](http://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/) 新教程”来了解最新情况。

 [https://www.youtube.com/embed/R_ssJNsGbx0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/R_ssJNsGbx0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Benji]的提示。