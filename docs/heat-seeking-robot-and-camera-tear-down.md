# 热寻机器人和摄像机拆卸

> 原文：<https://hackaday.com/2018/04/24/heat-seeking-robot-and-camera-tear-down/>

[Marco Reps]在他的邮箱里发现了一台 HT02 热成像相机。他发现这种分辨率对于观察大物体来说是不错的，但对于检查电路板来说却毫无价值。所以他决定把它撕成碎片——我们完全理解这种冲动。

里面是一个热电堆传感器，很容易逆向工程。所以[Marco]决定重新设计一个树莓派机器人来使用摄像头，并将其变成热探测器。

与其他类似设备相比，该相机相对便宜，并且显然使用了更便宜的传感器类型。然而，传感器本身易于使用。[Marco]发现了一个每半秒脉冲一次的引脚来触发采集。另一个引脚产生几千个脉冲，这是从器件读取模拟输出的信号。真的就这么简单。

对于正确的应用，HT02 可能值这个低价，尽管我们听说它们并不总是构造得很好。我们认为有趣的一个功能是能够合并可见光图像和红外图像，这样你可以更好地了解你正在看的东西。

低成本和低分辨率让我们想起了几年前 Hackaday 奖的参赛作品。然后，你可以采取更简单的方法，[建立一个逐点工作的扫描仪](https://hackaday.com/2017/01/19/diy-thermal-imaging-done-low-tech-style/)。

 [https://www.youtube.com/embed/dPZUcyfhzyg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dPZUcyfhzyg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

