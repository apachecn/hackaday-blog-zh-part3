# 愚蠢的机顶盒变聪明了

> 原文：<https://hackaday.com/2017/09/01/dumb-stb-gets-smart/>

[Vincent de conick]通过增加几欧元的硬件和一些软件智能，给一个旧的机顶盒赋予了新的生命。有问题的设备是一个老式的 vooder——一个思科机顶盒，由他在比利时的有线电视服务提供商 VOO 提供。

VOOcorder 没有任何 WiFi 硬件或基于浏览器/应用程序的界面。这是一个简单的设备，通过红外遥控器或前面板按钮控制。[Vincent]添加了一个 ESP8266，并将其连接到机顶盒上的红外接收器。他还将其设置为前面板 VFD 显示控制器的 SPI 从机，并将其连接到录像机的调试串行接口。另一方面，该软件需要更多的工作，包括在 ESP 本身上运行的代码、浏览器前端的几个 HTML 页面和 JavaScript 代码，以及在后台运行的几个脚本。

结果是在浏览器中实现了双向交互，允许他发送命令和接收状态信息，并提供了一个用户友好的搜索界面。此外，他的浏览器界面集成了来自服务提供商网站的信息，让他可以安排和录制节目。让我们感兴趣的是，他如何嗅出 IR 信号，找出前面板控制器使用的 SPI 协议，并为 ESP8266 实现 SPI-slave 模式。[Vincent]感到惊讶的是，如此便宜的设备可以处理三个不同的 web 服务器，同时毫不费力地解析两个消息流。

这是一个伟大的黑客告诉我们如何使用超级便宜的电子产品来升级和现代化的旧硬件。休息之后，看看这两个视频——展示了黑客行动的演示，以及硬件修改的演示。

 [https://www.youtube.com/embed/p36RanCVjt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p36RanCVjt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/wscXFrm4DLU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wscXFrm4DLU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

