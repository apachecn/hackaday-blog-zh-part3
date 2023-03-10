# Hackaday 获奖作品:智能手机盲文键盘

> 原文：<https://hackaday.com/2017/06/29/hackaday-prize-entry-a-braille-keypad-for-smartphone/>

[Vijay]的智能手机盲文键盘有几个突出之处。一个是最终结果的计划如何符合人体工程学，坐在智能手机的背面，这样你就可以像平常一样握着手机。另一个原因是，它可以像任何其他 USB 键盘一样插入。最后一个应该会让任何 vi 用户微笑——你不需要移动手指来打字。你只需按下手指下已有的按钮组合。

它由一个带有 AtMega32U4 的定制电路板、一个 16 MHz 振荡器、一个微型 USB 连接器和八个按钮开关组成。AtMega32U4 允许他使用 [Arduino HID 库](https://www.arduino.cc/en/Reference/HID)。将盲文按钮组合映射到按键后，HID 库通过 USB-OTG 电缆将键值发送到智能手机，让智能手机接受它们，就好像它们来自普通的即插即用键盘一样。

我们必须赞扬[Vishay]对有盲文经验的盲人进行测试。例如，他了解到，如果用户按下代表“b”的[Dots 1 2],然后按下代表“c”的[Dots 1 4],他们更愿意不将手指从两个字符之间的 1 上移开，以便更快地打字。他还了解到电池管理是有问题的，这可能是为什么他后来放弃了蓝牙通信的选择，只留下 USB，从而消除了对电池的需求。

[Vijay]的项目入围了有用物联网 Hackaday 奖的决赛，我们渴望看到最终的结果是什么样的。但与此同时，看看他的 [hackaday.io](https://hackaday.io/project/21175-tipo-braille-smartphone-keypad) 和 [GitHub](https://github.com/lyle963/Tipo) 页面，看看下面他正在使用的键盘的一次迭代的视频。

盲文设备似乎每年都会出现在黑客日奖中。例如，[海顿·琼斯]进入了一台[盲文印刷机](http://hackaday.com/2017/06/12/hackaday-prize-entry-compact-braille-printing-press/)，去年[马达翁]进入了一台[模块化盲文显示器](http://hackaday.com/2016/07/09/hackaday-prize-entry-modular-low-cost-braille-display/)，它使用 DIY 微型螺线管来升高和降低圆点。

 [https://www.youtube.com/embed/9KrF9IJwGso?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9KrF9IJwGso?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)