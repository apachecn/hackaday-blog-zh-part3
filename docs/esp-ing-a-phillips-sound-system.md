# 使用飞利浦音响系统。

> 原文：<https://hackaday.com/2017/01/05/esp-ing-a-phillips-sound-system/>

把旧东西物化很酷。或者甚至是新的，离线的东西。这似乎是一种趋势。而且很性感。是的，它是。为什么人们要这样做，你可能会问:我们说为什么不呢？为什么烤面包机不能放在物联网上？还是钻床？或者收音机？是的，一台收音机。

Wummi 博士]刚刚为物联网添加了另一个设备，他称之为丁字裤互联网。这是一台[飞利浦 MCM205 微型音响系统](http://stuff.wummi.at/pages/espradio.php)收音机。他想让他的收音机自动化，但他最初的想法是建立一个带有红外 LED 的装置来远程控制它，但失败了。他将其归咎于“一些时髦的红外巫术”。因此，他决定采用基于 ESP8266 和 NodeMCU 的解决方案。 [ESP8266 红外遥控器在](https://hackaday.com/2016/09/16/smartphone-tv-remote-courtesy-of-homekit-and-esp8266/)之前就已经知道可以工作了，但也许这些还不是巫毒等级的。

打开收音机后，他很快发现实际的 AM/FM 收音机是一个独立的模块。制造商好心地在主板上留下了精美的针脚标签。标有 SCL/SDA 的引脚暗示 AM/FM 模块使用 I C。他通过 [Bus Pirate](http://store.hackaday.com/products/buspirate-v3-6-thm180c4m) 接入协议，很明显收音机在主 PCB 的某个地方有 EEPROM。一次搜索发现电路板中有一个 24C02 IC，这是一个 2K I C EEPROM。到目前为止还不错，但还有其他功能需要控制，比如音量或 CD 播放。为此，他计划接入前面的按钮旋钮。按钮有不同的电阻，并串联连接，因此它们在主板无线电 ADC 引脚上产生不同的电压。他试图用 NodeMCU 进行 PWM 来模拟这种情况，但就是不起作用。

具有讽刺意味的是，他意识到他可以接入红外接收器线，模拟一个红外代码直接发送到电线上。没有光的干扰，这次也没有“时髦的红外巫术”。

一些 Lua 行之后，无线电升级了 GET API，允许:

*   按下所有的按钮
*   设置任意调频频率
*   检查收音机是开着还是关着

让我们来看看它的实际应用:

 [https://www.youtube.com/embed/SBpCl1bxgc4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SBpCl1bxgc4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[感谢 gregor4005]