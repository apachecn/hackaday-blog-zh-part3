# 用松弛度控制空调

> 原文：<https://hackaday.com/2017/08/23/control-the-air-conditioning-with-slack/>

[Raphael Baron]需要一种更好的方法来控制办公室的空调设备。当然，他们有遥控器，但那太简单了。[Raphael]想出了一个[解决方案，它使用了一个 ESP8266、一台计算机、红外 led 和一个在 Slack 上运行的机器人](http://rbaron.net/blog/2017/08/05/A-Slack-bot-for-controlling-the-offices-ac.html)。

[Raphael]在 protoboard 上构建了一个 ESP8266 硬件原型，并使用它来读取和记录来自遥控器的红外信号。一旦他解决了他正在使用的 IR 库的问题，他就可以用它向 AC 单元发送 IR 命令。由于他们的办公室有两个交流单元，[Raphael]制作了第二个原型，它有两个红外发光二极管，但没有红外接收器。利用这个，他可以打开和关闭两个空调设备，并设置它们的温度。

对于服务器，[Raphael]转向 Clojure，这是 Lisp 的一种方言，它提供了对 Java 框架的简单访问，主要是为了练习使用这种语言。服务器的主要职责是使用 Slack 的实时 API 来监听来自 Slack bot 的消息，并将它们转发给 ESP。通过这种方式，与 Slack bot 交谈的用户可以向其发送消息，服务器将这些消息转发给微控制器，微控制器进而解析这些消息，并向 AC 单元发送 IR 命令。

[Raphael]承认这不是最先进、最专业的东西，但没关系。GitHub 上提供了 ESP8266 板的原理图以及 ESP 板和服务器的代码。似乎有很多黑客使用 Slack，比如这个由 Slack 机器人控制的 NERF 炮塔。或者[这个点唱机](https://hackaday.com/2017/06/02/hackerspace-jukebox/)，用户可以通过与 Slack 机器人对话来与之互动。