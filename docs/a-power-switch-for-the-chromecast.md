# Chromecast 的电源开关

> 原文：<https://hackaday.com/2016/01/22/a-power-switch-for-the-chromecast/>

Chromecasts 是非常棒的小产品，它们基本上是可以插入任何显示器或电视的小 HDMI 棒，然后使用手机或电脑作为控制器来播放内容。它们由背后的微型 USB 端口供电，如果你幸运的话，你的电视有一个端口，你可以吸走果汁。但是，如果你想在使用电视上的不同输入时将其关闭~~，这样你的显示器就会自动休眠，该怎么办呢？你可能需要[制造一个电源开关。](https://ilias.giechaskiel.com/posts/bluetooth_serial/index.html)~~

现在老实说，Chromecast 变得很热，但与你的电视相比，它在不使用时消耗的电量仍然可以忽略不计。每一瓦特都很重要，[伊利亚斯]以此为契机，完善自己的技能，结合使用 Arduino、蓝牙和 Android 的系统，为 Chromecast 创建一个强大的电源开关解决方案。

设置相当简单。HC-05 蓝牙模块连接到 Attiny85，用一些晶体管控制 5V 电源输出。Arduino 负责蓝牙连接，并使用串行输入来控制晶体管输出。最后，这一切都是由 Android 手机上的一个 [Tasker](https://www.google.ca/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=0ahUKEwi-9JnXzbjKAhXkuIMKHRxcCZIQFggcMAA&url=http%3A%2F%2Ftasker.dinglisch.net%2F&usg=AFQjCNG-mGsCzcoD1tyBfkkOdLvCauFT5w&sig2=T0_9BCVBrFsTKwM9heNrGQ) 插件控制的，它通过蓝牙发送串行消息。

在[Ilias'] [GitHub](https://github.com/giech/arduinotaskerbluetooth) 资源库中可以找到你自己制作一个所需要的所有信息。想了解更多关于 Chromecast 的信息，为什么不看看[我们三年前的评论](http://hackaday.com/2013/08/09/rant-why-i-love-what-the-chromecast-stands-for/)——它已经过时了！