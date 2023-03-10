# 用振动器将 DC 转换成 DC

> 原文：<https://hackaday.com/2016/07/04/retrotechtacular-dc-to-dc-conversion-by-vibrator/>

电有两种基本形式:交流电和直流电(DC)。DC 使用方便，易于分析。然而，AC 也有一些有用的属性。特别是，交流电流可以驱动变压器，变压器可以很容易地升压或降压。当然，功率是守恒的(实际上，由于变压器中的损耗，你得到的功率更少)。

你不能用纯 DC 做到这一点。你可以降低电压，尽管这通常会浪费热量(例如，分压器或线性稳压器)。除非你先把 DC 电压转换成某种交流电，否则你不能轻易提高它。

在电子管时代，这是一个特别严重的问题——尤其是汽车收音机中的电子管。汽车的电压可能是 12V，但电子管的极板可能需要数百伏电压。你是做什么的？一些老式汽车收音机使用所谓的发电机。这只是一个盒子里的马达和发电机。你可以用 12V 旋转马达，让发电机产生不同的电压(甚至是 DC 电压)。

 [https://www.youtube.com/embed/QLQBSZZLn_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QLQBSZZLn_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 电动发电机

仔细想想，变压器实际上只是一台发电机(次级)，其转轴被移动磁场(初级)所取代。然而，有了发电机，你可以用 DC 发动机来旋转输入。对于变压器，必须有交流输入，因为这是移动磁场的原因。注意，不一定要正弦波，只要电流极性切换足够快，就可以驱动原边。

那么，如何将汽车收音机中的 DC 转换成交流电呢？在车的另一部分有一个线索:用来闪灯的闪光灯。今天，你可能会用一些电子设备来闪烁，但老式汽车没有太多的电子设备。他们拥有的是一种特殊的装置。当你给这个装置通电时，它会加热一个双金属片。铝带会慢慢移动并切断电流。这将冷却铝带，铝带将恢复其原始位置并再次开始电流流动。

如果你想让事情进展得更快，你可以用接力赛来做同样的事情。让继电器线圈通过常闭触点获取电流。当线圈通电时，触点打开，切断电流。然后触点闭合，重复该过程。

## 测试，1，2，3

[![RCA-tube-tester-at-Oklahoma-History-Center](img/e22611654c30b76d45589e4551a3a8fb.png)](https://hackaday.com/wp-content/uploads/2016/06/rca-tube-tester-at-oklahoma-history-center.jpg) 药店里的老试管测试员(见右图)经常对震动棒进行测试。在那些日子里，那没有你今天所期待的意义。事实上，振动器是一个继电器，用来中断交流 DC 电流。你可能会认为这些经常失败，去一趟药店会让你测试振动器和管子，买一个替代品，并修理你自己的设备。

振动器这个名字来源于这些设备发出的特有的嗡嗡声。一旦 DC 被振动器打破，变压器就可以将电压升高(或降低，但几乎总是升高)。这会产生更高的交流电压，然后电路会对其进行整流和滤波，以获得所需的更高电压。

[![Heathkit_Vibrator](img/7951bd34b6a279a255e75b07b2e1f319.png)](https://hackaday.com/wp-content/uploads/2016/06/heathkit_vibrator.jpg) 制造一个好的振动器电源实际上比你想象的要复杂得多。机械零件不停地移动。此外，触点会产生火花，这会腐蚀触点。这也造成了许多干扰或混乱。一个好的设计会抑制火花和杂碎。由此产生的整流电流也需要很好的滤波。左边的照片显示了一对 Heathkit 振动器，包括通常隐藏的内部结构。

虽然振动器似乎效率不高，但它胜过发电机。它更安静，运动部件更少，更小，也更便宜。当时，这似乎是一种进步。

## 今天

除了老式设备，振动器早已过时。晶体管功率逆变器变得实用并逐渐被淘汰。今天，您更有可能使用开关模式电源来获得相同的效果。原理没什么不同，但是 DC 到交流电的转换是电子的，控制更精确。

如果你想了解更多关于振动器的信息——包括原理图——请看下面的视频。

 [https://www.youtube.com/embed/Fp6PkRTmb8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Fp6PkRTmb8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



WikimediaFoundationVEVO 拍摄的振动器照片( [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0) )

* * *

**Retrotechtacular is a column featuring hacks, technology, and kitsch from ages of yore. Help keep it fresh by [sending in your ideas for future installments](mailto:tips@hackaday.com?Subject=[Retrotechtacular]).**