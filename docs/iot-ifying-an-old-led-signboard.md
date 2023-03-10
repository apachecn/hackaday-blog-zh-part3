# 旧 LED 招牌的物联网化

> 原文：<https://hackaday.com/2016/12/26/iot-ifying-an-old-led-signboard/>

滚动 LED 标志在过去很受欢迎，现在很容易买到，价格也很便宜。[为物联网任务](http://ruralhacker.blogspot.pt/2016/12/retrofitting-led-display-into-iot.html)配置一个招牌可能很棘手，但正如[kripthor]向我们展示的那样，只要安全性不是你最关心的问题，并且你可以调整串行接口，这并不是那么糟糕。

[![dec-16-2016-10-57-pm-edited](img/744f3019c042b3b487c99763a22af7ce.png)](https://hackaday.com/wp-content/uploads/2016/12/dec-16-2016-10-57-pm-edited.gif) 【克里普索尔】偶然发现了一个 [Amplus AM03127](http://www.amplus.com.hk/LED_%20AM03127-H13.htm) 招牌，它来自三色发光二极管大行其道的时代。由于电池漏液，该设备配有一个废弃的遥控器，但内置的串行接口提供了一种连接方式。不幸的是，招牌上的 RS-232 标准需要相对于地的正负电压来表示 1 和 0，这不适用于[kripthor]针对的 ESP8266。无处不在的 MAX-232 收发器用于将逻辑电平转换为 RS-232 信号，并增加了一个小型降压转换器为 ESP 供电。写一点脚本，招牌就在网上，随时可以被互联网使用和滥用——[kripthor]说他会后悔，但我们对第一次远程访问的结果很满意。请随意查看[现场视频反馈](http://kripthor.zapto.org:8081/video)，看看当前的信息是什么。

就个人而言，我们不太需要招牌，但让 RS-232 设备在 Arduino 生态系统中工作绝对是我们要记住的一个技巧。如果异步串行协议不是你的强项，你可能想看看我们自己的[埃利奥特·威廉姆斯]的[指南。](http://hackaday.com/2016/06/22/what-could-go-wrong-asynchronous-serial-edition/)