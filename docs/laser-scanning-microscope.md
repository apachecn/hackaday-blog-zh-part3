# 激光扫描显微镜

> 原文：<https://hackaday.com/2017/02/08/laser-scanning-microscope/>

还记得你第一次低头看显微镜时的那种感觉吗？现在你可以重新体验它，但方式略有不同。[Venkes]想出了一种方法来制作激光扫描显微镜(LSM)，其中大部分是现成的组件，你可能会坐在那里，在你的车库里收集灰尘。他使用了一些改装的 DVD 摄像头、一台 Arduino Uno、一台激光和一台 LDR。

[![fuyati3iy4qiced-large](img/5e9bec2afbc83f55c0f7926e8587571e.png)](https://hackaday.com/wp-content/uploads/2017/02/fuyati3iy4qiced-large.jpg)

EPROM die shot

老实说，LSM 的制作还涉及到更多的东西，但是[文斯]做了一个详细的说明，解释了所有的东西是如何组合在一起的。你需要相当大的耐心，对焦不容易，而且非常慢，一幅图像需要大约半个小时才能完成，但它可以在 65k 像素(256×256)下放大 1300 倍。从阅读说明来看，似乎你需要一只稳定的手来组装它，有些步骤看起来有点棘手。在软件方面，LSM 使用 Arduino 和 Processing。Arduino 部分负责镜头的转向和 LDR 读数。然后，这些信息被发送到处理单元，处理单元负责解释数据并将其转换成图像。

构建难度等级应该在 [DIY 智能手机显微镜](http://hackaday.com/2013/10/30/use-your-smartphone-as-a-microscope-for-less-than-10/)和[激光测序仪超级显微镜](http://hackaday.com/2016/08/15/laser-sequencer-uses-arduino-to-enable-super-microscope/)之间。最后，如果一切顺利，你会得到一些很酷的图片:

 [https://www.youtube.com/embed/CtK4RvX8Kis?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CtK4RvX8Kis?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

