# Web 矩阵控件证明了 ESP8266 的强大功能

> 原文：<https://hackaday.com/2016/11/01/web-matrix-control-proves-power-of-esp8266/>

LED 矩阵项目无处不在，但这个项目非常简单:它是一个直接由 ESP8266 板驱动的 LED [矩阵。[Ray]将其作为一个快速项目，供他的学生教授 LED 编程的基础知识。](http://rayshobby.net/wifi-color-led-matrix/)

它是使用他自己设计的 ws 2812 LED 矩阵板和他自己的 [ESPToy ESP8266 开发板](http://rayshobby.net/esptoy/)建造的。但是硬件的要点仅仅是一个 ESP8266 和一些 WS2812。有趣的是用户交互方面的东西。ESP 使 WiFi 和网络服务变得容易，而[Ray]已经在固件中构建了一个简单的 HTTP GET API。对于 web dashboard 和基于 JavaScript 的动画程序来说，这是一个很好的组合[Ray]在下面的视频中演示了这一点。

只需进入同一个网络，加载模块的 WiFi 地址，即可获得 5×7 LED 矩阵的图形表示。选择一种颜色，打开或关闭像素，或者选择一个预定义的模式并将其发送到硬件。这是一种获取用户输入的有效方法，以此为指导，你可以很快地为你能想到的应用程序做好准备。你只需浏览他为研讨会准备的[文档(Zip 文件链接)，包括他用来举办研讨会的所有代码和幻灯片。](http://raysfiles.com/workshops/WiFiLEDWorkshop.zip)

 [https://www.youtube.com/embed/ZKuIWDocIiM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZKuIWDocIiM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

