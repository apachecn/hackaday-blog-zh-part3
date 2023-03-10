# 宜家 Tradfri 黑客

> 原文：<https://hackaday.com/2017/06/14/ikea-tradfri-hacking/>

智能照明现在风靡一时。当然，Phillips Hue 是市场上的巨头，但还有很多 ZigBee、蓝牙和 WiFi 灯泡。以廉价家具、肉丸和华夫饼闻名的宜家最近加入了他们的 Tradfri 系统。像宜家的大多数产品一样，它们既有效又便宜。[Andreas] [拿着一个 Dremel 到控制器](https://www.youtube.com/watch?v=olxPqiJcUAQ)并展示如何侵入系统来使用 MQTT。你可以看看下面的视频。

一旦他打开了设备，他就使用我们之前谈到的[德国制造杂志文章](https://hackaday.com/2017/02/06/reverse-engineering-ikeas-new-smart-bulbs/)来帮助理解他有什么。有了引出线，他就能把线束焊接到控制器上了。然后，他连接了一个 WeMos 板。一点 Arduino 代码之后，他用 MQTT 控制灯光。

在 MQTT 中，很容易将灯连接到各种系统，而不必像默认情况下那样使用单独的集线器。[Andreas]指出，尽管如此，该系统没有提供任何可能使事情变得困难的反馈。然而，他计划在未来进一步破解这些设备。

如果您想了解更多关于 MQTT 的信息，顺便说一下，[埃利奥特·威廉姆斯]做了一个很好的系列文章，可以帮助您开始。

 [https://www.youtube.com/embed/olxPqiJcUAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/olxPqiJcUAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

