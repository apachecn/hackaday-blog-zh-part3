# 测量斯图加特的微粒

> 原文：<https://hackaday.com/2017/04/08/getting-a-measure-on-particulates-in-stuttgart/>

德国目前正在进行一场关于颗粒物空气污染的大讨论。德国的“汽车城”斯图加特是但丁笔下高峰时段七大地狱之一，去年发布了全国首个空气污染预警。许多城市正在考虑彻底禁止老式柴油车。到目前为止，斯图加特的禁驾日是自愿的，季节的变化也帮了很大的忙。但这并不意味着没有问题。

但是这个问题有多大？又在哪里本地化呢？还是颗粒物污染根本就是局部化的？这些问题将受益于颗粒传感器的分布式网络，斯图加特的 OK 实验室已经[组织了一个简单的项目](http://luftdaten.info/feinstaubsensor-bauen/)(此处翻译为)将大量联网的传感器放到野外，价格低廉。

基本构建是一个带有 SDS011 颗粒传感器的 ESP8266，如果你觉得有趣，还可以带有温度和湿度传感器。这个建议的房屋非常巧妙:两个 90 度的 PVC 管段阻挡雨水，但让灰尘通过一个小管进入。他们提供的固件负责让设备通过您的家庭 WiFi 上网。一旦你让它运行起来，给他们发一封电子邮件，你就上线了。如果你需要帮助，可以到窝棚去。

我们喜欢这种聚合的公民科学监测项目，特别是当它们的设计使得购买成本很低时，无论是从花费的金钱还是从让您的传感器上线的难度来看。这一努力让我们想起了 [Blitzortung](http://hackaday.com/2014/06/29/a-cloud-of-lightning-detectors/) 、[这个辐射监测网络](http://hackaday.com/2015/12/07/globally-distributed-sensor-net-monitors-air-quality-and-radiation/)，或者是 [2014 年获得黑客日大奖的卫星图](http://hackaday.com/2015/02/19/ground-stations-are-just-the-beginning-the-satnogs-story/)。虽然我们理解对昂贵和校准设备的需求，但看看用便宜得多的设备能走多远也很有趣。