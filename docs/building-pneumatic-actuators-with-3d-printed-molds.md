# 用 3D 打印模具制造气动执行器

> 原文：<https://hackaday.com/2016/09/23/building-pneumatic-actuators-with-3d-printed-molds/>

气动执行器在软机器人和交互设计等应用中提供了有趣的前景。【艾丹·里奇】用硅橡胶制作[他自己的气动执行器。他的致动器包含嵌入式空气通道，可以填充加压空气，当没有压力时，可以完全折叠成平板。](http://www.instructables.com/id/Flat-Soft-Actuators-From-Images/)

[![pneumatic-actuators-animation](img/5669c7fd0c7f33b5d9f47a07101938c0.png)](https://hackaday.com/wp-content/uploads/2016/09/pneumatic-actuators-animation.gif) 该工艺基于 Kevin C. Galloway 等人对[【零容积气室】](http://www.kevincgalloway.com/portfolio/zero-volume-air-chambers/)的研究工作。研究小组发现，他们可以将一层薄薄的硅橡胶倒入一个平模具中，然后使用激光切割掩模选择性地将脱模剂图案应用到固化层的表面，然后在顶部倒入第二层硅胶。脱模防止了两层硅树脂粘结在一起，留下了充气的空气通道，该通道在未加压时需要接近零的体积。

为了复制他们的结果，[Aidan's]编写了一个 [OpenSCAD 脚本](http://www.thingiverse.com/thing:1708181)，可以从黑白图像中生成 3D 可打印模具。模具包括脱模剂的掩模，而图像中的白色区域定义了嵌入的空气通道，黑色区域定义了固体硅胶。请欣赏下面的视频，其中[Aidan]演示了他的过程！

 [https://www.youtube.com/embed/LlxUZABcah0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LlxUZABcah0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Jean]的提示！