# 拯救、修复和增强动力轮

> 原文：<https://hackaday.com/2016/11/14/power-wheels-rescued-restored-and-enhanced/>

动力轮似乎就像乐高——它们是一代一代传下来的。[Nicolas]在 1997 年收到了他的全新 Peg-Perego Montana 电动轮作为圣诞礼物。在谷仓里坐了十年，甚至卷入了一场洪水，现在是时候把它交给他的教子了，尽管不是没有一些修复和添加功能。他的网页有一个非常好的文章，只是没有包括图表，但你可以在下面找到一个缩写版本。

![The starting point](img/2e96a2a9bee5298c9be182786509a310.png)

The starting point

由于时间和洪水，它不仅需要一个新的油漆工作，一些塑料位恢复，但硬塑料轮必须清空水，整个线束需要更换，因为一些螺丝。幸运的是，变速箱和电机只需要清洁和新的油脂。

不管它是否需要，[Nicolas]想要添加一个 Teensy 2.0++作为大脑，因为他以前没有见过任何人这样做，这也让他可以重温他的 Arduino 技能(Teensy 与 Arduino 软件和库兼容)。

![Teensy board and speedometer LCD display](img/4b7fae2b58f2781eb1ae974d1413c6fb.png)

Teensy board and speedometer LCD display

他首先利用 Teensy 的一个新功能，一个安装在仪表板上的诺基亚 5110 液晶显示器的速度计。为了测量速度，他使用了一个红外二极管以及一个 NPN 晶体管、两个 LM324 运算放大器和一些其他部件。他甚至为 LCD 显示器绘制了一些非常漂亮的自定义图形。

他原本计划通过让 Teensy 对一个定制的 H 桥进行 PWM 来添加一个可变加速器，甚至走了一段相当长的路来实现它，但即使在 100% PWM 的情况下，速度也太慢了。由于当时只有一个不好的示波器用于调试，他放弃了 H 桥，转而使用继电器。

![Lights](img/4f1f251539a1baf8b06ae56ad138b469.png)

Lights

当谈到照明时，[Nicolas]全力以赴，在定制电路板上安装高强度白色和蓝色 led。他还不得不在网上彻底搜索灯罩，但幸运的是，那里有相当多的电动轮零件，尽管有些是他在垃圾场从一辆思域上买的。[Nicolas]在法国，阅读他寻找这些零件的经历，可以有趣地了解到在运费很容易超过零件成本的情况下，从美国买东西有多困难。我们可以理解为什么有时这根本不是一个选项。

另一个新功能是仪表板安装的收音机。随后是一个新的电池充电器，一些足以与许多汽车相媲美的保险丝，精心完成的油漆工作和许多标签和贴纸，表明这是一项充满激情的工作。我们确信他的教子们会喜欢他们比新的更好的动力轮。

 [![Engine compartment](img/112f333c234000641cf3f61e0ed10c5d.png "Engine compartment")](https://hackaday.com/2016/11/14/power-wheels-rescued-restored-and-enhanced/engine_compartment_img253_cr/) Engine compartment [![Restored Power Wheels](img/1f64e3aa0513212999388c99b3713ebe.png "Restored Power Wheels")](https://hackaday.com/2016/11/14/power-wheels-rescued-restored-and-enhanced/finished_power_wheels_img241/) Restored Power Wheels

请注意，Hackaday 对电动轮并不陌生。虽然[Nicolas']的本意是为他的教子们设计一辆安全的赛车，但我们已经看到他们以完全相反的方式进行了改装，其中的赛车只能在两个轮子上转弯。一些[比赛甚至有维修站工作人员](http://hackaday.com/2014/10/02/even-more-power-wheels-racers/)参与，并涉及带有来自福特 Fusion plugin hybrids 的[电池组的车辆。](http://hackaday.com/2014/09/30/the-chibi-mikuvan-or-a-power-wheels-with-a-ford-fusion-battery/)