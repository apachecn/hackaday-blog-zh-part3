# hack let 122–光谱仪

> 原文：<https://hackaday.com/2016/08/27/hacklet-122-spectrometers/>

当浏览 Hackaday.io 上的项目时，总会发现一些有趣的东西。我总是惊讶于黑客在地下室和家庭实验室中可以完成多少工作。我发现的一个令人惊讶的趋势是全球范围内人们正在从事的光谱仪项目的数量。我一直知道分光计是什么，但我从来不知道这么多黑客想要它们。尽管这些数字不会说谎——世界上许多黑客都想测量光的光谱——无论是测试一种新的 LED，还是确定一个物体的结构。本周我们在 [Hackaday.io](https://hackaday.io) 上查看一些最好的分光计项目！

[![ramanpi](img/7391211ad14de2dcfad3d931b2cf79f1.png)](https://hackaday.io/project/1279) 我们从【fl@C@】和[Raman pi–拉曼光谱仪](https://hackaday.io/project/1279)开始。RamanPi 是 Hackaday.io 上的首批光谱仪项目之一。[fl@C@]将他的项目纳入了 2014 年 Hackaday 奖，是 5 名决赛选手之一。顾名思义，ramanPi 是一种[拉曼光谱仪](https://en.wikipedia.org/wiki/Raman_spectroscopy)，化学中常用的一种类型。这台机器最初的用途是确定原子的键角。RamanPi 尽可能使用标准桌面打印机创建的 3D 打印零件。树莓派运行系统，最初是 B 型，但现在我确信 Pi 3 会符合要求。检测器是东芝线性 CCD。

[![dh-spec](img/df8a2c3c126ff5dd4fcb658c288f4724.png)](https://hackaday.io/project/12335) 接下来是【大卫 H 哈夫纳 Sr】带着 [DH 4.0 光谱仪 V 4(升级 2 )](https://hackaday.io/project/12335) 。[大卫的]项目在描述文本中没有给出很多背景知识——他直接进入了设计和建造分光计的技术细节。他的传感器是 JDEPC-OV04，这是一个用于笔记本电脑的网络摄像头模块。[大卫]最近的大部分工作都是在光路上进行的。分光计可以使用衍射光栅和狭缝将光分成光谱。[David]正在使用可记录 DVD 作为他的衍射光栅。这条缝更像是自制的。两个吉列剃须刀刀片和一个醋酸纤维条用于形成仅 0.11 毫米宽的光学狭缝。[大卫]已经用他的分光计分析原油。

[![pure-eng](img/068477c398058f6ea16026507a7f8f84.png)](https://hackaday.io/project/4141) 接下来我们有【纯工程】带 [C12666MA 微型光谱仪](https://hackaday.io/project/4141)。光电制造商 Hamamatsu 已经在一个指尖大小的罐子里创造了一个光学分光计。他们的 C12666MA 微型光谱仪听起来一定很神奇——的确如此。微电子机械系统(MEMS)的魔力让这种设备焕发了生机。然而，将这些设备中的一个带上来并不是一件容易的事情。[Pure Engineering]为 C12666MA 设计了分线板。他们甚至包括一个 404 纳米激光二极管和一个白色 LED 照明。该板可以插入标准 Arduino 接头。

[![adam](img/1369d3d5ff66f9c312977a83516172f8.png)](https://hackaday.io/project/12724) 最后，我们有【亚当】与[手持 VNIR 光谱仪](https://hackaday.io/project/12724)。在这种情况下，VNIR 代表可见光和近红外。[亚当]创造了这个装置，这样他就可以了解光谱仪是如何工作的。这是我听过的最崇高的目标。他正在构建一个便携的系统，这样他就可以在实验室之外进行测量。传感器是索尼 ILX511B 线性 CCD。Arduino nano 读取 CCD 并将数据传送到 PC 进行分析。【亚当的】衍射光栅是公共实验室的凹面全息东西。[Adam]还使用了从公共实验室购买的醋酸纤维狭缝。照明通过光纤束进入。

如果你想看更多的光谱仪项目，请查看我们新的[光谱仪项目列表](https://hackaday.io/list/13340-spectrometers)。看到一个我可能错过的项目？不要害羞，[在 Hackaday.io 上给我留言就行了](https://hackaday.io/adam)。这就是本周的 Hacklet，一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！

如果你想看更多的光谱仪项目，请查看我们新的[光谱仪项目列表](https://hackaday.io/list/13340-spectrometers)。看到一个我可能错过的项目？不要害羞，[在 Hackaday.io 上给我留言就行了](https://hackaday.io/adam)。这就是本周的 Hacklet，一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！