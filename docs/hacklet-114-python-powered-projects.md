# hacklet 114–Python 支持的项目

> 原文：<https://hackaday.com/2016/07/02/hacklet-114-python-powered-projects/>

Python 是当今最流行的编程语言之一。它真的把“派”放在了树莓派里。Python 的历史可以追溯到 20 世纪 80 年代末，当时它是由吉多·范·罗苏姆首次编写的。[Rossum]在 1989 年圣诞节期间创建了 Python 作为业余爱好项目。他想要一种对 Unix/C 黑客有吸引力的语言。我得说他在这方面相当成功。黑客们接受了 Python，使其成为他们项目中的首选。本周的 Hacklet 聚焦于 [Hackaday.io](https://hackaday.io) 上一些最好的基于 Python 的项目。

[![pytool](img/58a13f00e360c4a4235a91a7d91b39d6.png)](https://hackaday.io/project/5971) 我们先从【Jithin】和 [Python 驱动的科学仪器工具](https://hackaday.io/project/5971)说起，他是 2015 年 Hackaday 奖的参赛作品。[Jithin]创造了一个“盒子里的电子实验室”式的工具，可以与标价数千美元的商业产品竞争。Python 驱动的科学仪器工具使用简单的微控制器驱动的硬件来创建可编程增益放大器、波形发生器、LCR 计、CC 源等。微控制器处理所有实时操作。数据处理在运行 Python 脚本的连接 PC 上进行。Scipy 等流行的 Python 库使信号处理和波形显示变得简单。

[![pymusic](img/6e3a3104111b5d8956a3eaf1cc5ab405.png)](https://hackaday.io/project/9097) 接下来是【比尔·皮特森】和[詹皮](https://hackaday.io/project/9097)。[Bill]喜欢他的音乐键盘，但讨厌带着笔记本电脑、音频接口和所有相关的电缆到处走。他需要一个像基于 PC 的合成器一样灵活，但又像 MIDI 声音模块一样简单紧凑的设备。JamPi 做了所有这些，甚至更多。[Bill]正在使用 [fluidsynth](http://www.fluidsynth.org/) 产生声音。在 fluidsynth.py 模块的帮助下，在 Python 中处理控制和接口软件。所有这些功能都包含在一个带有 2 行字符 LCD 的简单盒子中。现在[比尔]随时随地都可以即兴演奏。

[![openmv-feature](img/fab7371670b01244bcdb9a7a0f75b4b6.png)](https://hackaday.io/project/1313) 接下来是【i.abdalkader】与 [OpenMV](https://hackaday.io/project/1313) ，他的参赛作品在 2014 年 Hackaday 奖。[I . abdalkader]的目标是创造“机器视觉的 Arduino”。他正在努力实现这一目标。2015 年，OpenMV 曾有过一次成功的 Kickstarter 战役。在经历了一些制造故障后，客户现在可以收到他们的设备了。OpenMV 是一种基于 Python 的低成本机器视觉设备。耦合到简单图像传感器的 ARM 微控制器构成了该设备的核心。在 OpenMV 团队创建的许多图像处理库的帮助下，相机是用 MicroPython 编程的。[i.abdalkader]甚至用 Glade 和 PyGTK 创建了自己的 IDE。

[![pyface](img/a4cb7432e93d82c4a7a020c052795549.png)](https://hackaday.io/project/11607) 最后我们有了【osannolik】配[校准和测量工具](https://hackaday.io/project/11607)。您是否曾经想要显示嵌入式项目中的一些调试参数，但是没有显示空间(或者根本没有显示)？在不退出 JTAG 设置和启动调试器的情况下更改参数怎么样？[Osannolik]创建了一个简单的 Python 驱动的基于 PC 的前端，可以用作开发嵌入式系统的瑞士军刀。变量可以实时显示，参数改变。由于 pyqtgraph，甚至可以使用图表。

如果您想要更多 Python 驱动的好处，请查看我们新的 [Python 驱动的项目列表](https://hackaday.io/list/12494-python-powered-projects)！我错过你的项目了吗？不要害羞，[在 Hackaday.io 上给我留言就行了](https://hackaday.io/adam)。这就是本周的 Hacklet。一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！