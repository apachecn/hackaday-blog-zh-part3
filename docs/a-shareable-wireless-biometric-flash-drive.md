# 一个可共享的无线生物识别闪存盘

> 原文：<https://hackaday.com/2016/01/15/a-shareable-wireless-biometric-flash-drive/>

无线存储和生物认证都是已解决的问题。但正如[Nathan]和[Zhi]所注意到的，没有一个单一的存储解决方案可以同时兼顾这两者。在[Bruce Land]的 ECE 4760 的最后一个项目中，[他们试图在预算紧张的情况下将这两个想法结合起来](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2015/nds55_zt27/nds55_zt27/nds55_zt27/index.html)，同时尽可能多地添加额外功能，如有机发光二极管和感应线圈充电。

![final_product_600](img/650a7090f9a85f85bc8f5af953144a3c.png)他们的解决方案可由多达 20 个不同的人使用，每个人在存储单元中获得一片 SD 卡。有两个物理片，一个基站和无线存储单元本身。基站通过 USB 连接到主机，包含一个用于串行直通的 Arduino 和一个用于与存储端通信的 nRF24L01+模块。存储驱动器的组件被塞在一个透明的塑料盒里。这不仅看起来很酷，而且不需要切割端口来安装指纹传感器和有机发光二极管。传感器通过盒子读取用户凭证，身份验证状态显示在有机发光二极管上。文件通过必不可少的 PIC32 通过第二个 nRF24L01+与 SD 卡进行双向传输。

指纹授权为该单元提供了一些物理安全性，但是[Nathan]和[Zhi]想要添加一个加密方案。由于预算限制和时间限制，数据传输不是很快(840 字节/秒)，但这并不是 nRF 模块的真正过错——大部分传输协议是在软件中实现的，他们只是用完了调试时间。也没有文件系统架构。尽管有这些缺点，[Nathan]和[Zhi]为无线生物识别存储创造了一个可行的概念证明，他们对此感到满意。休息后参观一下。

 [https://www.youtube.com/embed/zBD0YH_G21c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zBD0YH_G21c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

