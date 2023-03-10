# 用一个便宜的自制尿液流量计来评估你的尿量

> 原文：<https://hackaday.com/2018/04/01/assess-your-output-with-a-cheap-diy-urine-flowmeter/>

关于人体的一些东西测量起来微不足道。身高、体重、血压、脉搏、体温——这些都可以用最简单的仪器轻松量化，并能为我们的健康状况提供有价值的见解。心脏和大脑中的电活动也可以用更复杂的仪器来捕捉，各种各样的示波器可以插入各种孔中，以获得关于正在发生的事情的可操作信息。

但是，呃，去呢？尿流量可以是许多疾病和状况的重要先行指标，但它通常依赖于患者的主观报告。有没有一种方法可以客观的衡量尿液流动的好坏？[当然有](http://www.rodic.si/wordpress/diy-uroflowmetry-machine-arduino-part1/)。

[GreenEyedExplorer]的简易尿流计的目标很简单:提供一种便宜、易于使用的仪器，任何患者都可以使用它来量化排尿时的尿流率。现在，我们知道你在想什么——难道液体流量不是通常在一个封闭的系统中测量的吗?中有[一个桨轮](https://hackaday.com/2017/09/02/hackaday-prize-entry-fighting-dehydration-one-sip-at-a-time/)或[一些伸入液流的东西？](https://hackaday.com/2017/08/25/custom-cut-pinwheel-makes-a-useful-hvac-duct-flow-meter/)这样的尿流装置不是侵入性的就是杂乱的，或者两者兼而有之？放心，这个手法简单又整齐。一个小型称重传感器通过 HX711 称重传感器放大器连接到 ESP8266。测压元件上的一个小盘子在排尿时接收尿液，尿液撞击盘子的力由软件评估。可以打印报告与您的医生分享，并保留记录以查看流量随时间的变化。

开玩笑，这可能是一个重要的诊断工具，在 10€建立，它授权任何人负责自己的健康。由于[GreenEyedExplorer]实际上是一名泌尿科医生，我们对此非常重视。

 [https://www.youtube.com/embed/bqYgydm8a3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bqYgydm8a3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/NMbClpUaz8Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NMbClpUaz8Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 [r/esp8266](https://www.reddit.com/r/esp8266/comments/88a102/diy_uroflowmetry_machine_for_10_free_plans/)