# 视觉扫描仪将障碍物变成盲文

> 原文：<https://hackaday.com/2017/06/09/visual-scanner-turns-obstacles-into-braille/>

麻省理工学院的这个有趣项目旨在通过使用触觉反馈带、胸前安装的传感器和盲文显示器，利用技术帮助视力受损的人导航。

这种皮带由一个振动电机组成，该电机由一个看起来像树莓 Pi(无论如何是原型)的东西控制，并连接有一个距离传感器和摄像头。核心算法旨在从摄像头和距离传感器获取输入，以计算到障碍物的距离，并启动正确的电机来提醒用户——这是相当预期的事情。然而，该项目有一个更高的目标:协助识别和使用椅子。

为了检测座位和手臂，该算法会寻找三个彼此靠近的水平表面，特别注意确保椅子没有被占用。该研究发现，与拐杖结合使用，该系统明显帮助用户在真实的环境中导航，通过轻微和严重的碰撞进行测量。与单独使用该系统或单独使用拐杖相比，用户记录的碰撞明显减少。该项目还要求安装在腰带上的盲文显示器向用户传递更复杂的信息。

我们在 HaD 已经跟进了几个盲文项目，包括一个[可刷新盲文显示器](http://hackaday.com/2016/04/28/refreshable-braille-display-and-braille-keyboard/)，一台带有[盲文显示器和键盘的计算机](http://hackaday.com/2015/05/31/hackaday-prize-entry-a-braille-computer/)，以及这台[盲文打印机](http://hackaday.com/2014/02/24/braigo-a-lego-braille-printer/)。

 [https://www.youtube.com/embed/R6Pjbk9w2Jk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/R6Pjbk9w2Jk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [麻省理工学院新闻](http://news.mit.edu/2017/wearable-visually-impaired-users-navigate-0531)