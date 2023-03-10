# 音频耦合烟雾报警接口发送文本、电子邮件

> 原文：<https://hackaday.com/2015/11/16/audio-coupled-smoke-alarm-interface-sends-texts-emails/>

物联网正在成为一项大业务。谷歌的 Nest 品牌是这一趋势的一部分，他们正在建立一个产品线，填补利基市场，看起来很好，包括 Nest Protect 烟雾和一氧化碳探测器。如果你的烟雾报警器响了，收到短信和电子邮件是很好的，但是如果你不想花 99 美元来享受这个特权，看看这个 [$10 DIY 烟雾报警器界面](http://www.simpleiothings.com/10-diy-wifi-smoke-alarm-notifier-roost-nest-alternative-full-tutorial/)。

将[Team SimpleIOThings']界面的成本保持在最低水平的秘密是利用非常便宜的 ESP8266 平台和[上可用的功能。为了使电路尽可能简单和通用，ESP8266 开发板通过一个简单的麦克风传感器与现有的烟雾探测器接口。从我们所看到的，它只是一个声级传感器，这应该与靠近烟雾探测器的麦克风工作良好。但是在你的房子里有很高的噪音水平，就像孩子和狗带来的噪音，假警报可能是一个问题。在这种情况下，我们打赌软件可以被修改来监听大多数现代烟雾探测器使用的](https://ifttt.com/)[时间三模式](https://en.wikipedia.org/wiki/Fire_alarm_notification_appliance#Coding)。您甚至可以添加代码来发送一个单独的消息，让 CO 检测器发出一个时间 4 模式的声音。

与烟雾探测器接口并不是什么新鲜事，这个 ESP8266 之前的项目就证明了这一点。但是多功能的 WiFi SoC 使得像这样的接口变得快速而简单。

 [https://www.youtube.com/embed/_Ec-0__Wh3w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_Ec-0__Wh3w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

