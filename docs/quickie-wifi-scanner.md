# Quickie WiFi 扫描仪

> 原文：<https://hackaday.com/2016/02/24/quickie-wifi-scanner/>

把这个项目放在“把事情做完”而不是“最闪亮的东西”下面。[filid]与当地的一个免费 WiFi 接入小组合作，想要[绘制出他们安装的信号强度(RSSI)和覆盖范围](https://hackaday.io/project/9794-rssi-mapper-for-muenchenfreifunknet)。对于 ESP8266 来说，这是一个微不足道的任务，对于[filid]来说甚至更容易，因为他已经[为相同的硬件](https://www.linuxpinguin.de/project/iot-esp8266-local-wifi-scanner/)编写了一些 WiFi 扫描仪代码。

基本上，该设备是一个连接到 ESP8266 的 Neopixel 环。如果它检测到一个属于 [Freifunk München](https://ffmuc.net/) 网络的路由器，它会在一个吸引人的圆形“条形图”中显示环上的 RSSI。当它没有检测到 Freifunk 节点时，它会显示找到的 WiFi 路由器的数量。它通过串行端口转储更多的细节。

代码简短而甜蜜。如果您刚刚开始在 ESP 上使用 Arduino 固件进行联网，请查看一下。即使你不住在慕尼黑，你也能在几秒钟内把它调整到适合你自己的情况。

我们希望看到一个 GPS 和一个 SD 卡添加到这个，一个独立的有目的的 wardriving 设置。虽然我们承认小外形可能适合这个项目，但如果它像比尔博的“刺”一样发出蓝色的光，会有多酷呢？