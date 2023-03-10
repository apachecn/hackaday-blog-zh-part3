# 遥控汽车驾驶，防爆挡板放下

> 原文：<https://hackaday.com/2016/09/16/rc-car-piloting-with-the-blast-shield-down/>

我们很多人在年轻的时候都有过一辆无线电控制的汽车，尽管很可能没有人完全掌握它。人们对壮观的撞车事故记忆犹新，如果我们真的运气不好，由于必须安装新零件，田宫先生的银行存款余额会进一步增加。

[颜仲坤]正看着他年幼的儿子玩一个无线电遥控玩具，他被双操纵杆控制布局的不直观所震惊。相比之下，当面对有第一人称视角和方向盘的游戏机时，男孩毫不犹豫地投入游戏。这一观察促使他研究将控制台方向盘引入遥控汽车，结果是[一次令人印象深刻的 FPV 沉浸式驾驶体验](https://pauldyan.wordpress.com/2016/09/07/first-person-driving-with-a-wheel/)。

[![Paul's FPV car, explained.](img/7627c29a83a21df7aef729ed1e3106c7.png)](https://hackaday.com/wp-content/uploads/2016/09/fpd_diagram.jpg)

Paul’s FPV car, explained.

他的构建采用了一个带踏板的 PS2 方向盘外围设备，并通过 PS2 护盾将其与 Arduino Uno 配对。Uno 与 Nordic NRF24L01 射频模块对话，后者与车上的另一个 NRF24L01 通信。这反过来又与车载 Arduino 微处理器对话，后者控制汽车伺服系统和速度控制器。

FPV 视频由安装在汽车上的多旋翼飞行世界的微型摄像机和发射器提供，并通过 5GHz 将其图像传输到一套监控护目镜。遗憾的是，他似乎没有发布任何相关的软件，尽管我们怀疑如果你想亲自尝试的话，会不会有太大的挑战。

下面的视频显示了这辆车的运行，伴随着他年幼的儿子过度热情的加速和碰撞。他告诉我们，这是一种类似于在现实世界中玩赛车游戏的体验，看过视频后，我们希望可以一试。

 [https://www.youtube.com/embed/DCkqqOrIXCw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DCkqqOrIXCw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们在过去展示过另一款方向盘控制的 FPV 汽车,尽管这款更优雅。然而，两者都无法击败模型鹰教练机的 FPV 飞行，其中[是伺服控制的飞行员的手，以获得额外的真实感](http://hackaday.com/2014/06/18/rc-plane-flies-with-a-cockpit-view/)。