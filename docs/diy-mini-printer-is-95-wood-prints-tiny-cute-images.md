# DIY 迷你打印机是 95%的木材，打印微小可爱的图像

> 原文：<https://hackaday.com/2016/12/12/diy-mini-printer-is-95-wood-prints-tiny-cute-images/>

这个由[叶戈尔]设计的 DIY 64×64 图形打印机在设计上是笔式绘图仪的一部分，在操作上有点像点阵，并且巧妙地设计成使用未经修改的 9G 伺服系统。[项目页面](https://geektimes.ru/post/262098/)全是俄文(这里翻译成英文)但是有大量的照片让操作和设计清晰可见。虽然几乎整个建筑都是由激光切割的木材制成，但[叶戈尔]说激光切割机是可选设备。第一个版本完全是用手工工具切割的。

[![screenshot-2016-12-06-10-49-13](img/365d50ed0b37c10dc39a188f43e09e40.png)](https://hackaday.com/wp-content/uploads/2016/12/screenshot-2016-12-06-10-49-13.png) 通过串行线驱动的小型 DIY 数控机器通常使用 Arduinos 和 CD-ROM 驱动器(如这个[泡沫切割器](http://hackaday.com/2015/08/24/hot-wire-cnc-foam-cutter-from-e-waste/)或这个[激光切纸机](http://hackaday.com/2014/03/16/a-3-axis-paper-cutting-mini-laser/))但这个构建使用自己定制的齿轮齿条系统，并有一些很棒的小细节，如弹簧夹，用于将纸张固定在打印垫上。

框架和零件(包括所有齿轮)由 4 毫米胶合板激光切割而成，该装置由三个小型伺服系统驱动。一个简单的 Java 程序处理图像，Arduino UNO 处理底层控制。下面嵌入了所有活动的视频。

 [https://www.youtube.com/embed/AlBPFC41FsM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AlBPFC41FsM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



说到使用廉价伺服系统的齿轮齿条式设置，这个想法被[带到了下一个层次，这是一个使用未经修改的伺服系统的 3d 打印线性致动器](https://hackaday.io/project/10578-3d-printed-linear-servo-extender)的设计。