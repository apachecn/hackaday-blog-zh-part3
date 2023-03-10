# 无电池高清视频流通过反向散射实现

> 原文：<https://hackaday.com/2018/05/17/no-battery-hd-video-streaming-does-it-with-backscatter/>

如果谷歌眼镜没有电池会怎样？那也不算太牵强。这款[无电池高清视频流摄像机](http://batteryfreevideo.cs.washington.edu/)可以嵌入一副眼镜框中，在不使用大容量电池或外部电源的情况下，将高清视频传输到附近的手机或其他接收器。华盛顿大学的研究人员正在利用反向散射来实现这一目标。

问题是，由于需要数字处理器和发射器，将高清视频无线传输到接收器的摄像机功耗超过 1 瓦。研究人员已经将处理硬件分离到接收单元中。然后，他们将模拟像素从相机传感器直接发送到反向散射硬件。反向散射包括将接收到的波反射回它们的来源。通过将视频信号添加到这些反射波中，他们消除了对耗电发射机的需求。完整的细节在他们的论文中，但这里是重点。

[![Battery-free camera design approach](img/32d4100d8eac6b2ea5af958b7f9381e8.png)](https://hackaday.com/wp-content/uploads/2018/05/battery_free_camera_design_approach.png)

在摄像机端，像素电压(CAM Out)是一个模拟信号，与三角波形一起被馈入比较器。只要三角波的电压低于像素电压，比较器就输出 0，否则输出 1。这样，像素电压被转换成不同的脉冲宽度。选择三角波形的最小和最大电压，使其覆盖摄像机电压的全部可能范围。

图中使用异或门的子载波调制是为了解决自干扰问题。这是来自与载波频率相同的发射机的不想要的干扰。因此使用子载波将 PWM 输出转换成不同的频率。然后，接收器可以滤除干扰。XOR 门实际上是 FPGA 的一部分，它也插入帧和行同步模式。

他们测试了这种电路设计的两种不同实现方式，一种是 112 x 112 灰度级，最高每秒 13 帧(fps)，另一种是高清。不幸的是，市场上没有高清摄像头能够提供原始模拟像素输出，因此他们使用 USB 从笔记本电脑中获取高清视频，并通过 DAC，然后进入 PWM 转换器。USB 将其限制在 10 fps。

结果是，720p 和 10 fps 的视频流使用低至 250 μW 的功率，并可反向散射达 16 英尺。他们还模拟了一个 ASIC，分别使用 321 μW 和 806 μW 在 60 fps 下实现了 720p 和 1080p。请看下面的视频，获得动画解释和演示。仅被动电源的结果视频令人印象深刻。

如果华盛顿大学在反向散射方面看起来很熟悉，那是因为我们之前报道过他们的[无电池(几乎)手机](https://hackaday.com/2017/07/09/at-last-almost-a-cellphone-with-no-batteries/)。尽管他们不是唯一的实验者。这里是[反向散射被用于土壤网络](https://hackaday.com/2017/03/03/using-backscatter-radio-for-a-soil-sensor-network/)的地方。所有这些都涉及到能量收集，现在是开始温习这些概念并构建自己的原型的好时机。[hack aday 奖包括今年的电能收集挑战](https://hackaday.io/prize/details#three)。

 [https://www.youtube.com/embed/0H9MHixUVko?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0H9MHixUVko?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

