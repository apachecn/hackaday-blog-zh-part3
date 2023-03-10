# 通过您的 Pi 3 连接您的所有物联网

> 原文：<https://hackaday.com/2016/04/29/connect-all-your-iot-through-your-pi-3/>

如果你在玩*时下流行的宾果游戏*，今天是你的幸运日！因为这篇文章不仅包含了“Pi 3”和“IoT”，而且我们正要键入“ESP8266”和“家庭自动化”。检查一下看有没有填一行什么的…

不过说真的。如果你在运行一个家庭设备网络，并且像我们一样完全不安全地运行，你可能想至少把这些东西从更大的互联网上隔离开，并且可能也隔离掉你关心的任何计算机。最简单的方法是将您的设备放在它们自己的 WiFi 网络上。你刚买的那个闪亮的 Pi 3 有 WiFi，而且不会用太多的电，以至于你会介意一直开着它。

即使你不是 Linux 网络专家，【Phil Martin】关于[将 Raspberry Pi 3 设置为 WiFi 接入点](https://frillip.com/using-your-raspberry-pi-3-as-a-wifi-access-point-with-hostapd/)的教程应该可以让你轻松地将 Pi 3 用作物联网系统的 WiFi 中心。他甚至向您展示了如何配置它，以通过有线以太网将您的物联网网络的数据包转发到现实世界，但如果您也可以使用 Pi 3 作为您的中央服务器，这甚至可能没有必要。您想要的大多数物联网服务都可以在 Pi 上获得。

那些确实想向世界开放的人，你可以很容易地在 Pi 上设置一个非常严格的防火墙，不会干扰你家的正常 WiFi。这里有一个在 Pi 上设置 iptables 的[快速指南，但是使用像](http://qcktech.blogspot.de/2012/08/raspberry-pi-as-router.html) [Shorewall](http://shorewall.net/) 这样更友好的软件也应该可以完成这项工作。

还没有填满你的宾果卡吗？“Arduino！”