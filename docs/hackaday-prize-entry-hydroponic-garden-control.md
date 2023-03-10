# Hackaday 奖参赛作品:水培花园控制

> 原文：<https://hackaday.com/2017/07/21/hackaday-prize-entry-hydroponic-garden-control/>

[Todd Christell]在自家后院的水培桶中种植西红柿，最近他遭受了作物损失，因为一个机械计时器未能按照指示分配养分。他决定解决方案是给他的家庭网络增加一个传感器阵列。

[Todd]的家庭自动化设置在一个加载了 Jessie OS 和 Node-Red 的 Raspberry Pi 上运行，Mosquitto 作为他的 MQTT 消息代理。有了传感器网络，[托德]就可以在他的手机上获得更新，提醒他泵是否有问题，或者营养槽是否太低了。

提议的溶液培养装置将包括一个配备有 DS18B20 防水温度传感器的 ESP8266-12，一个检测营养水平的簧片传感器，以及一个继电器板，该继电器板触发一个泵从主贮槽向生长桶注水，另一个泵从储备罐向贮槽注水。他遇到的一个早期问题是他用来让松鼠远离他的西红柿的电栅栏(如上图)，干扰了 ESP8266 的信号。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)