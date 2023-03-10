# 将 Arduino 用于四轴飞行器频谱分析仪

> 原文：<https://hackaday.com/2016/01/26/using-arduino-for-quadcopter-spectrum-analyzers/>

第一人称视角(FPV)飞行，通过给地面上的肉加上摄像机、视频发射器和视频护目镜，是体验遥控飞行的最佳方式之一。只需几百美元，这是你能得到的最接近长出翅膀并在当地公园的树上飞翔的东西。最受欢迎和最便宜的方法之一是 Boscam RX5808 无线接收器，这是一个 9 美元的模块，能够通过 5.8GHz 无线电从飞机上下载视频。Stock，这个无线电模块还可以，但经过一些修改，[它可以变成一个非常好的接收机，带有频谱分析仪和自动扫描](https://dronegarageblog.wordpress.com/2016/01/20/arduino-5-8ghz-rx5808-module-open-source-fpv-receiver/)。

Boscam RX5808 有三个 DIP 开关，允许八个不同的通道接收视频，这是大多数 RC 爱好者止步的地方。但该模块还有一个非常强大的 SPI 接口，通过添加一个简单的 Arduino，可以释放该接收器的全部功能。

构建的核心软件是[markohoepken]的 [rx5808-pro](https://code.google.com/p/rx5808-pro/) 和 [rx5808_pro_osd](https://github.com/markohoepken/rx5808_pro_osd) ，以及[crazyheea]的 [rx5808-pro-diversity](https://github.com/sheaivey/rx5808-pro-diversity) ，以实现 rx5808 接收机中可用的所有功能。有了现成的 LCD，这些乱七八糟的电线和电路板就变成了自动扫描频谱分析仪，它也能够将无人机的视频放到屏幕上。

[garagedrone]将整个构建的非常完整的演示视频放在一起。你可以看看下面。

 [https://www.youtube.com/embed/uMBqOuJBiWQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uMBqOuJBiWQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

