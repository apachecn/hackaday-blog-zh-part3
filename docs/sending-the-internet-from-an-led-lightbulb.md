# 从 LED 灯泡发送互联网

> 原文：<https://hackaday.com/2015/09/27/sending-the-internet-from-an-led-lightbulb/>

能承载互联网流量的东西总是在增加。现在，你可以将 LED 灯泡添加到这个列表中，因为迪士尼研究所的工程师刚刚展示了一个使用 LED 灯泡传输互联网流量的系统。这种通信方式并不新鲜:可见光通信(VLC)之前已经由迪士尼和[其他](http://www.hhi.fraunhofer.de/departments/photonic-networks-and-systems/products-and-services/vlc-system-500-mbits.html)在[演示过，但这个项目将其放入标准的 LED 灯泡中。这种灯泡已经过修改，包括运行 OpenWRT 的 Atheros AR9331 SoC 和控制发送和接收数据的 LED 元件和传感器的 Atmel ATmega328p。因此，该设备充当了 WiFi 网络和 VLC 网络之间的网关。](http://www.disneyresearch.com/project/visible-light-communication/)

迪士尼的[新测试系统](http://www.disneyresearch.com/wp-content/uploads/Linux-Light-Bulbs-Enabling-Internet-Protocol-Connectivity-for-Light-Bulb-Networks-Paper.pdf) (PDF 链接)并不是特别快:它每秒只能传输大约 380 到 400 比特，所以它不会很快成为流媒体视频。这绝对够快了，尽管要向玩具发送控制数据，或者向房间里的设备发送持续更新的数据流，例如带有持续更新的百科全书的电子书阅读器。这就是迪斯尼，作者们创造了一个新词来结束他们的论文:玩具互联网。