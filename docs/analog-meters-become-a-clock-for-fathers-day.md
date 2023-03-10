# 模拟仪表成为父亲节的时钟

> 原文：<https://hackaday.com/2018/06/22/analog-meters-become-a-clock-for-fathers-day/>

每年父亲节前后，我们通常会看到一些以父亲为导向的项目。有些是爸爸或爷爷给孩子们的项目，而有些是给大家伙的礼物。[这款模拟时钟](http://michaelteeuw.nl/post/174972004187/what-time-is-it-fathers-day)属于后一类，额外的奖励是承认和尊重[Micheal Teeuw]的父亲在所有技术方面对他的影响。

[![](img/34e2a40b50d6fd9ba52cfa793379e670.png)](https://hackaday.com/wp-content/uploads/2018/06/tumblr_inline_paf160rj641s95p1z_500.gif) 【迈克尔】有一阵子一直在琢磨一个伏特计时钟，那里的时、分、秒都显示在动圈表上。来自 Ali Express 的三个模拟电表将为该项目提供合适的外观，但作为 200 伏交流电表，它们需要稍加修改。[Michael]移除了机芯内部的整流二极管和滤波电容器，并替换了具有较小值的限流电阻器，以在仪表上获得 5 伏的全量程偏转。Adobe Illustrator 帮助将原始刻度替换为时间刻度，并将 led 添加到仪表中用于背光照明。TinyRTC 记录时间并产生三个 PWM 信号来驱动电表。每一个血糖仪都安装在它自己的 3D 打印的盒子里，三个盒子连接在一起成为一个光滑的控制台。我们喜欢它的外观，这让我们想起了飞机驾驶舱里的仪表组。

为[迈克尔的父亲]让他的儿子进入修补艺术而喝彩，为[迈克尔]的好身材干杯。我们喜欢看到旧计量器的新用途，比如这些服务器性能监控计量器。

[通过 [r/DIY](https://www.reddit.com/r/DIY/comments/8s1efr/due_to_my_dads_fascination_for_analog_volt_meters/)