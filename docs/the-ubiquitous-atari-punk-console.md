# 无处不在的雅达利朋克游戏机

> 原文：<https://hackaday.com/2015/09/17/the-ubiquitous-atari-punk-console/>

雅达利朋克控制台(APC)是一个基于双 555(或单 556)的合成器。该电路由著名的(也有些声名狼藉的)福里斯特·米姆斯于 1980 年设计，最初被简单地命名为[“声音合成器”](http://web.media.mit.edu/~stefanm/HowTo/Electronics.html)，当被考斯蒂克机器公司重新命名为“雅达利朋克控制台”时，它最近变得更受欢迎。然而，该电路与雅达利 2600 没有太大关系，雅达利 2600】没有包含 555 定时器芯片。然而，我们假设 2600 产生了类似的故障方波音频输出。

[![a2](img/086af5ffe80c66dcf8628c9986757218.png)](https://hackaday.com/wp-content/uploads/2015/09/a2.jpg) 电路操作容易掌握，只用 9 个元件。这种设计和建造的简易性使得建筑商可以更专注于其建筑的美学，将其改造成有趣的、通常不太可能的外壳和系统。一个这样的黑客是“雅达利朋克桶”(如图所示)，APC 和一个简单的放大器被砍进一个生锈的旧桶。APC 与一个简单的放大器和再生扬声器一起建立在条形板上。[【法默·格林奇】](https://www.youtube.com/watch?v=9kpYrl5UQHU)在现场用它做道具，看起来和听起来都很棒。

[电子音乐论坛](http://electro-music.com/forum/viewtopic.php?t=17371)用户【dnny】在将整个东西塞进一个[灯泡](https://www.youtube.com/watch?v=yUUTSjfVZnU)之前，对电路进行了空中布线，并用光敏电阻替换了罐子。

 [![light_apc](img/34b30e8867e747f278fea507bedd8488.png "light_apc")](https://hackaday.com/2015/09/17/the-ubiquitous-atari-punk-console/light_apc-2/)  [![creepy](img/f83b2deaa5388c662a007af78929744f.png "creepy")](https://hackaday.com/2015/09/17/the-ubiquitous-atari-punk-console/creepy/) 

还被黑成了[游戏机，](https://www.youtube.com/watch?v=0uIFJ3VRBAU)变成了[“接触特雷门”](http://sinkhacks.com/vostok-i-contact-theremin-2/)(这里的可变电阻换成了一个[人形](https://www.youtube.com/watch?v=3sujuW7hxrE))，嵌入了[吉他踏板](https://www.youtube.com/watch?v=NndG0aCoBa8)，被卡进了令人不安的[雅达利朋克毛骨悚然玩偶](https://www.youtube.com/watch?v=QFZNXmDTiug)。

由于基本电路如此简单，它也为音序器项目提供了一个很好的构建模块，其中许多都是基于[“baby 10”音序器](http://sendling-info.blogspot.co.uk/2006/11/baby-10-sequencer.html)的设计。这些建筑给 APC 增加了一个新的维度，[听起来相当不错。](https://www.youtube.com/watch?v=Qe1ButmzNWY)

不知何故，在其原始出版物 35 年后，装甲运兵车奇怪的复古声音继续激发。为什么不试着自己造一辆 APC，然后找一个你自己的奇怪的外壳把它塞进去呢？

## 该电路

APC 是 555 的一个相对简单的应用，是初学者的好选择。555 也是无处不在的廉价零件(少量不到 10 美分)。完整的电路如下所示:

[![punk](img/e3819a565b250eca246bd8f83041a5cf.png)](https://hackaday.com/wp-content/uploads/2015/09/punk1.png)

该电路作为非稳态振荡器工作，驱动单稳态电路，稳定和单稳态电路均由 555 实现。不稳定电路与 [TI 数据表](http://www.ti.com/lit/ds/symlink/ne555.pdf)中显示的电路密切相关:

[![tidata](img/fa576d284b81469eb24acc69fafc67f6.png)](https://hackaday.com/wp-content/uploads/2015/09/tidata.png)

当 555 启动时，放电引脚(DISCH)实际上未连接。这允许电容器(C)通过 R [A] 和 R [B] 充电。555 使用 THRES 引脚检测电容器上的电压。当电压为电源电压的 2/3 时，555 允许电容器上的电压通过 R [B] 经由放电引脚放电。同时，555 将其输出引脚设置为低电平。当电容耗尽，电压降至电源电压的 1/3 以下时，TRIG 引脚会检测到这一情况，并将输出设为高电平，并“断开”放电引脚。这允许电容器再次充电，并且该过程重新开始产生振荡。在 APC R [中，]是一个可变电阻，可以控制充电速率，从而控制频率。

非稳态 555 输出一个固定的脉冲长度，在我的建设，这是大约 10 微秒。虽然这很好，如果连接到扬声器，会产生一个可听音，但 APC 增加了第二个单稳态电路。单稳态电路在输入脉冲时触发，保持输出一段时间，与输入脉冲长度无关。这允许 APCs 脉冲宽度变化。较长的脉冲似乎有助于驱动扬声器，但也对不稳定的输出频率有调节作用，因为多个脉冲可能被屏蔽。555 单稳态电路的操作与非稳态振荡器几乎相同，但是触发输入不连接到定时电容。这意味着电路不会“自触发”，而是需要一个输入(在这种情况下来自非稳态电路)。第二可变电阻器允许脉冲宽度变化。

虽然有许多套件可用，但使用一个 556 或两个 555 就可以轻松实现电路试验。如果你建造了一个有趣的 APC [让我们知道](http://hackaday.com/submit-a-tip/)！