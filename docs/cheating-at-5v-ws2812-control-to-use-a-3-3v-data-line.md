# 在 5V 时欺骗 WS2812 控制使用 3.3V 数据

> 原文：<https://hackaday.com/2017/01/20/cheating-at-5v-ws2812-control-to-use-a-3-3v-data-line/>

如果你想使用运行在 3.3 伏的微控制器来控制 WS2812(或 neo pixel)led，你可能会遇到一些问题。数据手册告诉我们，在最小电压`0.7 * Vcc`时将检测到逻辑高输入。如果您在 5V 下运行 LED，这意味着 WS2812 将需要`5 V * 0.7 = 3.5 V`来检测数据线上的‘1’。虽然使用 3.3 V 可能不会有问题，但数据手册中的所有规格都是针对最差情况的，因此有可能会遇到可靠性问题。

所以通常我们会说“添加一个电平转换器将 3.3V 转换为 5V”，这篇文章就结束了。我们甚至有一整篇[关于建造电平移动器](http://hackaday.com/2016/12/05/taking-it-to-another-level-making-3-3v-and-5v-logic-communicate-with-level-shifters/)的文章，对于这种应用来说很好。然而，CrashSpace 的[todbot]想出了一个巧妙的方法，它需要更少的组件，却能确保可靠性。

![bigbutton-front-back](img/daea47910971564615da5126ffeccd7e.png)对于在[碰撞空间](https://blog.crashspace.org/)的[大按钮项目](https://todbot.com/blog/2017/01/12/crashspace-bigbutton-w-esp8266/),【tod bot】使用运行在 3.3 伏的 ESP8266 和运行在 5 伏的 WS2812 LEDs。为了执行电平转换，信号二极管与第一个 LED 的电源串联放置。这将第一个 LED 降至 4.3 V，这意味着可以使用`4.3 V * 0.7 = 3.01 V`信号来控制它。此 LED 的逻辑输出将为 4.3 V，这足以为其余以 5 V 运行的 LED 供电。

这个小技巧意味着用一个 3.3 V 微控制器控制 5v led 只需要一个二极管。第一个 LED 可能不太亮，因为它在较低的电压下工作，但这是[todbot]为了简化这种设计而做出的权衡。这是一个执行良好的项目的一小部分，所以一定要点击进入，享受[todbot]投入到一个伟大构建中的所有思想。