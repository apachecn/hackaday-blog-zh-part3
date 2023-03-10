# 从光盘驱动器构建的激光 PCB 曝光机

> 原文：<https://hackaday.com/2016/03/14/laser-pcb-exposer-built-from-cd-rom-drives/>

[Neumi]使用 CD-ROM 驱动器作为 X 和 Y 运动平台，制造了一台 [CNC 激光器。小型 405 纳米激光器可以雕刻木头和泡沫等轻质材料。视频中展示的最酷的用途是曝光预涂的光致抗蚀剂 PCB。](https://www.youtube.com/watch?v=gs4uoEPE4Lk)

在这个项目中，Arduino、步进驱动器和激光器的价格为 61 美元(55 欧元)，[Nuemi]从垃圾箱中添加了一些部件后，得到了一台非常强大的机器。为了学习激光雕刻机背后的概念，他想避免使用现有的软件。最终，他有了一个可以将光栅扫描发送到 Arduino mega 的工作软件包。然后，mega 控制步进机和激光器之间的同步。该代码可在 GitHub 上获得。

这台机器可以在 10 分钟内完成 30×30 毫米的印刷电路板。它不会创造纪录，但它很酷，价格也不低。你可以在视频中看到从最初的调整开始失败的 PCB 排成一行，但最终的一个产生了一个非常等效于墨粉转移方法的板。休息后的视频。

 [https://www.youtube.com/embed/gs4uoEPE4Lk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gs4uoEPE4Lk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

