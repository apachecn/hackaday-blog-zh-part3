# 34C3:麦克风窃听器

> 原文：<https://hackaday.com/2018/01/01/34c3-microphone-bugs/>

灵感可以来自很多地方。当来自阿根廷 MatesLab Hackerspace 的[Veronica Valeros]和[Sebastian Garcia]得知[艾未未]花了四年时间才发现他的家被窃听时，他们决定更仔细地研究一些标准的音频监控设备。感觉到社区内缺乏对该主题的研究，他们将问题掌握在自己手中，并在 34C3 的 [Spy vs. Spy:麦克风窃听器操作和检测的现代研究](https://media.ccc.de/v/34c3-8735-spy_vs_spy_a_modern_study_of_microphone_bugs_operation_and_detection)演讲中展示了结果。你可以在这里找到幻灯片[，在这里](https://gsec.hitb.org/materials/sg2017/D1%20-%20Veronica%20Valeros%20and%20Sebastian%20Garcia%20-%20A%20Modern%20Study%20of%20Microphone%20Bugs.pdf)找到他们的白皮书[。](https://gsec.hitb.org/materials/sg2017/WHITEPAPER%20-%20Veronica%20Valeros%20and%20Sebastian%20Garcia%20-%20A%20Modern%20Study%20of%20Microphone%20Bugs.pdf)

[Veronica]和[Sebastian]将他们的研究主要集中在 FM 无线电发射设备上，他们从一些历史实例和这类设备的开发开始，这些设备现在很便宜就可以买到。虽然这些设备可能会被视为苏联时代间谍小说的遗物和模拟时代的工具，但容易获得和使用仍然使它们在今天具有相关性。他们用一个捉迷藏的游戏作为真实生活的实验来结束他们的研究，使用的是从商店里买来的普通发射器。

没有 RTL-SDR 加密狗，这样的任务是不完整的，因此[Sebastian]开发了 [Salamandra 间谍麦克风检测工具](https://github.com/eldraco/Salamandra)作为现成检测设备的替代产品。利用加密狗的能量水平，Salamandra 检测并定位潜在发射器的存在，跟踪所有发现。如果你对一些最早的、技术上最迷人的秘密监听设备感兴趣，没有比[特雷门琴的窃听器](https://hackaday.com/2015/12/08/theremins-bug/)更好的例子了。

[https://media.ccc.de/v/34c3-8735-spy_vs_spy_a_modern_study_of_microphone_bugs_operation_and_detection/oembed](https://media.ccc.de/v/34c3-8735-spy_vs_spy_a_modern_study_of_microphone_bugs_operation_and_detection/oembed)