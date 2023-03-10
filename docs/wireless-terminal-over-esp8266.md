# ESP8266 上的无线终端

> 原文：<https://hackaday.com/2017/05/15/wireless-terminal-over-esp8266/>

从调试信息到基本的“hello world ”,串行通信都是通过三根小电线完成的。现在想象一下，您可以切断下一个微控制器项目的电源线，并将您的手机用作 VT100 终端。这是[ondřej·赫鲁什卡]的[无线终端项目](https://www.ondrovo.com/a/20170316-esp-terminal/)的前提，他拿着一台 ESP8266，添加了一个可以通过 WiFi 访问的浏览器内终端仿真器。最终硬件使用安装在试验板适配器顶部的 ESP-01 模块，带有 3.3V LDO、引脚保护电路和欠压禁用功能。

固件基于[SpriteTM]的 [libesphttpd 代码](https://github.com/MightyPork/libesphttpd)，该代码经过修改后包含了 VT100 转义序列解析器。反过来，解析器被编码为状态机，并使用 [Ragel](https://www.colm.net/open-source/ragel/) 进行编译，这极大地简化了此类项目。当您访问微型网络服务器时，加载的网页开始通过网络套接字与 ESP-01 通信。来自终端的按键被发送到缓冲区，并到达解析器和控制逻辑。然后，这些字符以 115200bps 的速度传递到硬件 UART 线路，如果检测到转义序列，则执行相应的操作。

[ondřej·赫鲁什卡]分享了[代码](https://github.com/MightyPork/esp-vt100-firmware)以及 PDF 格式的[用户手册](https://www.ondrovo.com/a/20170316-esp-terminal/espterm-interfacing_2017-03-02.pdf)，供任何想尝试并帮助改进项目的人使用。通过[学习状态机](http://hackaday.com/2015/08/13/becoming-a-state-machine-design-mastermind/)的一点启发，你也可以将这个项目扩展到你自己的用例中。

谢谢你的提示