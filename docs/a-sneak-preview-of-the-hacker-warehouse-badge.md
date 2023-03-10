# 黑客仓库徽章的预览

> 原文：<https://hackaday.com/2018/07/06/a-sneak-preview-of-the-hacker-warehouse-badge/>

我们很幸运地拿到了新的黑客仓库徽章的手工焊接原型，好家伙，这是一种享受。它很时尚，很炫，最令人印象深刻的是，它是一个非常有用的工具。这个徽章可以取代你手机上的谷歌认证器双因素认证应用，它是一个 USB 橡胶鸭子。也是徽章。今年徽章变得有用了吗？查看下面的视频，了解更多信息。

每年的这个时候，来自北美各地的硬件黑客都在忙于硬件和制造的演示工作。这是 badgelife，为拉斯维加斯的一个特殊周末制造定制可穿戴电子产品的庆典。从现在起大约一个月后，将有数以千计的独立徽章涌入拉斯维加斯的凯撒宫，配有 blinkies，定制芯片，创新的制造工艺，以及许多用玻璃纤维和阻焊膜渲染的模因。

 [https://www.youtube.com/embed/7PMtJVYy9Jc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7PMtJVYy9Jc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 徽章演变

[![](img/a23535472b34d09acc78db1d6415c1bd.png)](https://hackaday.com/wp-content/uploads/2018/06/memes.jpg)

This year’s Hacker Warehouse badge has support for this year’s independent add-ons.

当我们看一看去年的黑客仓库徽章时，这是你可以从独立 DEF CON 徽章中期待的一切。板上有一个 ESP8266，一堆小得惊人的 WS2812 RGB LEDs，以及一个 96×64 有机发光二极管，带有四个 d-pad 排列的按钮。这个软件很棒，它可以玩 Snake，还能检测 WiFi deauth 数据包。应该注意的是，DEF CON 的地板是地球上最恶劣的射频环境(尽管其原因更多的是 lulz 而不是实际的*威胁*，能够检测 WiFi deauth 数据包是非常非常有用的东西。

今年的徽章比去年的黑客仓库徽章有了显著的进步。代替 ESP8266，今年的徽章采用了置于独特 PCB 布局上的 ESP32，与徽章的设计相得益彰。迷你 WS2812s 仍然存在，有 8 Mb 的闪存存储，ATMega 32u4 提供 USB HID 功能。还包括两个“劣质附加”标题，[因为今年徽章有了自己的徽章](https://hackaday.com/2018/06/21/this-is-the-year-conference-badges-get-their-own-badges/)。

## 这个徽章很显眼

更好的芯片赋予这个徽章更多的功能。有了 ESP32，这个徽章可以监听 NTP 服务器，这意味着这个徽章知道时间。对于一个可以在小型有机发光二极管上玩 Snake 的徽章来说，这可能不是什么大事，但这个徽章也支持双因素认证(TOTP 和 HOTP)，并作为谷歌认证器。这本身就是一些惊人的功能，我们不记得在任何项目中看到过，基本上只是一个 ESP32 和有机发光二极管显示器。使用 ESP32，您还可以获得一台网络服务器，以及所有相关的乐趣。

这个徽章上还有一个支持 USB 的芯片。这是带 USB 的 ATMega32u4，这意味着这个徽章可以充当 HID 键盘和鼠标。它就像一个 USB 橡胶鸭子，一个击键注入工具，可以打开命令行，在控制台上输入任何内容。徽章接受 Ducky 脚本格式，所以你不用花 40 美元买一个看起来像 USB 拇指驱动器的东西，你可以多花一点钱买一些更时尚的东西。当你不想触发屏保时，它也可以作为鼠标抖动器。

这个徽章真的是一件艺术品。它是时尚，它是电子产品，结合了谷歌认证器、网络服务器和橡皮鸭功能，这是一个真正的工具，不会在 DEF CON 的供应商区出现。

你现在就可以在黑客仓库预订这些徽章，并在 DEF CON 期间发货。如果你不能参加，也可以选择在 CON 之后发货[。这也将是一个公开的徽章:](https://hackerwarehouse.com/product/hacker-warehouse-2018-electronic-badge-shipped/)[所有固件都已经可用](https://github.com/hackerwarehouse/HW-DC26-Badge)，硬件来源将在大会后公开

你是在做徽章还是附加品？我们很想听听，所以[给我们发个提示](mailto:tips@hackaday.com?subject=[Badges])。此外，Hackaday.io 是一个发布这些构建信息的好地方，我们已经[有一个巨大的会议徽章项目列表](https://hackaday.io/list/25935-conference-badges)！