# 用 ESP8266 做一个便宜的 GoPro 遥控器

> 原文：<https://hackaday.com/2015/12/29/make-a-cheap-gopro-remote-from-an-esp8266/>

GoPro 相机变得相当复杂，但它们还不能读心术:你必须告诉它们何时开始录制。幸运的是，它们可以通过 WiFi 连接非常容易地进行远程控制，这个来自[euerdesign]的简洁教程展示了如何使用 ESP8266 来构建一个[非常便宜的 GoPro 遥控器](http://euerdesign.de/2015/12/28/ultralowcost-diy-gopro-remote/)。这个想法很简单:你按下一个连接到 ESP8266 的按钮，它是用 GoPro 创建的 ad hoc WiFi 网络的详细信息编程的。然后，它向 GoPro 发送一个简单的 URL 请求，go pro 开始记录。总成本？ESP8266 的几块钱，一个按钮和几根电线。

遥控器做什么是由你设置它请求的 URL 定义的:GoPro 的几乎所有功能都可以这样控制。如果你想变得有趣，你可以扩展它来创建一个多按钮遥控器，它可以做其他事情，例如改变帧速率或在你不想冒险使用智能手机或其他同样昂贵的东西的情况下开始向互联网传输。

 [https://www.youtube.com/embed/vy4t8yiqmr8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vy4t8yiqmr8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

