# 电阻轮形成独特的旋转编码器

> 原文：<https://hackaday.com/2016/06/15/wheel-of-resistors-form-unique-rotary-encoder/>

延续他用金属丝和木屑制造奇迹的传统，[HomoFaciens]又回来了，为机电编码器设计了一个独特而巧妙的[。](http://www.homofaciens.de/technics-base-circuits-encoder-disc-2_en_navion.htm)

有很多方法可以构建一个编码器，这是一个我们以前从未见过的方法。无意以任何方式成为实际的工程解决方案，[HomoFaciens]的构建日志和下面的视频记录了他的方法。使用一个由三个、六个或八个电阻分成若干段的旋转圆盘，编码器通过在圆盘转动时将每个电阻添加到分压器中来工作。Arduino 读取分压器的输出，并通过比较电压序列来确定旋转方向。电阻越多，分辨率越高，但由于擦拭触点的软件去抖，最大轴速会降低。[HomoFaciens]在他的关于光学编码器的教程中已经涉及了类似的内容，但这是一个新的转折——一种低分辨率连续旋转电位计。这是一个简单的概念，是对分压器的良好回顾，也是检测轴旋转的独特方式。

这些真的都是基本的东西吗？没错。这有什么实际意义吗？可能不会，尽管我们会打赌这些编码器会在未来的 CNC 构建中找到出路。这是一个执行良好的好主意吗？哦是的。

 [https://www.youtube.com/embed/RwIpz9oP2hY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RwIpz9oP2hY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

