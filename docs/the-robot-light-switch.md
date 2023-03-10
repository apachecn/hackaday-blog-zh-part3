# 机器人灯开关

> 原文：<https://hackaday.com/2015/11/06/the-robot-light-switch/>

让你的家自动化是一项了不起的努力——但是如果你不知道你在做什么，玩交流电源可能是一件危险的事情。那么，为什么不谨慎行事，利用你的电灯开关呢？

诚然，这并不是因为[泰勒·布莱奇]不想直接和 AC 乱搞，而是出于必要。你看，他刚刚搬进一个新办公室，他的“智能”空调…在晚上不会自动关闭。

> 有一个遥控器可以设定目标温度，但是这个装置不够智能，不能在晚上关闭。相反，有一个物理墙壁开关，这样你就可以像野蛮人一样用你实际的手来关闭它。

拒绝做一个野蛮人(和工作到很晚)，他决定通过建立一个伺服驱动的光开关板来简化问题。这不是最漂亮的——但确实有用。

他在 Thingiverse 中设计了[支架来安装一个标准的 9g 伺服电机来完成翻转。Arduino Nano 控制它，但由于你只需要一个输出引脚来运行伺服，你可以很容易地使用 ESP8266。他接着添加了一个小有机发光二极管屏幕和几个按钮——他用这个作为定时器来控制空调设备，但这是在乞求一个网络仪表板，对吗？](http://www.thingiverse.com/thing:1111962)

 [https://www.youtube.com/embed/MVAaZy_-zt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MVAaZy_-zt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



或者，[你可以使用 Raspberry Pi 直接使用 AC](http://hackaday.com/2015/02/11/wifi-controlled-power-outlets-with-raspberry-pi/),但是你应该拥有你计划“升级”的地方。