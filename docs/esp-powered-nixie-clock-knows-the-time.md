# ESP 供电的谢妮时钟知道时间

> 原文：<https://hackaday.com/2017/11/10/esp-powered-nixie-clock-knows-the-time/>

在 Hackaday，我们看到了太多的谢妮时钟，很高兴能遇到一个具有一些巧妙功能的时钟。[VGC]设计了他的[数码管时钟](https://hackaday.io/project/25114-nixie-clock-on-esp8266-module),以使用最少的能量运行:它只需要通过 USB 5V 的电压就可以工作，消耗仅仅 200 mA。Nixies 需要苏联批准的 180v 来触发，所以[VGC]使用动态指示和升压转换器来运行它们，用 74141 谢妮解码器来完成繁重的工作。

该项目的大脑是一个 ESP8266，它可以自动连接到他家的 WiFi。时钟只需拨入 NTP 服务器并设置自己的时间，因此不需要 RTC。它还可以通过电报与云通信，允许时钟向[VGC]的设备发送警报。ESP 的固件同样可以通过 WiFi 更新。3D 打印的表壳和闪烁的秒针指示器是时钟功能的完美点缀。

正如我们所说，从[手表](https://hackaday.com/2017/01/20/plus-size-watch-with-a-pair-of-tiny-nixies/)到[仪表盘转速表](https://hackaday.com/2017/07/29/nixie-tachometer-displays-in-style/)的所有东西都使用数码管来显示——我们喜欢那些老式的电子管！

 [https://www.youtube.com/embed/xMENl978gz0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xMENl978gz0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

