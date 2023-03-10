# 死星的视觉暂留

> 原文：<https://hackaday.com/2017/01/21/persistence-of-vision-death-star/>

在《星球大战》电影中，死星被摧毁了两次，但仍有一颗活在这个由英国利兹大学孟小组制作的 168 LED 视觉暂留地球仪中。虽然死星需求量很大，但他们将其安装在倾斜 23.4 度(与地球相同)的轴上，以便他们可以显示覆盖有天气信息、国际空间站位置或世界时钟的地球。

更多细节可在他们的[系统概述页面](https://povglobe.wordpress.com/system-overview/)上获得，但简单来说:旋转在内部并安装在轴上的是一个 Raspberry Pi，它通过其 HDMI 端口将视频或静态图像发送到一个定制的基于 FPGA 的 HDMI 解码器板。该板然后控制安装在一个平衡良好的铝环上的 14 个 LED 驱动板。所有这些都需要 75W 的电流通过一个四相整流器。旋转速度为 300 RPM，帧速率为 10 FPS，正如你在下面的视频中看到的，它工作得很好。

这不是我们在这里看到的第一颗 POV 死星。[Jason]用他自己的旋转 PCB 做了一个[小一点的，只能用牛逼来形容。](http://hackaday.com/2012/10/01/build-a-pov-death-star-you-will/)

 [https://www.youtube.com/embed/1qDidn_xEYE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1qDidn_xEYE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[途径 [Adafruit](https://blog.adafruit.com/2017/01/13/build-your-own-death-star-as-a-3d-spherical-persistence-of-vision-display-piday-raspberrypi-raspberry_pi/)