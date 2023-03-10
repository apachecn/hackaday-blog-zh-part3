# magic shifter 3000:15 年历程的超工程 POV 棒

> 原文：<https://hackaday.com/2016/08/22/magicshifter-3000-an-over-engineered-pov-stick-has-come-a-long-way/>

3 个黑客，16 个 led，15 年的开发，一个目标:一个适合你口袋的视觉暂留显示棒。那就是 [magicShifter 3000](https://hackaday.io/project/9668-magicshifter-3000) 。当挥动时，这个 10 厘米(4 英寸)长的小手持设备利用视觉暂留效应在半空中绘制稳定的图像。现在，该项目已经达到了另一个里程碑:生产。

自从 2002 年绿色 LED 条形图问世以来，这种设计已经有所发展。当前版本具有 16 个 APA102(又名 dot star)RGB led、一个 ESP-12E WiFi 模块、一个恩智浦加速度计/磁力计、强制 Silabs USB 接口，以及一个 LiPo 电池和充电器，具有令人印象深刻的电源管理部分。Arduino 友好的固件实现了图像稳定，以及基于 React 的 web 界面，用于上传和绘制图像。

 [![x-default](img/542acf5da73277409dcb204c92a85bfb.png "x-default")](https://hackaday.com/2016/08/22/magicshifter-3000-an-over-engineered-pov-stick-has-come-a-long-way/x-default/)  [![03_povhearts](img/582af9cb44774e132541a5ac2fac0d81.png "03_povhearts")](https://hackaday.com/2016/08/22/magicshifter-3000-an-over-engineered-pov-stick-has-come-a-long-way/03_povhearts/)  [![ms3000-pcb-and-assembled](img/2d8a4c1e5571d5c663ef70e37ff8842e.png "ms3000-pcb-and-assembled")](https://hackaday.com/2016/08/22/magicshifter-3000-an-over-engineered-pov-stick-has-come-a-long-way/ms3000-pcb-and-assembled/) 

在 Seeedstudio 对之前的原型进行试验后，该团队在保加利亚制造了 500 台。他们的项目让他们在硬件制造中来回穿梭。从为坚如磐石的设计消除微小的缺陷，到构建测试平台和编写测试程序，再到产出管理。传统上，所有 magicShifter 外壳都是 3D 打印的，因此[Overflo]和[Martin]轮班工作，开始打印 500 张照片，每张照片大约需要 50 分钟才能完成。打印机仍在嗡嗡作响，但组装好的单元可以在他们的[商店](https://hackerspaceshop.com/products/magicshifter3000)买到。

 [![24067877080_b944fe8d6d_o](img/e2e1535e8a4f70940f05bc592cbe5318.png "24067877080_b944fe8d6d_o")](https://hackaday.com/2016/08/22/magicshifter-3000-an-over-engineered-pov-stick-has-come-a-long-way/24067877080_b944fe8d6d_o/)  [![24337122776_d32cbed995_o](img/1f1bba914bf2d4853082a8606c257ba2.png "24337122776_d32cbed995_o")](https://hackaday.com/2016/08/22/magicshifter-3000-an-over-engineered-pov-stick-has-come-a-long-way/24337122776_d32cbed995_o/)  [![9779981363_84a8453023_o](img/e417e03bae88287ca321bc1e57f963c8.png "9779981363_84a8453023_o")](https://hackaday.com/2016/08/22/magicshifter-3000-an-over-engineered-pov-stick-has-come-a-long-way/9779981363_84a8453023_o/) 

多年来，magicShifter 作为过度设计的开放式硬件口袋 POV 棒赢得了声誉和[资金](http://blog.magicshifter.net/#post434454625)。如果你住在欧洲，很有可能你已经看到了众多原型装置中的一个，或者在一次随机黑客活动中遇到了[Phillip Tiefenbacher]又名[wizard23],得到了 magicShifter 的简短演示。该项目总是记录硬件黑客的现状:每年，它都变得更小，更好，并反映了哪些部分碰巧流行。

![magicshifter-timeline](img/8ffa64b76636dee64964acc81e27946a.png)

[固件](https://github.com/magicshifter/MS3000)和 [3D 可打印外壳](https://github.com/magicshifter/MS3000-3DPrinted)仍然是开源的，最新设计的[原理图](https://github.com/magicshifter/MS3000-Schematic/raw/master/MS3000_V_1_23.pdf)可以在 GitHub 上找到。虽然，你会徒劳地搜索布局或 Gerber 文件。大批量生产然后被廉价克隆产品淘汰的风险给这个项目留下了印记，让 magicShifter 再次反映了硬件黑客的当前全球化状态。然而，我们很高兴 POV 项目的基石仍然存在。看看下面朗朗上口的解释性视频。

 [https://www.youtube.com/embed/37QBSWLmHT8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/37QBSWLmHT8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

