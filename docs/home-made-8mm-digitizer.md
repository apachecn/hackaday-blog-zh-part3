# 国产 8 毫米数字化仪

> 原文：<https://hackaday.com/2016/03/18/home-made-8mm-digitizer/>

8 毫米的电影造型正在回归，但发行是一个问题。[Heikki Hietala]想要一种简单的方法来数字化捕捉他制作的 8 毫米电影。因此，他用一台 Arduino、一台廉价的佳能相机和一台旧的 8 毫米胶片相机的内脏制造了一台 8 毫米数字化仪。当你扔进一些 3D 打印组件和一些奇怪的电子设备时，你会得到一个令人印象深刻的构建，以令人印象深刻的速度和质量拍摄 8 毫米胶片。

这个构建从运行 CHDK(佳能 Hack 开发工具包)的佳能 Ixus 5 相机开始，以锁定设置。它通过微距镜头指向胶片，因此胶片的每一帧都充满了整个画面。Arduino 然后使用 USB 电缆触发相机拍照。同一个 Arduino 还控制着一个马达，这个马达可以卷胶卷，并从他抢救回来的相机中触发胶片门。通过反转功能并用伺服电机触发它，他可以很容易地封闭框架的边缘，这样就不会有杂散光穿过薄膜材料造成任何问题。一旦摄像机捕捉到了胶片上的每一帧，他就把捕捉到的图像输入 Blender，Blender 对图像进行处理，然后输出最终的电影。

这是一个非常令人印象深刻的整体建设。[海基]显然花了很多心思，整个事情看起来运行得非常高效和迅速。捕捉到的视频看起来很棒，正如你从[这个样本](https://www.youtube.com/watch?v=uCxfIB59b1E)中看到的。使用回收的电影大门是一个明智的决定:如果前几代工程师已经解决了这个问题，就没有必要重新发明轮子。[海基]也记录了这个过程的很多细节，这值得称赞:他在博客上制作了一个 5 集系列，展示了他是如何以及为什么做出这些决定的。这个系列回顾了项目的[全景](http://www.sabulo.com/sb/8mm-film/the-8mm-film-scanner-project-part-1/)、[用 CHDK 控制摄像机](http://www.sabulo.com/sb/8mm-film/the-8mm-film-scanner-telecine-project-part-2/)、 [3D 打印部件](http://www.sabulo.com/sb/3d-printing-2/the-8mm-film-scanner-telecine-project-part-3-printed-parts/)、布线[Arduino](http://www.sabulo.com/sb/8mm-film/the-8mm-film-scanner-telecine-project-part-4-arduino/)和[编写控制系统的代码](http://www.sabulo.com/sb/blender/the-8mm-film-scanner-telecine-project-part-5-programming/)。

这与我们最近写的 8 毫米摄像头黑客技术非常相似。这一次不需要拆开相机(除了提供大门的牺牲相机)，你仍然可以获得 8 毫米胶片的美妙粒状、跳动的外观。

 [https://www.youtube.com/embed/kD9TfAbHeqA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kD9TfAbHeqA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

