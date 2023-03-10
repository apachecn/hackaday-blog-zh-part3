# 宜家灯，树莓皮是室内最智能的灯泡

> 原文：<https://hackaday.com/2018/05/16/ikea-lamp-with-raspberry-pi-as-the-smartest-bulb-in-the-house/>

我们喜欢破解宜家产品，惊叹树莓派的创意，沐浴在视频投影的光芒中。[Nord Projects]将我们最喜欢的东西组合成了 [Lantern](http://nordprojects.co/lantern/) ，这个名字和它使用的宜家灯具一样简约。但结果几乎是神奇的。

这个建筑的关键部件是一个紧凑的激光照明视频投影仪，它的图像总是在焦点上。Lantern 的主要用户界面是移动灯，在投射到不同表面的不同信息通道之间切换。如果用户每次移动后都必须重新对焦，这将是一个麻烦，但无焦点激光投影仪消除了这种摩擦。

Lantern 的软件通过加速度计检测到用户物理改变灯的方向。某些通道在真实世界对象的顶部投影信息叠加。Lantern 从 Raspberry Pi 相机获得反馈来定位覆盖图，而不是期望它的人类用户执行精确的对齐。

说到软件,[Nord Projects]展示的 Lantern 是我们在之前提到过的[谷歌](https://hackaday.com/2016/12/14/google-scrubs-brillo-reveals-android-things/)[Android Things](https://experiments.withgoogle.com/lantern)旗下的一个展示项目。但是没有任何东西把硬件和谷歌直接联系起来。因为这个项目是开源的，有关于 [Hackster.io](https://www.hackster.io/nord-projects/lantern-9f0c28) 和 [GitHub](https://github.com/nordprojects/lantern) 的信息，所以选择权在你。像他们一样用 Google 构建一个，或者编写自己的软件来绑定到不同的基础设施(MQTT？)，或者根本没有连接的独立单元。

我们让宜家的灯具被黑客攻击成 LED 阵列，我们让树莓派(Raspberry Pi)内置到视频投影仪中。现在他们已经走到了一起，下一步是什么？也许[会为机动灯笼加入一些伺服系统](https://hackaday.com/2017/01/04/from-ikea-lamp-to-robot-arm/)？

 [https://www.youtube.com/embed/43cJ0XZKiaY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/43cJ0XZKiaY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via[Raspberrypi.org](https://www.raspberrypi.org/blog/augmented-reality-projector/)