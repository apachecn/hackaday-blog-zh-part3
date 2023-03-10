# 让 LED 灯泡变得更加智能

> 原文：<https://hackaday.com/2018/05/05/giving-an-led-bulb-some-smarts/>

你的项目中有多少是纯粹出于无聊的白日梦？由于没有更有成效的事情可做，[dantheflipman]将沃尔玛的标准 LED 灯泡改装成了智能灯泡。

拆开后，他们将电线焊接到螺纹插座上，并为 Hi-Link hlk-pm01 电源模块添加了一个连接器。输出上限为 5 V 和 600 mA，但谁说这将是探照灯？一个威莫斯 D1 迷你克隆体在电源模块旁边滑动得很好，叠在上面的是一个新像素宝石 7。[dantheflipman]承认他还没有在宝石前增加一个电容器，所以我们将看看 led 能持续多久。重新组装后，灯泡通过原型 Blynk 应用程序控制。好到可以快速破解。

[dantheflipman]坦率地谈到了干扰电源电压的问题:除非你完全知道自己在做什么，否则不要这么做。在这种情况下，他已经注意到他们的焊接和环氧树脂所有的电线和焊点，以确保没有任何东西会松动和短路，一个“压力测试”即将到来。

无论你怎么看，智能灯泡都很酷，所以对智能灯泡如何工作的多一点[了解](https://hackaday.com/2017/02/06/reverse-engineering-ikeas-new-smart-bulbs/)一些进入黑客攻击的[细节](https://hackaday.com/2018/01/11/esp32-makes-not-so-smart-lights-smart/)可能会满足你对知识的渴望。

[通过 [/r/arduino](https://www.reddit.com/r/arduino/comments/8eww6n/walmart_led_bulb_to_smart_bulb_with_esp8266_wemos/)