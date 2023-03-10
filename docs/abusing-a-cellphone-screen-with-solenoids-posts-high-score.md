# 滥用手机屏幕与螺线管张贴高分

> 原文：<https://hackaday.com/2016/08/25/abusing-a-cellphone-screen-with-solenoids-posts-high-score/>

这款拥有计算机视觉和两个螺线管“手指”的[Raspberry Pi 2](http://blog.tkjelectronics.dk/2016/08/raspberry-pi-playing-zombuster)在 2015 年末的一款手机游戏上获得了高得离谱的分数，但直到最近【Kristian】才完成了该项目的详细文档。

这个项目是为图像分析和计算机视觉课程开发的，并不是真的关于在手机游戏中作弊。它甚至不是智能手机屏幕的机器人界面；这是一个开发和展示他正在学习的图像分析理论的平台，计算机视觉部分不是一个简单的工作。OpenCV 被用作访问相机的基础，但没有使用内置过滤器。所有的图像分析都是从头开始实施的。

这个游戏很简单。人类和僵尸分两列向下移动。僵尸(绿色)应该得到一个屏幕点击，但不是人类。Raspberry Pi 相机拍摄智能手机屏幕的照片，对其应用 HSV 过滤器，以过滤掉除绿色物体(僵尸)之外的所有东西。仅此一点就足以获得一些基本的结果，但还不足以真正可靠和可重复。因此，在挑选出绿色物体之后，是一系列附加的过滤。细节在[【克里斯蒂安】的博客文章](http://blog.tkjelectronics.dk/2016/08/raspberry-pi-playing-zombuster/)中有所报道，但是[项目](https://github.com/Lauszus/ImageAnalysisWithMicrocomputer30330/raw/master/docs/KristianSlothLauszus_s123808_2015.pdf)的最终报告(PDF)才是真正的细节。

如果你感兴趣的主要是看一台机器打出完美的胜利，下面的视频显示一切运行顺利。重击声让屏幕看起来像是受到了很大的虐待，但[Kristian]提到那实际上是来自螺线管的噪音，而不是它们与触摸屏斗争的产物。这种设置可以很容易地在不同型号的手机上测试应用程序——这在历史上花费了相当多的钱。

如果你对计算机视觉部分使用的原因和方法的本质细节感兴趣，一定要仔细阅读[Kristian]的[github 知识库](https://github.com/Lauszus/ImageAnalysisWithMicrocomputer30330)，那里存放着关于该项目的所有内容(包括前面提到的最终报告。)

 [https://www.youtube.com/embed/B6UYqpyV3GU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B6UYqpyV3GU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们也看到了像这个[乐高机器人玩 iPad](http://hackaday.com/2014/04/17/lego-robot-plays-games-for-you-as-you-sleep/) 和这个 [Arduino 使用伺服系统在正确的时间点击按钮](http://hackaday.com/2016/06/22/cheating-at-video-games-arduino-edition/)这样的项目，这表明目标并不总是研究。有时候，目标只是让一台机器在你睡觉的时候完成一项重复的任务。