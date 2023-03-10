# Arduino +几何+自行车=速度计

> 原文：<https://hackaday.com/2017/03/09/arduino-geometry-bicycle-speedometer/>

去大商店为你的自行车买一个数字速度计是很容易的。这不仅不好玩，而且这个小小的数字显示器也不会为你赢得任何黑客信誉。[AlexGyver]有答案。利用 Arduino 和伺服系统，他为自己的自行车制造了一个经典的指针式速度计。它也有一个数字显示器，并使用霍尔效应传感器来获取车轮速度。你可以在下面看到这个项目的视频。

[Alex]讲述了相关的几何知识，以防你的高中数学已经深入你的后视镜。轮子的周长是你转一圈的距离。如果你知道距离和时间，你就知道速度，剩下的就是把数字速度转换成伺服电机的角度。代码在 [GitHub](https://github.com/AlexGyver/Arduino_speedometer) 上发布。

诚然，阅读磁铁，保持时间，并驱动伺服不完全是尖端。另一方面，它让我们思考你还能驱动什么样的输出。例如，我们还没有见过数码管速度计(好吧，反正不是在[自行车](https://hackaday.com/2015/07/16/nixie-tube-speedometer-in-motorcycle-handlebars/)上)。或者可能是一个像旧钟一样的机械翻转数字。

我们已经看到了一些带有 Arduinos 和许多 led 的产品(虽然，再次强调，不是真正的自行车)。[这个速度表](https://hackaday.com/2011/10/07/light-up-biking-vest-shows-impatient-drivers-how-fast-you-are-going/)可能仍然是我们最喜欢的。

 [https://www.youtube.com/embed/1ycA7TFV4t4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1ycA7TFV4t4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

