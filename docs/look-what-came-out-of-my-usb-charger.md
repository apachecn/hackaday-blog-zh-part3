# 看看我的 USB 充电器出来了什么！

> 原文：<https://hackaday.com/2017/10/21/look-what-came-out-of-my-usb-charger/>

快速充电是高通通过 USB 技术传输电力的技术，于 2013 年推出，经过几个版本的发展，提供了越来越高的电力传输水平。当前版本——qcv 3.0——在 3.6 V 至 20 V 的电压水平下提供 18 W 功率，此外，连接的器件可以协商并请求这两个限值之间的任何电压，步进为 200 mV。经过一番修补，【文森特·德孔尼克】成功地[将快速充电 3.0 充电器变成了可变电压电源](http://blog.deconinck.info/post/2017/08/09/Turning-a-Quick-Charge-3.0-charger-into-a-variable-voltage-power-supply)。

他的博客文章对快速充电生态系统进行了很好的介绍和介绍。[Vincent]在阅读了[Septillion]和[Hugatry]关于[将 QCv2.0 充电器引入可变电压源](https://hackaday.com/2017/06/02/usb-charger-persuaded-to-variable-voltage-source/)的工作后受到了启发，该可变电压源可以输出 5 V、9 V 或 12 V。他在他们的工作基础上添加了 QCv3.0 功能，创建了一个新的[qc3 控制库](https://github.com/vdeconinck/QC3Control)。

为了掌握引擎盖下发生的事情，他首先获得了几个 QC2 和 QC3 充电器，将它们连接到 Arduino，并运行 QC2Control 库以查看它们如何响应。有一些意想不到的结果；在 QC 模式下，每次交换 5 V 握手请求时，充电器复位，其输出降至 0 V，然后稳定回固定的 5 V 输出。之后，需要一个新的握手来恢复到 QC 模式。深入研究后，他了解到快速充电系统依赖于在 USB 端口的 D+和 D-端子上检测到的特定控制电压来确定模式和输出电压。这些控制电压由连接到微控制器 GPIO 引脚的电阻网络产生。在建立了一个旨在更接近地产生推荐控制电压的新电阻网络，然后进一步优化它，只使用两个微控制器引脚后，他能够让它按预期工作。有了所有这些信息，他开始设计 qc3 控制库，可以在 GitHub 上下载。

由于他的新库和双输出 QC3 充电器，他能够通过让 Arduino 快速发出电压变化请求，在他的 Rigol 上生成 Jolly Wrencher。

 [https://www.youtube.com/embed/2FVUbehwVQs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2FVUbehwVQs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

