# 用 Arduino 抓住一颗冉冉升起的新星

> 原文：<https://hackaday.com/2018/04/26/catch-a-rising-star-with-arduino/>

空间大。非常大。然而在电视和电影中，敌人的宇宙飞船通常会在大致相同的地点相遇，并且奇迹般地在相同的方向相遇。如果你曾经试图在望远镜中找到比月亮还小的东西，你会发现这并不容易。定位物体有很多技巧，从昂贵的带马达的电脑化望远镜到在你的望远镜上安装一部带谷歌天空或类似程序的手机。[dentarthurdent]没有使用电话。他使用了一个带有外置 GPS 模块的 Arduino。

你仍然需要自己移动瞄准镜，但是 GPS 意味着你知道你的位置和高度准确的时间。在开始观察之前，你只需将望远镜对准北极星来校准算法，这个过程在北半球相当容易。

讨论中的望远镜是一个多布森望远镜，因此易于移动，并且易于使用电位计和 A/D 来感测其位置。该项目还包括用于将时间、纬度、经度、赤经和赤纬转换为位置数据的数学的详细描述。四个 led 中的一个显示您应该向上、向下、向左还是向右移动。当您达到目标时，所有四个 led 都会亮起。我们假设你应该使用红色发光二极管和红色液晶滤光器，这样你就不会破坏你的夜视能力。

有几个错误的来源和[阿瑟]做了大量的工作，分析和纠正每一个。该项目甚至有一个漂亮的 3D 打印案例。该数据库只包含 45 个对象，但很容易添加更多。我们想知道使用更大的计算机[如 Raspberry Pi](https://hackaday.com/2017/12/05/astro-cat-raspberry-pi-telescope-controller/) 来获得恒星数据——甚至可能来自互联网——并依靠 Arduino 来管理位置感测和方向指示是否会更好，但话说回来，这是可行的，而且非常便宜。

这不是我们看到的第一个 Arduino 望远镜。最后一个甚至有触摸屏。