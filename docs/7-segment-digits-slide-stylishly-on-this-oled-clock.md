# 7 段数字在这款有机发光二极管时钟上时尚地滑动

> 原文：<https://hackaday.com/2017/10/02/7-segment-digits-slide-stylishly-on-this-oled-clock/>

在 Sparkfun 上，[Alex]分享了一个目前正在进行的[有机发光二极管时钟项目](https://www.sparkfun.com/news/2484)，但是有一些有趣的变化。首先是每个数字都使用了一个小的有机发光二极管屏幕,[Alex]为其添加了一点风格。通过让分段以平滑的动画动作垂直滑动来过渡数字。这是一个吸引人的效果，代码可以在他的 [github 库](https://github.com/awende/OLED_Clock)上找到，任何人都可以尝试。

[Alex]还发现，通过使用 ESP32 微控制器并通过 NTP over WiFi 同步时钟，在硬件中实现实时时钟的额外成本变得没有必要。如果没有 RTC，时间每天都会漂移几秒钟，并且需要重置。目前，时钟需要 SSID 和密码被硬编码，但是[Alex]更愿意允许通过网页来配置，并且可以使用一些帮助。如果您已经在 ESP32 上实现了 web 服务器，[Alex]想知道您是如何处理多个页面的。“在整个构建过程中，我一直在为如何完成这件事而挠头，”他写道。“在 ESP8266 上，有`on(const String &uri, handler function)`，但在 ESP32 上似乎已经被删除了。”如果你能给亚历克斯指出正确的方向，一定要说出来。

有机发光二极管的显示器和时钟经常搭配在一起，就像我们在像 [DIY 有机发光二极管智能手表](https://hackaday.com/2014/07/07/diy-oled-smart-watch/)这样的项目中看到的那样，但是很高兴看到有人利用有机发光二极管的优势为一个平淡无奇的显示器添加一些视觉天赋。