# Hackaday 获奖作品:无头 Linux 系统的接口

> 原文：<https://hackaday.com/2016/05/28/hackaday-prize-entry-a-hat-for-the-headless-linux-system/>

将一个无头的 Raspberry Pi 连接到无线网络可能是一个非常矛盾的情况。要将其连接到网络，您需要打开一个 SSH 连接来配置无线端口。但是要做到这一点，你首先需要一个网络连接。当然，您仍然可以使用 USB 转 UART 适配器或 Pi 的以太网端口(如果存在的话)获得命令行访问，但是[Arsenijs]为他的 Hackaday 奖品条目设计了一个更方便的解决方案:[pyl ci Linux 控制接口](https://hackaday.io/project/10001-pylci-linux-control-interface)。

他的解决方案是用 Python 编写的软件框架，使用字符显示和按钮来制作简单的硬件界面。这允许你从一个有条理的点击和滚动菜单中配置 Raspberry Pi——或任何其他 Linux SBC——的所有重要方面。实现了一大堆有用的工具:有一个网络工具可以扫描和连接到 WiFi 网络。一个 systemctl 工具，允许您管理系统上运行的服务，这在您需要重新启动停滞的服务时特别有用。分区工具有助于查看和卸载海量存储设备。他甚至计划添加一个文件系统浏览器。

通过他的[开源](https://github.com/CRImier/pyLCI)项目，【Arsenjs】旨在通过从零开始实现基本接口功能来缩短嵌入式项目的开发时间。事实上，在无数的场景中，一个基本的显示界面可以有很大的价值。鉴于伟大的[项目文档](http://pylci.readthedocs.io/en/latest/)和事实上它可以与几乎任何 Arduino 或 Raspberry Pi LCD-button-hat 或 shield 一起工作，我们确信这将会被大量使用。享受视频！

 [https://www.youtube.com/embed/2hem8to5hA0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2hem8to5hA0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[编辑:根据项目业主提供的信息进行了一些更正。]

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)