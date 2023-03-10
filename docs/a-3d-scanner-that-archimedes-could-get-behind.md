# 阿基米德可以拿到的 3D 扫描仪

> 原文：<https://hackaday.com/2017/07/14/a-3d-scanner-that-archimedes-could-get-behind/>

3D 扫描似乎是一个简单的过程——将物体放入运动控制机架中，从表面反射光线，测量反射，并做一些数学运算来重建三维形状。但是传统的 3D 扫描对于具有复杂拓扑结构和大量光线无法到达的角落和缝隙的物体来说并不好。这就是为什么[体积 3D 扫描](http://irc.cs.sdu.edu.cn/3dshape/)有一天会成为一个重要的工具。

顾名思义，体积扫描依赖于测量物体通过介质时介质体积的变化。在[克菲尔·阿伯曼]和[柳文欢·卡齐尔]的“倾斜扫描”方法中，介质是一个水箱，它的水位是用浮子传感器高精度测量的。在收集数据时，机器人将待扫描的物体缓慢浸入水中。机器人移开物体，改变方向，再次下沉。重复蘸取，直到收集了足够的数据来运行能够重建物体形状的变换算法。水可以到达的任何地方都可以被扫描，下面的视频显示了如果有足够的数据，结果会有多好。完整的细节可以在他们论文的 PDF 文档中找到。

虽然使用标准转盘和激光配置的光学 3D 扫描可能会持续一段时间，但倾斜扫描似乎是一种使用真正简单的设备获得拓扑数据的强大方法。

[https://videopress.com/embed/xx88I1SN?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0](https://videopress.com/embed/xx88I1SN?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0)