# 通过 Wi-Fi 控制将您的办公室空调带入 21 世纪

> 原文：<https://hackaday.com/2017/10/03/drag-your-office-aircon-into-the-21st-century-with-wi-fi-control/>

我们都曾在有空调的办公室里工作过，但有点太多了。在大热天走进有空调的舒适凉爽的办公室是一件美妙的事情，但是在一两个小时的寒风之后，你穿着夏装瑟瑟发抖，皮肤也变得干巴巴的。与此同时，在大楼的另一边，市场部的 Ted 已经将整个系统发挥到了极致，因为他的新陈代谢很快，他的办公室处于正午阳光的强烈照射下。

如果单个的空调机组可以很容易控制，那不是很好吗？为此，[Maya Posch]制作了一个设计相当不错的电路板，它采用了一个带有 ESP8266 处理器的 NodeMCU 电路板，[使用其四个输出作为 PWM，通过滤波器和运算放大器产生 0-10 伏模拟输出，以控制各个单元](https://hackaday.io/project/27548-wifi-ac-controller)。此外，还有一个车载 CO2 传感器和一个温度传感器，以及一个外部温度传感器。整个装置非常适合一个标准的电源插座外壳。

在软件方面，该系统使用 [Sming 框架](https://github.com/SmingHub)提供与后端服务器的 MQTT 通信，允许用户控制他们的空调体验。这是一项正在进行的工作，所以软件还没有发布。(提示，[玛雅]，提示！)虽然整个项目是一个非常整洁的构建，事实上，它是一个你会从高质量商业产品中期待的美的标准。这是在软件发布前我们的特色，这是一个值得关注的问题，因为像这样的质量不是每天都有的。

这不是我们带给你的第一个空调控制器，看看这个通过松弛控制的控制器。