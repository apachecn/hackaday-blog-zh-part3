# pike let–一台 Pi-Zero PC

> 原文：<https://hackaday.com/2017/01/25/pikelet-a-pi-zero-pc/>

旧的 10 Mbps 以太网集线器除了用作网络中的减速带之外，还有许多用途。(这一点也不好玩！)[thinkerzone]决定拆除旧的 EN104 湾网络公司的“Netgear Hub ”,将坚固的钢制外壳重新用作 Raspberry Pi Zero PC 外壳。这个被[thinkerzone]称为 Pikelet 的项目旨在成为一个“物联网服务器”,给人一种 PC 的感觉。注意:一台个人电脑，而不是一台[游戏机](http://hackaday.com/2016/11/12/pi-zero-transforms-to-game-boy/)。在他的 hackaday.io 项目中，他描述了 Pikelet 的最小功能集。

*   电源按钮–电脑需要电源按钮
*   电源和状态 LEDS–蓝色代表电源，RGB 代表可编程状态 LED
*   USB 端口–使用 Zero4U 集线器扩展 Pi Zero usb 端口
*   以太网——使用 ENC28J60 模块是最初的想法，但是在制作项目的时候烧了
*   HDMI 接入–机箱应确保 HDMI 端口可接入
*   最小存储空间——32gb 的 SD 卡被认为“足够用”
*   UART–通过 FT232 模块
*   WiFi——一个带有外部天线的 WiFi 加密狗，因为如果它在里面，金属外壳会减弱信号，所以 [WiFi 帽](http://hackaday.com/2016/04/21/usb-less-wifi-for-the-pi-zero/)不是一个选项

在软件方面，它运行最新版本的 Raspbian，并对 UART 端口和状态 LED 引脚进行了一些额外配置。

在项目日志中，我们可以跟踪[thinkerzone]在项目实施过程中的战斗，以及墨菲定律。描述性日志的用处之一是它可以提醒人们，一个看似简单的项目可能会有很多挫折。有时，一个易于描述的项目实施起来相当困难。当向其他人(非黑客/制造者)解释这些挑战时，他们会说:“这只是连接一些电线…”

感觉熟悉吗？很高兴看到别人也在经历这一切。