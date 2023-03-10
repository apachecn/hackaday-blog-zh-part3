# 透明 ESP8266 WiFi 转串行桥

> 原文：<https://hackaday.com/2015/09/18/transparent-esp8266-wifi-to-serial-bridge/>

如今，将您的微控制器项目连接到 WiFi 网络相当容易——您可以将 ESP8266 连接到您的微控制器项目，并假装它是一个 WiFi 调制解调器，使用这些老派风格的 AT 命令。但是，如果您需要将新代码刷新到微控制器中，该怎么办呢？你不能通过 ESP8266 远程重新编程微处理器，因为那些愚蠢的 AT 命令会碍事。

解决办法？通过将 [esp-link](https://github.com/jeelabs/esp-link) 固件刷新到您的 ESP8266 中，您可以通过 WiFi 直接与微控制器对话，就像通过串行电缆连接一样:ESP8266 成为了一个完全透明的 WiFi 串行桥。现在，通过串行引导加载程序和 Wifi 转串行桥模式下的 ESP8266，您可以无线刷新微控制器，然后远程登录以远程交互和调试系统。一旦你修复了错误，你就可以重新刷新微控制器:通过 WiFi，而不必爬上梯子去够你的物联网阁楼温度传感器。

例如，要刷新已连接的 Arduino，您需要做的就是说服 AVRDUDE 使用网络，而不是本地连接的 USB 串行电缆:`avrdude -p m328p -c arduino -b 115200 -P net:192.168.1.123:23 -U:yourHexFile.hex`。ESP8266 通过其 TX 和 RX 线将数据直接传递到您的微控制器，一切都像有线一样工作。

允许 ESP8266 加入您的 WiFi 网络的配置在使用[Sprite_tm]的 [esp-httpd 独立服务器](http://www.esp8266.com/viewtopic.php?f=34&t=376)的自托管网页上进行，这使得设置非常容易。然后，您可以简单地在端口 telnet 到 ESP8266，然后键入，或者做任何其他您想用有线串行连接做的事情。

虽然首先出现的是简单的桥接模式，但 esp-link 看起来正在发展成为满足您所有物联网或微控制器+ WiFi 需求的一站式商店。除了串行桥代码，还有一个基于 REST 的微控制器到互联网模式，并且在 wings 中有双向 MQTT 支持。我们还没有机会深入研究这些，所以如果你有，请在评论中告诉我们。

如果你想更深入地研究，可以去[[JEE labs]‘博客](http://jeelabs.org/2015/06/24/ftdi-over-wifi-esp-bridge/)看看这个由代码作者 Thorsten von Eicken 写的稍微有点过时的项目之旅。对于最新的发展新闻，请关注 esp8266 论坛上[的 esp-link 的非常活跃的发展。](http://www.esp8266.com/viewtopic.php?f=34&t=3445)