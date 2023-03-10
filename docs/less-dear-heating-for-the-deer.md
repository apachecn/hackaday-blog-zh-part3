# 对鹿来说不太贵的取暖设备

> 原文：<https://hackaday.com/2018/01/13/less-dear-heating-for-the-deer/>

将来自世界热带地区的动物饲养在寒冷的气候中是一件昂贵的事情，它们需要一个温暖的环境在它们的围栏和睡觉的地方。马韦尔动物园花了一大笔钱用电加热来为他们的 nyalas(一种羚羊，而不是如标题所示的鹿，原产于南非)取暖，所以他们寻找一种可以降低成本的技术，只在动物在围栏中时加热。

人们可能会认为被动红外传感器可以解决这个问题，但睡觉的尼亚拉很快就会成为这些设备的背景热量的一部分，因此，加热器不会工作足够长的时间来保持动物的温暖。该解决方案来自一个不太可能的来源，即慕尼黑 IBM Watson 总部的咖啡队列监控项目，该项目使用一系列红外传感器来监控不断变化的热量模式，从而衡量长时间等待饮料的可能性。

在 zoo 应用程序中，连接到 ESP8266 电路板的一系列热传感器与 Raspberry Pi 进行对话，Raspberry Pi 汇总读数并将其发送到 IBM Watson 云，在那里由神经网络进行分析。然后决定尼亚拉是否在视野之内，并相应地烘烤动物。

这个项目在使用 Watson 的过程中，与 Hackaday 奖的参赛作品[自动野生动物识别](https://hackaday.com/2017/06/14/hackaday-prize-entry-automated-wildlife-recognition/)有一些相似之处。

尼亚拉形象:[Charlesjsharp【CC BY-SA 4.0】](https://commons.wikimedia.org/wiki/File:Nyala_(Tragelaphus_angasii)_female.jpg)。