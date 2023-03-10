# 互动动态视频

> 原文：<https://hackaday.com/2016/08/26/interactive-dynamic-video/>

如果一张图片胜过千言万语，那么一个视频一定价值百万。然而，计算机仍然不太擅长分析视频。像 OpenCV 这样的机器视觉软件可以很好地完成某些任务，如面部识别。但是目前的软件并不擅长确定被拍摄物体的物理性质。[Abe Davis、Justin G. Chen 和 Fredo Durand]是麻省理工学院计算机科学和人工智能实验室的成员。他们正在研究一种基于视频中物体的运动来确定物体结构的方法。

这项技术依赖于振动，这种振动可以被典型的每秒 30 或 60 帧(fps)的摄像机捕捉到。它是这样工作的:一个锁定的相机被用来拍摄一个物体。该物体由于风或有人敲打它或任何其他机械手段而移动。这一动作被录了下来。该团队的软件然后分析视频，以查看物体移动的确切位置，以及移动了多少。复杂物体可以有多种振动模式。视频中使用的线框图形就是一个很好的例子。人物的手会比人物的脚振动得更多。该软件使用这些信息来构建被拍摄对象的基本模型。然后，它允许用户通过用鼠标点击和拖动来与对象进行交互。拖手会比拖脚产生更多的运动。

结果并不完美——它们让我们想起了几年前的电脑动画。然而，这是非常有希望的。这些不是在 3D 建模软件中创建的纹理线框。使用软件分析自动创建模型和骨架。团队的研究论文 (PDF 链接)包含了他们研究的所有细节。看看吧，休息后看看视频。

 [https://www.youtube.com/embed/4f09VdXex3A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4f09VdXex3A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

