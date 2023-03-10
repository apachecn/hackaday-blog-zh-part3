# SDR 和 Node.js 遥控怪物漂移

> 原文：<https://hackaday.com/2017/01/30/sdr-and-node-js-remote-controlled-monster-drift/>

大多数老派遥控汽车在 27 兆赫广播他们的控制。一些软件定义无线电(SDR)单元的价格会低到这个水平。剩下的，正如我们硬件人员喜欢说的，就是简单的编码问题。

所以[沃森]真的做了编码，这是值得称赞的。他的 [monster drift](https://github.com/watson/monster-drift) 项目从基础开始——正确频率的正弦波和余弦波——并在正确的持续时间内将它们组合起来，以输出到 SDR，在这种情况下是一个 [HackRF](http://hackaday.com/2013/08/01/hackrf-or-playing-from-30-mhz-to-6-ghz/) 。看着他按下回车键时脸上的笑容，汽车驶出了一张史诗般的 180 号办公桌(视频嵌入下方)。

如果 JavaScript 是你的东西，你应该看看这个项目。它使用 [node-hackrf](https://github.com/mappum/node-hackrf) 库与 SDR 通信，看起来非常简单。为什么让 C 编码的人享受所有的乐趣呢？今天就开始编写你自己的遥控汽车操纵脚本吧！

 [https://www.youtube.com/embed/XtUH5GbOzug?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XtUH5GbOzug?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

