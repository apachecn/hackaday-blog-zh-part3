# Neopixel 卧室时钟使用 ESP8266

> 原文：<https://hackaday.com/2016/04/09/neopixel-bedroom-clock-uses-esp8266/>

当[Vance]加入他当地的 hackspace 时，他寻找一个项目来利用他所掌握的新工具。他的解决方案是:[一个吸引人的 LED 彩色轮时钟，使用由 NTP 同步的 ESP8266](http://va.nce.me/neopixel_clock.html) 驱动的新像素。每个新像素通过磨砂漫射器照亮钟面的一部分，小时以红光显示，分钟以蓝光显示，秒钟以绿光显示。当每一种颜色通过另一种颜色时，它们被混合在一起，形成一个不断变化的色彩景观。使用 12 个新像素，整个时钟安装在激光切割外壳中。

在一块条板上完成最初的原型后，他在 KiCad 中创建了一个 PCB，并为 3.3v 调节器留出了空间。这个和源代码可以在项目的 GitHub 库上找到。

由此产生的时钟是一个非常高质量的建设，以及有吸引力和有用的权利本身。视频展示了色彩混合的效果，或者至少是青色和黄色的混合效果。

 [https://www.youtube.com/embed/3ScniT1N5sI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3ScniT1N5sI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们喜欢 Hackaday 的时钟，这些年来我们展示了很多时钟。看看光钟，我们重点介绍了这个[柏林钟](http://hackaday.com/2015/12/01/light-duty-timekeeping-arduino-berlin-clock/)和这个[斐波那契数列钟](http://hackaday.com/2015/05/07/fibonacci-clock-is-hard-to-read-looks-good/)，但是更接近这个项目精神的是制作这些页面的许多环形钟。有这个 [200 LED 环形时钟](http://hackaday.com/2014/06/24/the-200-led-ring-clock/)，这个巨大的[圆形 LED 时钟带一个互锁 PCB](http://hackaday.com/2014/05/05/huge-rgb-ring-light-clock/) ，更接近【万斯】的时钟[，另一个 ESP8266 环形时钟设计](http://hackaday.com/2015/12/05/light-up-your-day-with-this-led-clock/)。

[via[rLab–阅读黑客空间](http://rlab.org.uk/)