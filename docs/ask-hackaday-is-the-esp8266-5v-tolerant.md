# 问 hack aday:ESP8266 的 5V 耐压吗？

> 原文：<https://hackaday.com/2016/07/28/ask-hackaday-is-the-esp8266-5v-tolerant/>

ESP8266 是占统治地位的 WiFi 神奇芯片，迅速巩固了其作为整个无线设备生态系统的首选平台的声誉。在性能与价格比较方面，没有什么能打败 ESP8266，这种微小的芯片甚至正在进入商业产品。对于硬件修补者来说，这也是一个神奇的设备，导致了数千个围绕这个微小神奇设备的自制项目。

在 ESP8266 的所有技术文档、摘要和描述中，ESP8266 都被称为 3.3V 器件。虽然我们已经进入 3.3V 逻辑时代，但仍有数量惊人的电路板和硬件仍然使用 5V 逻辑。在 Hackaday.io 堆栈上，[Radomir]正在质疑这个基本假设。[他想知道 ESP8266 到底能不能耐受 5V 电压](https://hackaday.io/page/2024-esp8266-is-5v-tolerant-after-all)。如果是的话，太好了。我们不需要电平转换器，ESP 与 USB TTL 串行适配器的接口变得更加容易。是的，如果项目的其余部分在 5V 下运行，您仍然需要使用调节器，但如果引脚支持 5V，那么 ESP8266 与各种硬件的接口就变得非常容易。

[Radomir]关于 5V 耐受输入可能性的证据来自 Espressif 的官方数据表中的细微差异，以及 Espressif 意识到他们将出售多少这些芯片之前社区翻译的数据表。

5V 耐受引脚的最佳证据可能来自现实世界的经验——如果你能连续几个月用 5V 驱动一个引脚而不出故障，这种说法可能有些道理。不过，这还不确定。仅仅因为一个设备可以在 5V 输入引脚下工作几个月，并不意味着它在未来不会出现故障。到目前为止，已经有几个人站出来发言，[展示了直接连接到 Arduino](https://hackaday.io/project/11922-home-automation-on-the-cheap) 的 5V 引脚上的 esp，这些 esp 在几个月的服务后仍然可以工作。如果这是 5V 耐受设计的证据，或者仅仅是运气完全是另一回事。

虽然 Espressif 的官方数据表列出的最大 V [IH] 为 3.3V，但最大规格很少是真正的最大值——你总是可以更用力地推动一个部件，而不会出现裂缝。不幸的是，除非我们从 Espressif 的工程师那里听到一些东西，否则我们不会知道 ESP8266 是否能够承受 5V 电压，它是否能够可靠地处理 5V 信号，或者 5V 信号是否是最终杀死芯片的好方法。

幸运的是，一些 Espressif 工程师阅读 Hackaday，这也是我们问 Hackaday 专栏的全部内容。欢迎他们和花生画廊的其他人一起在下面用假名附和。否则， [ESP8266 已经被解盖](http://zeptobars.com/en/read/Espressif-ESP8266-wifi-serial-rs232-ESP8089-IoT)；有没有芯片检测专家可以证明 GPIO 的 5V 容差？我们也有兴趣听听压力测试引脚容差的想法。