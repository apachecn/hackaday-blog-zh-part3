# 超感官知觉统治一切

> 原文：<https://hackaday.com/2017/07/19/def-con-badgelife-the-esp-rules-all/>

Badgelife 是独立硬件创造者的庆典，他们一次工作数月，将定制的电子徽章带到世界各地的会议上。今年在 DEF CON 上，Badgelife 是个大事件。这不仅仅是因为今年应该有一个非电子徽章，也不是因为官方徽章上个月爆炸了——badge life 是关于人们花一年的大部分时间设计和制造硬件，在一个非常特殊的周末达到高潮。

[Garrett]拥有 [Hacker Warehouse](http://hackerwarehouse.com/) ，这是一家提供各种整洁的黑客工具的商店，从软件定义的无线电到锁选择集到侧信道分析工具包。今年，[加勒特]决定拓展他的业务，涉足一点硬件的创造。他对此已经好奇了一段时间，并认为限量版的 DEF CON 徽章是有意义的。他最终得到的是一个漂亮的小徽章，上面有游戏、闪光、图形，还有可能引发很多无线恶作剧。

 [https://www.youtube.com/embed/8qkSUfDYMOI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8qkSUfDYMOI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![](img/e27f84dfffbe3b4ce2b43f6113839332.png)](https://hackaday.com/wp-content/uploads/2017/07/wifi.jpg)

Would you look at that. RF design on an independent badge.

与同样是今年 Badgelife 硬件庆典一部分的 Bender 徽章和令人费解的 crypto 徽章相比，Hacker Warehouse 徽章的设计出奇的简单。板上有一个 ESP8266，采用定制 PCB 实现，包括一个更大的闪存芯片。电路板的另一侧装载了四个 D-pad 排列的轻触开关。顶部是一个 96 x 64 像素的全彩色有机发光二极管显示器，由 14 个迷你 WS2812 RGB LEDs 提供闪烁。电源由两个 AA 电池和一个看起来很漂亮的开关调节器提供。这是真正的硬件，而不仅仅是几个模块和一堆 led 扔在一起。

### 哦，多有趣的无线通信啊

这个徽章是围绕 ESP8266 构建的，这是一个非常有趣的支持 WiFi 的微控制器，具有更多的功能。[Garrett]正在使用 ESP 作为各种 WiFi 扫描仪，允许任何拥有此徽章的人监控 WiFi 信道、接入点、数据包，以及-这很重要 deauth 数据包。

[![](img/f453fced46920bfea85438bec7817416.png)](https://hackaday.com/wp-content/uploads/2017/07/deauth.jpg) 在过去的一年里，互联网上出现了许多采用 ESP8266 并向频谱中释放去授权帧的项目。这些帧导致一个 WiFi 客户端停止使用一个接入点，基本上关闭了一个区域内的所有 WiFi。这是有据可查的，人们已经这样做了很多年，但是 ESP8266 使得 deauth 攻击变得非常非常容易。我们将在今年的 DEF CON 上看到许多 deauth 帧，黑客仓库徽章将能够检测到它们。它也可以*生成*这些帧，但是这种能力现在被锁定了。

### 闪烁发光

[![](img/cda53aa7e202df7dfc708f27bbe595c7.png)](https://hackaday.com/wp-content/uploads/2017/07/blinky.jpg) 电子会议徽章并不酷，除非它有令人讨厌的明亮发光二极管，而黑客仓库徽章*非常*酷。

黑客仓库徽章上有 14 个 RGB LEDs，编程有 46 种不同的模式，亮度足以惹恼别人。这是你需要的徽章，它很漂亮。

这是一个非常棒的徽章，也是 ESP8266 的绝佳开发板。便携式 WiFi 游戏乐趣所需的一切都已经存在——你有闪闪发光的 LED，有机发光二极管，看起来相当不错的电源，以及足够多的按钮来做一些有趣的事情。您只需将一个 USB 转串行适配器连接到预先安装的接头上，就可以对该徽章进行编程了。这是一个很棒的徽章，我们迫不及待地想在下周的 DEF CON 上看到这个伟大硬件的黑客。