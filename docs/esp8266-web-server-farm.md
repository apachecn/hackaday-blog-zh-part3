# ESP8266 Web 服务器场

> 原文：<https://hackaday.com/2015/09/05/esp8266-web-server-farm/>

似乎有一个黑客格言，无论你在使用什么小工具，最好有几个一起运行。这或许可以解释[埃尔登·布朗]建立的[ESP8266 网络服务器群](http://wa0uwh.blogspot.jp/2015/08/more-esp8266-web-server-farm.html)。是的，一个由三个每个人都喜欢的 WiFi 加密狗，不起眼的 ESP8266 组成的网络服务器群。

Eldon 的服务器群[目前在这里](http://dc02.ebcon.com:8160/)提供网页服务，运行在三块 ESP8266 板上。或者是在这个帖子把它变成一个冒烟的废墟之前(下面的截图以防万一)。每个模块都运行着一个动态网页和他想出的一些[聪明的程序，使得通过这些便宜的设备传输数据更快](http://wa0uwh.blogspot.jp/2015/08/my-wifi-transfer-improvement-160-times.html)。

他的页面并没有什么特别之处，但考虑到它运行在价值约 30 美元的硬件上，包括它所连接的试验板，它还是令人印象深刻的。该页面包括动态生成的图形和一些后端的东西。我不认为它会很快取代任何 LAMP 服务器(ESP8266 花了大约 2.6 秒生成下面的页面)，但它是一个令人印象深刻的黑客。[Eldon]已经发布了运行页面[的网络服务器的全部代码。因此，让我们将网络服务器农场添加到这个小巧设备可以处理的事情列表中，紧挨着](https://github.com/wa0uwh/ERB-EspWebServer)[工厂称重器](http://hackaday.com/2015/06/28/wirelessly-weighting-plants-with-the-esp8266/)、[比特币价格跟踪器](http://hackaday.com/2015/06/18/tracking-bitcoin-with-the-esp8266/)、 [MP3 播放器](http://hackaday.com/2015/06/06/esp8266-as-a-networked-mp3-decoder/)和[更多](http://hackaday.com/2014/12/05/hacklet-25-esp8266-wifi-module-projects/) …

感谢[PuceBaboon]的提示！

[![webfarm-full](img/da477c39b265a0ad9a341ea7e5bad490.png)](https://hackaday.com/wp-content/uploads/2015/09/webfarm-full.jpg)