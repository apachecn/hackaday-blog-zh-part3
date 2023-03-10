# OpenCV 炮塔跟踪运动，粉碎气枪弹丸

> 原文：<https://hackaday.com/2017/08/04/opencv-turret-tracks-motion-busts-airsoft-pellets/>

在争夺办公室主导地位的永恒斗争中，运动跟踪气枪/Nerf/无论什么，自主炮塔似乎是核选项。[Aaron]和[Davis]建造了一个[运动跟踪炮塔](https://hackaday.io/project/18665-motion-tracking-airsoft-turret)，它使用 openCV 来检测运动，然后点击继电器触发枪支。

有一个树莓 Pi 控制罗技 C210 Pi 兼容的网络摄像头，Pi 的步进器帽子控制两个 NEMA 步进器瞄准枪。设计简单而优雅，有一个旋转的底座和一个可以升降武器的组件。

openCV 引起了我们的兴趣。我们希望看到一个 openCV 驱动的带颜色检测的炮塔，这样你自己的队伍就不会和你倒霉的敌人一起被炸了。或者如果守卫你的隔间，一点点 openCV 面部识别怎么样？

如果你想尝试自己的项目，[Aaron]和[Davis]在他们的 Hackaday.io 页面上展示了他们是如何构建项目的，他们的 [Python 脚本](https://github.com/HackerHouseYT/Tracking-Turret)可以在 GitHub 上找到。否则，看看我们之前发布的[反恐精英气枪机器人](http://hackaday.com/2014/08/24/the-counter-strike-airsoft-robot/)、[气枪哨兵枪](http://hackaday.com/2015/12/06/airsoft-sentry-gun-keeps-your-house-guarded/)和[由 Slack](http://hackaday.com/2016/02/15/nerf-turret-controlled-by-slack/) 驱动的 Nerf 炮塔。

 [https://www.youtube.com/embed/HoRPWUl_sF8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HoRPWUl_sF8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

