# 部署全包式 Raspberry Pi 系统

> 原文：<https://hackaday.com/2018/06/04/deploying-a-turnkey-raspberry-pi-system/>

如果你只为自己做项目，那你就是被惯坏了。毕竟你比任何人都了解自己所处的环境。你知道你将拥有什么样的功率，温度范围，以及你的网络是如何配置的。如果您试图部署连接到无线局域网的东西，最后一部分尤其成问题。比方说，你如何配置一个树莓派，让它可以连接到一个未知用户的 WiFi 网络？解决这个问题是[schollz]的[Raspberry Pi turn key](https://github.com/schollz/raspberry-pi-turnkey)项目的目标。

这个想法很简单。一个 Raspberry Pi 图像第一次启动，并提供一个名为 ConnectToConnect 的 WiFi 热点。WiFi 密码也连接到 Connect。连接后，您将获得允许您根据网络定制系统的配置选项。当然，你可以让人们通过串行终端、有线以太网(也不总是设置正确)或 USB 键盘登录并重新配置，但这对大多数客户来说不是一个很好的开箱即用体验。

当 WiFi 凭证输入到地址为 192.168.4.1 的登录表单中时，Pi 将修改其配置，然后自行重启。启动脚本确保连接成功。如果凭证不正确，Pi 将重新引导到 AP 模式，允许您再次重新输入凭证。

这不是一个快速的过程，所以你应该尝试第一次就把它做好。您可以根据说明构建您的映像，或者您可以下载一个现成的映像，然后进行自定义。

我们不禁想到了为 ESP8266 设计的[同类系统](https://hackaday.com/2017/03/18/configure-esp8266-wifi-with-wifimanager/)。我们还想知道我们在 Pi Zero 上看到的[同步 AP 和客户端代码](https://hackaday.com/2017/09/29/simultaneous-ap-client-on-the-pi-zero-w/)是否能帮助【schollz】减少重启需求，但我们对此并不确定。

图片:加雷思·哈勒菲克里[ [CC BY-SA 2.0](https://commons.wikimedia.org/wiki/File:Raspberry_Pi_3_B%2B_(40759294382).png) ]和[ [CC BY-SA 2.0](https://commons.wikimedia.org/wiki/File:Raspberry_Pi_3_B%2B_(26931245278).png) 。