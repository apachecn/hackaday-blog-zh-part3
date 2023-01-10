# 厕所用的原木

> 原文：<https://hackaday.com/2017/04/29/logs-for-a-toilet/>

物联网是一个神奇的概念，最早出现在 90 年代初至中期的论文中。可穿戴设备会向私人服务器报告你的位置、健康状况和生理信息。你浴室里的摄像头会告诉你的医生痣是否变大了。你的车会监控你的机舱空气过滤器的寿命，到时候再买一个新的。纳米机器人将成为可编程的物质，可以变成椅子、房子和厨房用具。无处不在的计算将作为一种看不见的蜂群思维服务于人类。这是由越来越小的计算机、传感器和先进的机器人技术带来的天堂。

未来并没有像我们计划的那样。虽然科学家和工程师负责询问如何制造联网烤面包机，但没有人问 T2 为什么会有人想要这个。至少我们从这笔交易中得到了 3Com Audrey。

快进到今天，我们了解到【克里斯托弗·希勒】[刚刚把他的马桶放到了网上](https://hackaday.io/project/13336-i-put-my-toilet-on-the-internet)。他为什么要这么做？就连他自己也不知道，但这确实是一个很棒的“厕所里的木头”双关语。

这款设备的硬件是一个 [Digistump Oak](http://digistump.com/products/145) ，一个小巧的兼容 Arduino 的 WiFi 开发板。Digistump Oak 能够发布到[粒子云](http://www.particle.io/)，并且只需五行代码，【Chris】就能够发布一个 flush 到互联网。这个建筑传感器是一个便宜的塑料浮控开关。这个版本只有三个元件，其中一个是 4k7 电阻。

现在，这个版本有一些问题。它是电池供电的，但那只是因为[克里斯]的厕所离墙上的插座不够近。浴室里有点潮湿，保鲜膜暂时解决了这个问题，但一些愚蠢的锥形卡能以正确的方式解决这个问题。[克里斯]也有两个厕所，所以他需要再建一个。