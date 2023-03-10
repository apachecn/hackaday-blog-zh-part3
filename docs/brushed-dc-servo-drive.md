# 刷 DC 伺服驱动器

> 原文：<https://hackaday.com/2016/02/13/brushed-dc-servo-drive/>

无刷 DC 电机及其相关的驱动电子设备往往昂贵且复杂。[Ottoragam]正在寻找一种更便宜的替代品，并建造了这个[有刷 DC 电机伺服控制器](https://hackaday.io/project/9433-brushed-dc-servo-drive)，结果看起来很有希望。休息之后请看视频。

他需要一个低成本的闭环驱动来实现自制的 CNC。伺服驱动器能够在高达 36 V 的电压下向有刷 DC 电机提供高达 7 A 的连续电流，其输出功率约为 250 W 或 1/3 HP。它利用正交编码器的反馈进行闭环控制。该驱动器接受简单的步进和方向信号，使其易于与微控制器接口，并将其用作定位应用中步进电机的替代品。所有的控制都由 ATmega328P 处理。它接收输入信号和编码器数据，进行 PID 控制，并通过 [DRV8701 全桥 MOSFET 驱动器](http://www.ti.com/lit/ds/symlink/drv8701.pdf)驱动电机。还有一些错误检测电机过电流和驱动器欠压。H 桥配置中的四个[irfh 7545 MOSFET](http://www.irf.com/product-info/datasheets/data/irfh7545pbf.pdf)构成输出功率级。

这项工作仍在进行中，[Ottoragam]在他的愿望清单中还有一些未完成的特性。其中重要的包括添加一个串行接口以方便调整 PID 参数，以及创建一个 GUI 以方便调整。这个项目是开源的，所有的源文件都可以在他的 [Github 仓库](https://github.com/ottoragam/Brushed-DC-Servo-Drive)中找到。该板大多是表面贴装，但无源器件都是 0805，所以应该很容易组装。微控制器的 QFN 足迹可能是唯一棘手的问题。[Ottoragam]希望能有一些测试人员来测试他的电路板，也许还能得到一些有用的意见来改进他的设计。

 [https://www.youtube.com/embed/K9Jn150wsNk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K9Jn150wsNk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

