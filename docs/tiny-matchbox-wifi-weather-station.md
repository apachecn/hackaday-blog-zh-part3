# 微型火柴盒无线气象站

> 原文：<https://hackaday.com/2016/05/13/tiny-matchbox-wifi-weather-station/>

有时候，一个项目不一定要在技术上惊人才能赢得我们的心。[Malte]的基于 ESP8266 的气象站是如此可爱，如此完美，很容易值得一看。它完全可能是一种商业产品，而且比火柴盒还小。

它在 PCB 的一侧结合了温度、湿度和气压传感器，在另一侧结合了用于焊接预先构建的 ESP8266 模块的焊盘。把它们焊接在一起，刷新固件，你就差不多完成了。

最后一步是将其配置为与网络配合工作。为此，[Malte]内置了一个基于 web 的配置(和显示)应用程序。它还可以将其数据记录到 MQTT 系统中，因此那里需要更多的配置(我们正试图使这些配置变得更简单)，web 前端使这些工作变得容易。从硬件到固件，甚至是预编译的二进制文件，都在他的 GitHub 上。非常完整，做得非常好。

如果你能看懂德语，或者愿意通过翻译来阅读，也可以看看他的个人项目网页。这里有好东西。现在他所需要的就是一个[来匹配内部的漂亮显示器](http://hackaday.com/2016/03/27/beautiful-weather-station-uses-acrylic-rgb-led-and-and-esp8266/)。