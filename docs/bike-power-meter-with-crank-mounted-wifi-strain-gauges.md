# 带曲柄安装的 WiFi 应变仪的自行车功率计

> 原文：<https://hackaday.com/2016/04/03/bike-power-meter-with-crank-mounted-wifi-strain-gauges/>

在任何赛车运动中，你对引擎的性能了解得越多，车手在比赛中的表现就可能越好。这也适用于自行车，司机恰好也是引擎。市场上有很多便宜的自行车电脑，但测量功率输出的高端仪表有点贵。[chiprobot]希望通过自制的低成本自行车功率表来改变这种状况。

该项目似乎仍处于概念验证阶段，但这肯定是一个有趣的概念。股票曲柄臂小心翼翼地安装了两对微小的应变仪。应变计以惠斯通电桥的方式连接，每对中有一个应变计垂直安装在曲柄上，作为静态参考。电桥的输出馈入 HX711 仪表放大器。下面的演示视频展示了电桥和 24 位放大器的灵敏度。

目标是通过 WiFi 和一对 ESP8266 模块将曲柄数据发送到车把安装的用户界面。我们喜欢自行车区域网络的想法，但[chiprobot]在所有这些设备的加固和防风雨方面还有很多工作要做。我们一定会关注这个项目。与此同时，我们可以从去年报道的自行车电表项目中学到很多东西。

 [https://www.youtube.com/embed/ZZnG135o4ZQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZZnG135o4ZQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

