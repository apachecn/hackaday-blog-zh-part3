# 对你的茶壶来说太多了

> 原文：<https://hackaday.com/2017/03/09/a-little-iot-for-your-pid-tea-kettle/>

对于一些人来说，茶是一种简单的享受——烧开水，泡上茶，享受。然而，对有些人来说，喝茶是一种神圣的仪式，他们要求的精确温度控制只需要最好的水加热技术。还有一些人更进一步，将[一个 PID 控制的电茶壶，一个集成了亚马逊 Echo 的物联网设备](https://hackaday.io/project/20217-iotea-kettle)。

任何值得做的事情都不值得过度,[luma]为此得分。在 RadioShack 电子学习实验室对他的设计进行了早期迭代，这也是额外的加分——这是一个由 [Forrest Mims](http://hackaday.com/2017/01/18/forrest-mims-radio-shack-and-the-notebooks-that-launched-a-thousand-careers/) 编写的手册。[luma]开始使用带有 Zigbee 屏蔽的 Arduino，但意识到最终的电路必须位于外部外壳中。切换到 ESP8266，整个封装——包括光隔离器、继电器和一个小型壁式电源——小到足以放入水壶底座。最终结果是一个 MQTT 设备将它的状态发布到他的 SmartThings 家庭自动化系统，现在当他告诉 Alexa 该喝茶了时，它会做出响应。

破解咖啡因手段的项目对 Hackaday 来说并不陌生，无论你的首选载体是[茶](https://hackaday.com/2016/08/20/hacklet-121-tea-hacks/)、[咖啡](https://hackaday.com/2017/01/06/alexa-robot-coffee-maker-brews-coffee-speaks-for-itself/)，甚至是[纯咖啡](https://hackaday.com/2012/01/01/making-pure-caffeine-at-home/)。

 [https://www.youtube.com/embed/K4PnNO5ktlI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K4PnNO5ktlI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

