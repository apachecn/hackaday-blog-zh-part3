# 电路弯曲卡西欧 SK-1 得到一个 Arduino 大脑

> 原文：<https://hackaday.com/2018/02/05/circuit-bent-casio-sk-1-gets-an-arduino-brain/>

卡西欧 SK-1 键盘在“电路弯曲”领域相当有名，其简单的内部结构有助于以各种有趣的方式修改和调整设备的输出。但通过电路弯曲 SK-1 创作音乐可能会很乏味，因为它归结为盲目地摆弄内部，直到它听起来很酷。[尼克·普莱斯]想做一些更科学的东西，并决定尝试用 Arduino 取代他的 SK-1 的 ROM，这样他就可以完全控制它。

[![](img/0480f44bfc58a13e67dcb2e947b3c4e7.png)](https://hackaday.com/wp-content/uploads/2018/02/sk1_detail.jpg)

Replacing the ROM chip with header pins.

反正就是这个想法。现在他已经抛弃了 ROM，用 Arduino 代替它。不幸的是，由此产生的声音让人想起 56K 调制解调器在微波炉中烹饪的画面。显然[尼克]还有一些工作要做。

不过目前来看，进展已经足够引人入胜了。他能够从键盘上取出原来的 NEC 23C256 芯片，使用 Arduino 和他编写的一些代码读取其内容，[他甚至将转储文件放到网上](https://spun.io/wp-content/uploads/2018/02/sk1-rom-raw.zip)供其他 SK-1 黑客使用。然后，他为 Arduino 编写了一些新代码，以便在需要时将 rom 转储中的数据发送回键盘。理论上，它应该听起来和以前一样，但增加了“伪造”数据的能力，这些数据将返回键盘以发出新的声音。

结果就是你在休息后链接的视频中听到的。不完全是[尼克]想的那样。在与逻辑分析仪进行了一些窥探后，他认为问题在于 Arduino 不能像原来的 NEC 芯片那样快速响应。他现在得到了一个 NVRAM 芯片，以取代原来的 NEC 芯片；这个想法是，当他想摆弄声音时，他仍然可以使用 Arduino 重新编程 NVRAM 芯片。

我们在过去的中已经介绍过一些[非常奇特的弯曲电路乐器，但是如果你正在寻找更容易上手的乐器，我们在 2011 年](https://hackaday.com/2015/01/30/digitally-controlled-circuit-bending/)的旧时光[中运行了一个从头到尾的指南，这应该会有所帮助。](https://hackaday.com/2011/01/11/intro-to-circuit-bending/)

 [https://www.youtube.com/embed/0pExsDpxLyg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0pExsDpxLyg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

