# 一个命令行步进程序库，具有所有的虚饰

> 原文：<https://hackaday.com/2017/03/05/a-command-line-stepper-library-with-all-the-frills/>

当你已经确切地知道你希望你的马达在哪里以及如何运转时，一个代码-编译-刷新-运行-调试的循环可以很好地工作。但是如果你想用步进电机在 T1 周围玩游戏，没有什么比现场界面更好的了。[【布伦丹】的 RDL](http://forum.arduino.cc/index.php?topic=459096) 是一个通用的步进电机驱动环境，你可以把它闪入 Arduino。RDL 通过串口与你的电脑或手机对话，并能命令步进驱动器 IC 以三种模式移动电机:旋转、圆周分割和线性。(因此有了这个缩写名。)最棒的是，整个系统是交互式的。下面来看看[的视频](https://www.youtube.com/watch?v=Lm8oprDhAnQ)。

这个软件有相当多的功能。键入“？”给你一个命令列表，输入“@”告诉你电机认为它在哪里，输入“h”将电机移回原位。轮流旋转，旋转度数，或者旋转到一个特定的位置都很简单。它还可以从模拟操纵杆读取数据，该操纵杆将实时控制向前和向后的旋转速度。

分割模式将馅饼分割成许多片，马达旋转到这些特定的位置。例如，12 或 60 个除法给你一个时钟。加速和减速曲线是内置的，但可以调整。您可以动态改变微步，调整驱动器的许多参数，然后将所有结果保存到 EEPROM。如果你在玩一个新的马达，不知道它能加速多快，或者它能达到什么速度，没有什么比互动地玩它更好的了。

目前，除了代码本身和附带的视频之外，没有太多的文档，但实际上这看起来是您开始工作所需的全部内容。因此，如果你想复制哈卡戴(Moritz Walter)的[优秀的步进驱动器枪战](http://hackaday.com/2016/08/29/how-accurate-is-microstepping-really/)，像这样的工具正是你想要的。

 [https://www.youtube.com/embed/Lm8oprDhAnQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Lm8oprDhAnQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

