# 旋转框架将改变您的垂直图像视图

> 原文：<https://hackaday.com/2016/10/17/rotating-frame-will-change-your-view-of-vertical-images/>

[Tim]厌倦了将他的纵向数码照片硬塞进风景专用的相框中。由于找不到商业解决方案，他用一台 27 英寸的液晶电视制作了自己的旋转数码相框。

它使用一个 Raspi 3 在一个巨大的 SD 卡上查找[Tim]的照片。他最初想让 Pi 从 Google Photos 中提取图片并随机显示，但是 API 在这个方向上不起作用。相反，Python 脚本查看 SD 卡上的图片，并确定每张图片是横向还是纵向的。如果照片是在纵向模式下拍摄的，显示屏将旋转 90 度。旋转由 Arduino、步进电机和一些 3D 打印的人字齿轮处理。第一个版本有点嘈杂，所以[Tim]用柔性细丝重新打印了电机座和小齿轮。

[Tim]自己设计了底座和框架，并用激光从桦木胶合板上切割下来。我们喜欢他考虑到前面沉重，他用丙烯酸覆盖高压电路，以减轻电击的风险。所有的代码和设计文件都可以在他的项目页面上找到。跳过去观看简短的演示，然后走一走，留下来观看六分钟的幻灯片。

 [https://www.youtube.com/embed/VA_kyvEj8nw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VA_kyvEj8nw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/fsBi4q-bmz8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fsBi4q-bmz8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [![enpi](img/7d6ec196fe187128af3d9fd57fefe510.png)](https://hackaday.io/contest/15532-enlightened-raspberry-pi-contest)

**铺平学习道路，赢取奖品:**

* * *

### 进入[启蒙树莓 Pi 大赛](https://hackaday.io/contest/15532-enlightened-raspberry-pi-contest)！

只要教我们如何用圆周率做一些了不起的事情。([查看更多条目](https://hackaday.io/submissions/enlightened-raspberry-pi/list))