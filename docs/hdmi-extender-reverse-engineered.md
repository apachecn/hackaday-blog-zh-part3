# HDMI 扩展器反向工程

> 原文：<https://hackaday.com/2016/06/09/hdmi-extender-reverse-engineered/>

[danman]一直在尝试各种 HDMI 视频流选项，他突然想到了一个很棒的低成本解决方案。一个 40 美元的“HDMI 扩展器”实际上是引擎盖下的 HDMI-to- [RTP](https://en.wikipedia.org/wiki/Real-time_Transport_Protocol) 转换器。

他之前在一个类似的扩展器上做过工作，结果发现使用了一种古怪的方法来发送视频，他很自然地逆转了这种方法，并按照他的吩咐做了。但是非标准格式是一种痛苦。因此，当他得到同一设备的新版本，并开始用 Wireshark 偷窥数据包时，他惊喜地发现输出只是 RTP 上的 MPEG 编码视频。不需要黑客攻击。

到目前为止，通过 IP 网络从任意 HDMI 输出流视频一直很棘手，[丹曼]一直有点痴迷于让它廉价工作。除了这个扩展器的前一个版本，他还设法从一个[根 Android 机顶盒](http://hackaday.com/2016/01/06/android-set-top-box-lets-you-stream-and-record-via-hdmi-input/)中获得了一个流。这要多花一点钱，但是如果你需要的话，也可以同时录音。

然而，这些都没有解决 HDMI HDCP 加密的问题。那件事你得靠自己了。

(你们这些 Wireshark 向导会注意到，我们只是从项目的前一版本中抓取了标题图片。这个没有好的图像。很抱歉。)