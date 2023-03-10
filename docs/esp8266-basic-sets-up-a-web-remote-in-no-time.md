# ESP8266 BASIC 可立即设置网络遥控器

> 原文：<https://hackaday.com/2017/02/19/esp8266-basic-sets-up-a-web-remote-in-no-time/>

具有讽刺意味的是，我们自己的物联网的症结之一是互联网部分。我们愉快地构建硬件，但当需要编写 web 前端来驱动它时，兴奋感就消失了，项目只完成了一半。

将一些简单的基于 web 的脚本功能与微控制器基础知识结合在一起是 ESP8266 BASIC 最聪明的一招。BASIC 作者[mmiscool]在这个简短的演示中很好地利用了它:[一个通过 web 界面](https://www.instructables.com/id/Easiest-ESP8266-Learning-IR-Remote-Control-Via-WIF/?ALLSTEPS)驱动的完整的学习型 IR 遥控器，只用几行 BASIC 语言编写。

请注意，这里的一切都发生在 ESP8266 内部，从托管网页到解释，然后闪烁出 IR LED 代码来控制遥控器。这是一个复杂的“hello world ”,是让你入门的最低要求。界面可以看起来更光滑，红外遥控器可以通过更多的电流增加其范围，但这将涉及到添加一个晶体管和一些电阻，使零件数量增加一倍。

不过，对于大约 10 美元的零件，这是对 ESP 和 BASIC 的有趣介绍。其他的例子更简单，但是我们认为这个项目有一个很棒的/努力的比率，很难被超越。