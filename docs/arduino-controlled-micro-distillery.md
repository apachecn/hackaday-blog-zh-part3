# Arduino 控制的微型酒厂

> 原文：<https://hackaday.com/2016/12/01/arduino-controlled-micro-distillery/>

他们说，酒是塑造人类历史的主要因素之一。创造新的更快的酿酒方法一直是一个很大的工程问题，所以[山羊工业]的这个项目相当有趣。这是一个完全自动化的微型蒸馏厂，叫做纳米蒸馏厂。

整个事情可以无人值守运行，但上传酿造过程的数据，进行远程监控和通知。考虑到蒸馏涉及到像酒精蒸汽这样的爆炸性物质，这是一个很大的优势。它都是国产的，包括由钢板组装的锅炉和一个风冷冷凝器。它由一个 Arduino Mega 控制，该 Arduino Mega 与几个 Adafruit 板相连，这些板与各种传感器和泵相连，控制系统中的酒流量。还有一个 Adafruit FONA 板，它包括一个蜂窝调制解调器，可以将数据上传到数据库，以监控进度，并在完成时通知您。

Instructable 甚至包括运行进程的 [Arduino 代码。从工程的角度来看，这是一个令人印象深刻的构建，最后的润色必须是控制器用来叙述过程的令人毛骨悚然的赛昂人的声音。休息之后会有一个视频参观。](http://www.instructables.com/id/The-NanoStillery-Automated-Whiskey-Distillery/step17/Arduino-Mega-Code/)

 [https://www.youtube.com/embed/ck-_yTsY5Bo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ck-_yTsY5Bo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你对酒精和其他饮料在技术发展中的作用感到好奇，我建议你阅读汤姆·斯坦戴奇的《六杯装世界历史》，这是一本通过啤酒、葡萄酒、烈酒、咖啡、茶和可乐的历史追溯文明史的优秀书籍。