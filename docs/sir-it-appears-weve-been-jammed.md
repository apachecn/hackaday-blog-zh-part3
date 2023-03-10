# 长官，我们好像被卡住了！

> 原文：<https://hackaday.com/2017/03/30/sir-it-appears-weve-been-jammed/>

[Kedar Nimbalkar]重新制作了 Instructables 用户 spacehun 的版本 [WiFi 干扰器](https://github.com/spacehuhn/esp8266_deauther)，它带有一些功能，肯定会让激怒它的人感到沮丧。

![](img/7d28d8fe0f3c38857d173d355d4cf038.png)干扰器是一个 ESP8266 开发板，运行一些额外的自定义代码，通过手机访问和控制。通过该界面，[Nimbalkar]能够锁定 WiFi 网络，并通过解除验证将所有设备从网络中引导出来。另一种方法是用伪造的 SSIDs 淹没空域，使连接到一个有效的网络成为一件旷日持久的事情。

在你居住的地方，这种信号中断几乎肯定是非法的。它不会造成永久性损害，但会再次引发现有的 deauth 漏洞和 SSID 漏洞。[Nimbalkar]的目的是为了教育和强调 802.11 WiFi 协议中的弱点。802.11w 标准应该通过使用受保护的帧来缓解我们的一些伪 deauth 问题。一旦设备在网络上通过认证，它就能够检测出伪造的 deauth 数据包。

我们展示了这种黑客攻击的一个更有针对性的版本，可以使用 PC 来完成— [甚至针对它自己](http://hackaday.com/2011/10/04/wifi-jamming-via-deauthentication-packets/)！最近有一个版本可以通过[跳到 ACK](http://hackaday.com/2017/02/03/jamming-wifi-by-jumping-on-the-ack/) 上来瞄准特定的设备。

 [https://www.youtube.com/embed/N5JVQ-m5Kd0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/N5JVQ-m5Kd0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[A previous version of this post wrongly attributed credit to Kedar Nimbalkar for creating the device, when in actual fact credit goes to [spacehun](https://github.com/spacehuhn)]

【谢谢提示，意泰！]