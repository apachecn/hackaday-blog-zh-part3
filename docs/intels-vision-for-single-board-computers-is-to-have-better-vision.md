# 英特尔对单板电脑的愿景是拥有更好的愿景

> 原文：<https://hackaday.com/2017/05/26/intels-vision-for-single-board-computers-is-to-have-better-vision/>

在上周末的湾区制造商大会上，英特尔展示了单板计算机(SBC)市场上的几个性感新人。人们很容易陷入这样的想法，即 SBC 都是简单的主板，价格为两位数，就像 Raspberry Pi 一样。你怎么能和一台拥有巨大市场份额和庞大社区的 35 美元的电脑竞争呢？你通过吸引对这些入门级 SBC 不满意的人群来竞争，为此，英特尔似乎瞄准了更高端的受众，他们需要计算机视觉以及速度和马力来做一些有意义的事情。

上周末，我在 Maker Faire Bay Area 见到了英特尔的“创客沙皇”杰伊·梅利肯(Jay Melican)。一年前，引起我注意的是一台任天堂[电动手套控制的四轴飞行器](http://hackaday.com/2016/06/06/power-glove-takes-over-quadcopter-controls/)。今年，我只对提供的两个新的计算模块感兴趣，焦耳和欧几里德。他们都专注于将强大的处理器连接到高分辨率相机，并使用成熟的 Linux 操作系统进行图像处理。但感觉上，焦耳更适合普通的硬件黑客，欧几里德更适合那些将技能指向机器人但不想陷入硬件基本原理的软件工程师。在你在评论中对此感到愤怒之前，让我解释一下。

## 欧几里得

[![](img/043352561d1ba0e28c4411e02a581da6.png)](https://hackaday.com/wp-content/uploads/2017/05/dsc_0052.jpg) 这是欧几里得的。它的大小和形状让我想起了 20 世纪 90 年代和 21 世纪初的数码录音机，但它有一个光滑光滑的黑色表面(与 8 月份[第一次戏弄](https://hackaday.com/2016/08/26/intel-makes-a-cool-robot-brain-in-latest-attempt-to-pry-hackers-from-their-wallets/)时略有不同)，它布满了端口、按钮和几组明显的光学元件。

这款 beast 运行的是四核 Atom 处理器，配有 4 GB 内存和 32 GB 板载存储。仅此一点不会让你大吃一惊，但欧几里德还内置了一个 RealSense 深度相机、一个 RGB 相机和一个鱼眼相机。它能够实现立体视觉(VGA 分辨率)，并包括一系列对 IMU 和 GPS 等机器人技术至关重要的传感器。这东西甚至配有锂电池。

它运行的是 Ubuntu 的全桌面安装，这听起来有点大材小用，但我认为这样做的目的是为了那些不想学习新平台的人。下周我们将发表一篇关于一群黑客的文章，他们在集会上展示了他们的自动遥控车辆。他们参加了 Sparkfun 的 AVC 比赛，并为此在 RC 机箱上安装了 Macbook Pro。Euclid 将以五分之一到十分之一的价格提供与该版本相同的功能——所有功能都封装在一个舒适的小盒子中(标准三脚架便于使用)。拿起你的无线键盘，插入 HDMI 进行编程和调试，或者使用内置的 WiFi 接入。

在你看到的小型轮式机器人的例子中，与机器人的连接是通过 USB 完成的。一个较低级别的嵌入式板驱动电机控制器，从欧几里德发出串行命令。有些人可能会批评使用 USB 的延迟，但控制机器人的 SBC 几乎总是有类似的延迟问题。

## 焦耳

 [https://www.youtube.com/embed/Me10uzUWV3M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Me10uzUWV3M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你更喜欢裸露的 PCB，八月[宣布的](http://hackaday.com/2016/08/17/intel-releases-the-tiny-joule-compute-module/)[焦耳](http://intel.com/joule)值得一看。它使用了一种我们现在熟悉的英特尔“创客”产品的方法；Joule 本身就是一个模块，需要一个主板来断开所有的连接。它还运行 Atom 处理器，配有 4GB 内存和 32 GB 板载存储。听起来很像欧几里得，对吧？它们很接近，但两者的处理器确实不同。

基本上，Joule 是大脑，Euclid 是营销它们的华而不实的方式……就像我前面说的，让更多的人参与进来，而不会陷入试图将硬件连接在一起的困境。但是我们中的许多人喜欢将硬件连接在一起，这就是为什么 48 个 GPIO 是机器人制造商的最爱。

 [![Rajida stereoscopic camera and Joule](img/6c3f00bd95c937fffc216823e9489d63.png "DSC_0078")](https://hackaday.com/2017/05/26/intels-vision-for-single-board-computers-is-to-have-better-vision/dsc_0078-6/) Rajida stereoscopic camera and Joule [![Electronics cylinder in the ROV](img/f027ab0a77ff43fd7d219b670cc05707.png "DSC_0082")](https://hackaday.com/2017/05/26/intels-vision-for-single-board-computers-is-to-have-better-vision/dsc_0082-3/) Electronics cylinder in the ROV

这个模块提供了和欧几里得一样的处理计算机视觉的能力，但是你需要带你自己的照相机来参加聚会。你可以购买欧几里德包装的英特尔 RealSense 深度相机，但在英特尔展台上，引起我兴趣的是一个水下机器人。

Rajida 的团队从淘宝上购买了一个双目相机板，并建造了他们的 ROV 来跟随五颜六色的鱼。我用一根棍子上的黄色神仙鱼玩具做了一个非常漂亮的演示。不幸的是，英特尔的展台在室外，阳光明媚的加利福尼亚不是录制电视回放视频的地方。享受静止的图像，相信我，这是可行的，很酷。

 [![Enclosure for the ROV](img/ecc02d81dc81bf93fd93178b654a8958.png "DSC_0084")](https://hackaday.com/2017/05/26/intels-vision-for-single-board-computers-is-to-have-better-vision/dsc_0084-2/) Enclosure for the ROV [![Stereoscopic demo on the TV](img/5fc4997ce1857d98dbe23be42f8e3853.png "DSC_0088")](https://hackaday.com/2017/05/26/intels-vision-for-single-board-computers-is-to-have-better-vision/dsc_0088-4/) Stereoscopic demo on the TV [![Rajida's builder poses with the robot](img/d3fb49f62d71f57566fecd9184dd3d93.png "DSC_0089")](https://hackaday.com/2017/05/26/intels-vision-for-single-board-computers-is-to-have-better-vision/dsc_0089-4/) Rajida’s builder poses with the robot

布莱恩·本考夫经常写道(讽刺的是——ed。)关于“自拍无人机”是便携式计算机视觉的杀手级应用。我认为水下遥控潜水器会有巨大的市场，它可以跟随水肺潜水员，并以第三人称视角记录体验。

你现在可以花 299-349 美元买到一焦耳。看起来欧几里德还没有发货，但在英特尔网站上的预购价格约为 399 美元。