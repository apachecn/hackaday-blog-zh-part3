# 最低 433 MHz 网络家庭自动化

> 原文：<https://hackaday.com/2016/05/01/minimal-433-mhz-web-home-automation/>

一个像样的家庭自动化系统能有多简单？如果你需要一个 HTML 前端，你将需要一个网络服务器。一个 ESP8266 就可以了。然后你需要能够控制你的电子设备。最便宜和最简单的方法是使用无处不在的 433 MHz 遥控插座和一个在线拍卖网站上 1 美元的收音机。加上一个便宜的 ESP8266 模块，你的总支出将低于 20 美元。

这正是尼可斯·坎塔拉基亚斯所做的。他组合了一堆可用的 ESP8266 Arduino 库——一个是用于驱动 433 MHz 无线电模块的，【保罗·斯托弗雷根】的用于[保持时间](https://github.com/PaulStoffregen/Time/blob/master/Time.cpp)和[设置闹钟](https://github.com/PaulStoffregen/TimeAlarms)的库，另一个是用于跟踪[时区](https://github.com/JChristensen/Timezone)——加上他自己的一些用于[设置 WiFi 访问](https://github.com/nikant/espWiFi2eeprom)的代码，这就完成了。

这些都可以在 GitHub 上找到，供你阅读。该代码做了一些奇怪的事情，比如每次设置闹铃时都需要完全重启，但它确实允许您通过 ESP8266 本身提供的 web 界面设置连接设备的重复激活和一次性激活。如果你想让你的咖啡机在早上自动开机，并且想让你家里的其他人也能很容易地配置一个系统，像这样的东西可能就是你想要的。

但是，如果你正在寻找一个 ESP-tech 领域的另一端的项目，[CNLohr]为此编写了一个独立的以太网控制器。哇哦。