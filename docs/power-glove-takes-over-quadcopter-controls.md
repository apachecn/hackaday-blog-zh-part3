# 动力手套接管四轴飞行器控制

> 原文：<https://hackaday.com/2016/06/06/power-glove-takes-over-quadcopter-controls/>

Gerrit 和我在湾区创客大会上参观英特尔展台时，偶遇诺兰·摩尔(Nolan Moore)，他正在展示他的作品，将任天堂的动力手套和 AR 无人机四轴飞行器(T1)融合在一起。它不仅工作正常，而且展台有一个网笼，诺兰可以独自炫耀他的作品。请查看下面的视频剪辑。

控制方案相当可爱，将手平放(手掌朝向地面)以悬停，握紧拳头并向任何方向倾斜以影响俯仰和滚动，向上或向下指以影响高度，直指并扭转手以控制偏航。我们和 Nolan 讨论过这些控件，听起来有些粗糙，但演示证明它的响应速度很快。

 [![IMG_0930](img/5bce6d2d771ee722f6061c41c0dd0cc3.png "IMG_0930")](https://hackaday.com/2016/06/06/power-glove-takes-over-quadcopter-controls/img_0930/)  [![IMG_0938](img/fa354831ab98d3d7589fcfacf6a91168.png "IMG_0938")](https://hackaday.com/2016/06/06/power-glove-takes-over-quadcopter-controls/img_0938/) 

拳王手套的内脏已经被完全移除(这也是一个有趣的浏览项目日志！)和两个新设计和制造的主板来取代它们。他从 Eagle 开始，但在将设计发送出去制作之前，他转到了 KiCAD。我真的很喜欢他用手套手腕部分的纽扣留下的脚印。

一个 Teensy LC 将所有东西整合在一起，从安装在手背上的板上的 IMU 中读取数据，以及从 flex 传感器中读取数据，以测量您的手指在做什么。它解析这些手势，并将适当的命令传递给 ESP8266 模块。AR 无人机 2.0 是 WiFi 控制的，让 ESP8266 充当控制器。

 [https://www.youtube.com/embed/aLSF4A9h8Xs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aLSF4A9h8Xs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

