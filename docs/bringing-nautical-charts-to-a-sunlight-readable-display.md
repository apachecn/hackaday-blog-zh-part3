# 将航海图显示在阳光下

> 原文：<https://hackaday.com/2016/03/05/bringing-nautical-charts-to-a-sunlight-readable-display/>

道路地图仍在发布，但如果你有智能手机和谷歌地图，你就不会知道了。十年前拿到驾照的大多数飞行员都是从纸质地图开始的，但如今 iPad 主宰了驾驶舱。在一张 SD 卡上，你可以存储地球表面每平方英里的地图。[Erland]认为是时候让数字地图走向航海了，于是[造了一个类似平板电脑的设备，在航行时显示海图](https://hackaday.io/project/9471-pi-chart)。

当然，圆周率图表是由运行几十行 JavaScript 和 HTML 的 Raspberry Pi 驱动的。软件方面，除了新的[基于 OpenGL 的渲染](https://www.youtube.com/watch?v=DAsFxH2Vcv8)允许超平滑的地图渲染之外，没有太多的构建。

硬件是这个构建变得有用的地方，为此，[Erland]正在使用日光可读像素 Qi 显示器。锂离子电池提供大约 10 个小时的运行时间，蓝牙 GPS 加密狗告诉 Pi 船只的确切位置。

 [https://www.youtube.com/embed/DAsFxH2Vcv8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DAsFxH2Vcv8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



* * *

![Raspberry_Pi_LogoSmall](img/87d7e34f7ac8cc3ae6c8619ad96c149e.png)

树莓派零竞赛由 Hackaday 和 Adafruit 主办。奖品包括 Adafruit 的树莓派零和 Hackaday 商店的礼品卡！
[查看所有参赛作品](https://hackaday.io/submissions/adafruitpizerocontest/list) || [现在就进入你的项目吧！](https://hackaday.io/contest/9326-adafruit-pi-zero-contest)