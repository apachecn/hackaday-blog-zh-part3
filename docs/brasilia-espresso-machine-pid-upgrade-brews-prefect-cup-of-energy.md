# 巴西利亚浓缩咖啡机 PID 升级酿造提督杯能量

> 原文：<https://hackaday.com/2016/07/03/brasilia-espresso-machine-pid-upgrade-brews-prefect-cup-of-energy/>

咖啡、制作和黑客成瘾注定会失控。里斯·古德温的咖啡机也被黑了。最初只是一个二手咖啡机的小修复项目，最终导致了最先进的咖啡酿造技术的全面升级。

[![coffee_hack_arduino](img/d8402a28f5b83dce5f74a9d7afafff63.png)](https://hackaday.com/wp-content/uploads/2016/06/coffee_hack_arduino.jpg)*巴西利亚女士*号配有一个 300 毫升的黄铜锅炉、一个水泵和四个按钮，分别用于电源、咖啡、热水和蒸汽。一个直接连接到按钮上的 3 通交流电磁阀选择三种功能中的一种，而一个喜怒无常的双金属开关使锅炉大致保持在“差不多”和“太热”之间。

为了减少温度的波动，[里斯]决定增加一个 PID 控制回路，同时还增加一个有机发光二极管显示器。他为 Arduino Nano 设计了一个小防护罩，通过固态继电器与当前的硬件接口。两个热电偶测量锅炉和组头的温度，而热切断保险丝在发生故障时防止机器过热。

此外，*女士的*妆容接受了一次彻底的检修，从一层新鲜的粉末涂层开始。有机发光二极管显示器的密封外壳和抛光的顶部面板都是由铝加工而成的。[Rhys]还增加了一个外部水箱，通过闪亮的定制车床管接头连接到机器上。在水进入锅炉之前，它通过一个定制的预热器，以避免冷水直接进入锅炉。结果不仅看起来棒极了，它还提供了对温度和提取水量的更多控制，从而每次都能得到完美的冲泡。欣赏[Rhys]的视频，其中他解释了他的身材:

 [https://www.youtube.com/embed/OJqH6CJR3TU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OJqH6CJR3TU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Pirate14]的提示！