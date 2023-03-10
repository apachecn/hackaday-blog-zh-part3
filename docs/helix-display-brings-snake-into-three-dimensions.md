# 螺旋显示器将蛇带入三维空间

> 原文：<https://hackaday.com/2017/06/07/helix-display-brings-snake-into-three-dimensions/>

任何时候，只要有人找到一种很酷的 3D 显示方式——还有不酷的方式吗？—我们在船上。Instructables 用户[Gelstronic]的方法包括一系列旋转道具来玩 3D 游戏 Snake。

螺旋显示器由 12 个支柱组成，使用 3D 打印部件精确间隔和角度，每个支柱都有 12 个可单独寻址的 led。由 36 个 led 组成的四个控制组由 P8XBlade2 propeller 微控制器控制，每次旋转产生的 17280 个体素足以产生可识别的图像。

为了给 led 供电，[Gelstronic]使用了通常用于手机的无线充电线圈，将 10 瓦的功率传输到螺旋阵列。无刷电机让东西旋转，而 Arduino 通过编码器控制速度和位置。所有代码的链接都可以在[项目页面](http://www.instructables.com/id/PropHelix-3D-POV-Display/)上找到，但是我们在休息之后会有视频展示。

 [https://www.youtube.com/embed/cA4L49habEY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cA4L49habEY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



有一些[明显更容易](http://hackaday.com/2015/02/08/dead-simple-hologram-effect/)的方法来实现立体显示，也有一些感觉像是直接从视频游戏中撕下来的[。](http://hackaday.com/2017/05/13/say-hello-to-this-cortana-hologram/)

【谢谢提示，意泰！]