# 用浏览器控制的机器人跟踪你的猫

> 原文：<https://hackaday.com/2017/07/06/stalk-your-cats-with-a-browser-controlled-robot/>

在 Hackaday，一个好的机器人总是受欢迎的，Hackaday.io 用户[ igorfonseca83 ]“浏览器控制的”机器人也不例外。[猫科动物当心](http://www.instructables.com/id/WiDC-Wi-Fi-Controlled-FPV-Robot-with-Arduino-ESP82/)。

在他参与的另一个项目的基础上，机器人本身使用了简单的材料，但你可以使用任何东西。他这次构建的目标是使用通用工具最大化组件和构造的可访问性。

Arduino Uno 使用 H 桥电路驱动两个直流电机，从而独立控制车轮，ESP8266 支持 WiFi 访问，由简单的 5V USB 电源组供电。[ igorfonseca83 ]正在使用 Android 智能手机传输音频和视频数据；虽然这主要是为了他的方便，树莓 Pi 和相机模块组合是另一个很好的选择！

 [https://www.youtube.com/embed/Z30fH5iSuSg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Z30fH5iSuSg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



尽管有一些变通办法——考虑到这种特定配置中的一些组件并不直接相互连接——一堆[代码](http://www.instructables.com/id/WiDC-Wi-Fi-Controlled-FPV-Robot-with-Arduino-ESP82/#step7),建立一个网站作为访问 ESP8266 IP 地址的控制器，以及后来安装在音频/视频流智能手机上的一个应用程序，你就有了一个随时可以摇摆的猫跟踪机器人。当然，fpv 机器人还有其他[用途](http://hackaday.com/2017/02/03/the-ultimate-fpv-cleans-house/)，但结果可能没那么有趣。

[通过 [Hackaday.io](https://hackaday.io) 和 [Instructables](http://www.instructables.com/id/WiDC-Wi-Fi-Controlled-FPV-Robot-with-Arduino-ESP82/)