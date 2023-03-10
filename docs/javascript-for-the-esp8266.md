# ESP8266 的 JavaScript

> 原文：<https://hackaday.com/2015/09/27/javascript-for-the-esp8266/>

ESP8266 是一款流行的 WiFi 芯片，在微控制器的 TX 和 RX 引脚与 WiFi 网络之间提供相对透明的连接。它是一年多前发布的，从那时起，开发人员和硬件黑客已经将 ESP 变成了一个不仅仅是串行到 WiFi 的桥梁。它本身是一个微控制器平台，具有真实的开发环境和对脚本语言 Lua 的支持。

Lua 还不错，但是真正的赢家是这个微型 WiFi 平台的 JavaScript 解释器。这花费了数月的工作，[但是终于有了一个可用于 ESP8266](http://forum.espruino.com/conversations/266886/?offset=75) 的 JavaScript 开源版本。

这个构建基于 [Espruino 固件](https://github.com/espruino/Espruino)，一个用于微控制器的 JavaScript 解释器。该解释器运行在数十种不同的微控制器上，但作为最新、最棒、最受欢迎的新型微控制器平台，意味着 ESP 的新解决方案非常非常令人兴奋。

目前，ESP 的 JS 解释器正在测试中，人们对所有东西都将被移植到 Espruino 固件的主要分支中抱有很高的期望。这里有运行在 ESP 上的 JavaScript [的示例](https://github.com/esp8266-espruino/esp8266-espurino/wiki/07-Samples)，以及可以刷新到 ESP [上的二进制文件](https://github.com/esp8266-espruino/binaries)。

感谢[Richard]发送这封邮件。他已经在 ESP8266 社区论坛上建立了一个 Espruino 板，最终将会充满在 ESP 上运行的 JavaScript 的新例子。