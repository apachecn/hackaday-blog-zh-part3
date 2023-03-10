# Pi 零以太网的艰难之路

> 原文：<https://hackaday.com/2015/12/06/pi-zero-ethernet-the-hard-way/>

[Alex@Raspi.tv]不幸吹爆了一个 Raspberry Pi B+上的 USB 集线器和以太网端口。他考虑使用廉价的 SPI 转以太网板来拯救它，虽然他买了板，但他从未考虑过将其与损坏的 PI 接口。然而，当他看到 Raspberry Pi Zero 到达并注意到每个人都想将其连接到网络时，他想起了 SPI 板，从他的垃圾箱中将其救出，几个小时后通过 Raspberry Pi GPIO 使[以太网工作。](http://raspi.tv/2015/ethernet-on-pi-zero-how-to-put-an-ethernet-port-on-your-pi)

为了让事情变得更容易，他让所有的工作首先在 Pi A 上，然后移动到零。您可能会认为性能不会很好，但是[Alex]进行的测量显示它一点也不差，考虑到:

12 MHz 时的 Pi 零点下降 3.33 毫巴，上升 2.82 毫巴，延迟 39.956 毫秒，延迟 52.19 千米
16 MHz 时的 Pi 零点下降 3.67 毫巴，上升 2.90 毫巴，延迟 37.749 毫秒，延迟 43.57 千米
20 MHz 时的 Pi 零点下降 3.88 毫巴，上升 3.10 毫巴，延迟 42.474 毫秒，延迟 43.57 千米

[Alex]注意到 Pi 的官方 3.3V 供电轨容量不符合他使用的 SPI 以太网模块的要求。然而，他也说这是可行的，而且他“非正式地”听说这可能是可行的。我们不确定他是说他听说 Pi 的 3.3V 电源被低估了，还是以太网芯片的消耗被夸大了。

在过去的一两周内，我们已经看到了很多 Pi Zero 黑客攻击。WiFi 黑客攻击与此类似，还有[音频黑客攻击](http://hackaday.com/2015/12/05/swapping-gpio-pins-on-the-pi-zero-for-audio/)。当然，也有关于你是否应该尝试[延长零](http://hackaday.com/2015/12/01/raspberry-pi-zero-or-minus-one/)的激烈辩论。