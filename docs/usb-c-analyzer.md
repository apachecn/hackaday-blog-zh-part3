# USB C 分析器

> 原文：<https://hackaday.com/2016/05/19/usb-c-analyzer/>

USB C 允许数据传输，但也有传输与配电相关的数据的规定。当然，只要有数据，就需要窥探数据，以便进行故障排除或逆向工程。这就是开源 [Type-C/PD 分析仪](https://hackaday.io/project/11596-usb-type-cusb-pd-analyzer)背后的想法。

[![usb-type-c-analyzer](img/e18bd242813182052a800c50a8e7f709.png)](https://hackaday.io/project/11596-usb-type-cusb-pd-analyzer) 根据项目特性包括:

*   规格支持:USB PD 2.0 和 USB Type-C 1.1
*   允许传统 USB、USB 2.0、USB 3.1 和备用模式
    通信通过
*   非侵入性，保持信号完整性和时序条件
*   USB Type-C 连接上的透明插入
*   显示数据包计时
*   监控 USB Type-C 状态机
*   将收到的数据包导出为 CSV 和专有 bin 文件格式
*   完整的 PD 包解码
*   支持实时解码和错误检测
*   嗅探两条 CC 线路上的 PD 流量
*   以人类可读的形式显示 CC 数据包
*   监控 CC 和 VBus 线电压，并以图形方式显示

在该项目的[众筹页面](https://www.crowdsupply.com/goarks/usb-c-thru)有更多细节。还有一个视频(下图)。我们[最近覆盖了 USB C 接口](http://hackaday.com/2016/04/22/hackaday-dictionary-usb-type-c/)。我们也看到了[伪造的 C 型电缆](http://hackaday.com/2016/02/04/the-usb-type-c-cable-that-will-break-your-computer/)如何对你的电脑有害。

[https://player.vimeo.com/video/155074493](https://player.vimeo.com/video/155074493)