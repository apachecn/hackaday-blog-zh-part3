# 迪卡比特:或者不是阴谋论

> 原文：<https://hackaday.com/2016/12/06/decabit-or-the-conspiracy-theory-that-wasnt/>

[LDX]第一次注意到他的吊扇发出奇怪的声音，有规律地，每小时或半小时。然后他注意到灯也在闪烁。他意识到有事发生，于是[建造了一个测井电力线监视器](https://hackaday.io/project/18619-investigating-ac-noise),看看他是否能解码这些模糊的信号，并弄清楚通过电力线传输的是什么神秘的信息。很自然，他怀疑光明会是幕后黑手。

即使你不容易胡思乱想，你也可能想要跟踪你的电力线，因为它可以作为项目的[准确的长期时基，或者因为它可以告诉你一些关于电网](http://hackaday.com/2015/07/01/embed-with-elliot-we-dont-need-no-stinkin-rtcs/)整体健康状况的[。](http://hackaday.com/2013/12/12/mains-frequency-display/)

[![3696681480306491308](img/e71eae7d691b81b074bb4dcd23f29eb5.png)](https://hackaday.com/wp-content/uploads/2016/11/3696681480306491308.png)【LDX】电路简单得不能再简单。一个 10 伏的交流变压器将主电源降低到一个合理的水平。一个电阻分压器将其进一步削减至 Arduino 能够处理的范围，然后另一个分压器将信号偏置至 Arduino 的 ADC 中点。正负 10 V 信号因此在 0 和 5 V 之间摆动。

剧透！在确认电力线频率上叠加了一个更高频率的波动后，他~~联系了他在丹佛~~的电力公司的人。从一个叫[丹佛]的人那里得到了一个关于他的项目的建议。该系统名为 Decabit，用于控制路灯、热水锅炉和其他公共基础设施，这些设施可能希望在电力便宜或天黑时协调运行。他链接的 [PDF 解释了这一切](http://www.elec.uow.edu.au/apqrc/content/technotes/UOW019_Tech%20Note%2014_AW_screen.pdf)，所以你可以把锡纸帽摘下来了。
但是我们仍然认为调查电力线是一个有趣的项目。谁知道其他人会发现什么？振作起来！