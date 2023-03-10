# ESP8266 派对按钮的演变

> 原文：<https://hackaday.com/2018/03/28/evolution-of-the-esp8266-party-button/>

有时候，建造一件东西最好的部分是在更远的地方重新建造它。不要告诉任何人，但有时当我们开始一个项目时，我们甚至不知道结束会在哪里。这是一个起点，而不是终点。当你可以做两次的时候，谁愿意做一次呢？甚至可能是三次？

[![](img/1aece287628446480e6a5f5852dbb947.png)](https://hackaday.com/wp-content/uploads/2018/03/partybttn_detail.jpg)

Original version of the Party Button

当[Ryan]决定为他的孩子制作一个无线“派对按钮”时，就发生了这样的事情。连接到他的家庭助理自动化系统，一个按钮的味道在整个房子里播放音乐，并开始改变他的飞利浦色调灯的颜色。他的初始版本工作得足够好，但在休息后的视频中，他将这个一次性的小工具演变成一个通用的物联网接口，他可以用于其他项目。

总的想法非常简单，设备顶部的大物理按钮重置内部的 ESP8266，它被编程为连接到他的家庭 WiFi，并向他的 MQTT 服务器发送信号。在按钮的早期版本中，有相当多的支持电子设备来处理将按钮的瞬时动作转换为 ESP8266 的“硬”电源控制。[但是随着设计的进展](http://onryansdesk.com/display/NOT/Party+Button+v2),【Ryan】意识到他可以在 ESP8266 发出信号后让它进入深度睡眠，只需使用开关来触发芯片上的复位。

新版按钮的其他改进包括从碱性 AA 电池切换到可充电的锂离子电池组，甚至切换到裸露的 ESP8266，而不是他在第一次迭代中使用的 NodeMCU 开发板。

如果想用 ESP8266 体验 MQTT 家庭自动化，请查看这个[自动车库门控制系统](http://hackaday.com/2018/01/21/esp8266-beacon-announces-your-arrival/)。如果按下按钮引发派对的想法让你浮想联翩，[我们也看到了这种想法的一些精心制作的版本](https://hackaday.com/2011/10/31/salvaged-flight-stick-controls-av-system-triggers-emergency-party-system/)。

 [https://www.youtube.com/embed/itArtoHZlws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/itArtoHZlws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

