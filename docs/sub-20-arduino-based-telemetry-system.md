# 低于 20 美元的基于 Arduino 的遥测系统

> 原文：<https://hackaday.com/2017/09/12/sub-20-arduino-based-telemetry-system/>

[威廉·奥斯曼]着手证明，与昂贵的商业数据测井设备不同，他可以用不到 20 美元得到同样的结果。他想为一个赛车项目制造一个无线三轴加速度计，允许工程师根据收集的数据对悬架进行修改。

硬件由连接到三轴加速度计的 Arduino Pro Mini 和 nRF24L01 无线模块组成。电源由赛车的 12 V 供电，由线性调节器转换为 5 V，Pro Mini 依次提供 3.3 V。基站由一个 Arduino 和另一个插入笔记本电脑的 nRF24L01 模块组成。

遥测系统基于[宇宙](http://cosmosrb.com/docs/home/)，一个由贝尔航天公司推出的开源实时数据记录平台。COSMOS 由 15 个独立的应用程序组成，具体取决于您希望如何查看和管理您的遥测数据。你可以在谷歌文档上下载【威廉】的[宇宙配置文件和 Arduino 草图](https://drive.google.com/drive/folders/0B63acZxh19DWVUQxSW8yNlJzUFk?usp=sharing)。

我们已经发表了一堆关于遥测技术的文章，比如这个 [ESP8266 遥测项目](https://hackaday.com/2016/03/04/serial-telemetry-to-wi-fi-with-an-esp8266/)，一个[火箭遥测装置](https://hackaday.com/2012/07/16/rocket-telemetry-from-uav-hardware/)，以及[开源卫星遥测技术](https://hackaday.com/2014/11/25/open-sourcing-satellite-telemetry/)。

【谢谢丹尼斯·内斯特！]