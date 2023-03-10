# 走漫长的道路，以精确的激光印刷电路板曝光

> 原文：<https://hackaday.com/2016/04/06/take-the-long-road-to-a-precise-laser-pcb-exposer/>

根据[diyouware]的说法，每个 HD-DVD 播放器内部都有一个激光工程宝石，名称为 PHR-803T，它[只是乞求被转换为 PCB 曝光器](http://www.diyouware.com/node/161)。继类似的黑客将激光二极管从蓝光播放器中取出，暴露出[PCB](http://hackaday.com/2016/03/14/laser-pcb-exposer-built-from-cd-rom-drives/)之后，他们想在不拆卸的情况下使用整个 PHR-803T 单元，并尝试启用其所有独特的功能。

他们为他们的机器设想了像扫描仪这样简单的东西。只需将 PCB 放在玻璃片上，合上盖子，然后点击打印。不幸的是，移动激光器本身只是引起了太多的振动。于是他们改用倒三角机器人，命名为 TwinTeeth。在这种设计中，激光器会保持静止，而 PCB 会移动。

接下来是逆向工程和设计中令人印象深刻的旅程。PHR-803T 没有数据表，但有大量的功能。例如，它可以自动对焦，并有三个不同的激光二极管。发现并解决了许多有趣的问题。例如，来自激光的光晕导致周围的光致抗蚀剂固化。他们通过增加一个上面有紫外线过滤膜的玻璃板解决了这个问题。只有最集中的激光点才能穿透。

另一个冒险是自动对焦。他们想自动对焦在棋盘的四个角上。PHR-803T 旨在读取 HD-DVD，因此可以将光束聚焦到远低于 0.01 毫米的位置。他们使用紫外激光进行自动聚焦，但如果不固化光刻胶，就无法在 PCB 上使用它。所以他们把一块铝箔放在一个已知的水平开始。然后他们意识到他们可以用红色或红外二极管来聚焦。现在，他们可以在软件中调平 PCB，并在不固化光刻胶的情况下聚焦二极管。

最终他们有了一个倒三角形的迷你 PCB 工厂。它可以生产分辨率为 600 DPI 的 Arduino shield 大小的电路板。他们的机器还有钻孔和锡膏分配的附件。看看它的视频。

 [https://www.youtube.com/embed/rDTOBbg9ZXU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rDTOBbg9ZXU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

