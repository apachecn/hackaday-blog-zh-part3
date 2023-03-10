# 惊人的假宝丽来相机表演魔术

> 原文：<https://hackaday.com/2017/08/31/stunning-fake-polaroid-camera-performs-magic/>

是时候让我们麻瓜拥有拍摄《预言家日报》上的魔法照片的硬件了。Abhishek 已经在这个方向上迈出了开创性的第一步，他建造了这个类似宝丽来相机的移动图片相机，他称之为“Instagif NextStep”。这是一种摄像机，它可以录制一段三秒钟的视频，将其转换为 GIF 格式，然后弹出一个小盒子来显示动画照片。

这个令人惊叹的硬件是精心打造的，成品看起来很棒。用[Abhishek]自己的话来说，建设此类项目的好处在于，“它涉及一系列不同的技能组合和学科——硬件、软件、3D 建模、3D 打印、电路设计、机械/电气工程、设计、制造等，需要将它们整合在一起，以实现无缝工作。”

他可爱的相册里有很多照片，从头到尾详细描述了这个建筑。外壳和所有内部机械零件都是 3D 打印的，但需要使用 SLA 打印机。电子产品 BoM 是一个很长的列表。主摄像头名为 CamPi，有一个 Raspberry Pi 3 及其配套的摄像头模块，一个 2.8 英寸的 TFT 屏幕，一个 10000 mAh 的电源组，一个伺服系统和一系列配套部件。这款名为 SnapPi 的 GIF 墨盒有自己的 Raspberry Pi Zero W，另一个 2.8 英寸的 TFT 屏幕，一个 400 mAh 的 LiPo 和一个升压充电器。几个模块不得不在尺寸上进行修整，许多不必要的部分被移除，以使其完全匹配。

这两个 Pi 相互形成一个专用网络，用于通信和数据传输。大部分工作是由 Python 和通过 RPC 通信的节点脚本完成的。当按下快门按钮时，摄像机会录制一段三秒钟的视频。在通过网络发送到 SnapPi 之前，对其进行转换和压缩。缓慢淡入是宝丽来照片的标志，SnapPi 通过实现两种不同方法(在代码中选择)中的一种来实现淡入效果，从而模仿这一点。本质上，他正在生成一个逐渐增加不透明度的 GIF。这本身就是一个可怕的黑客。

他记录了他面临的所有问题，并描述了他是如何解决每一个问题的，这使得复制这台相机的任务变得更加容易。此外，对于那些黑客新手来说，这里还有一些方便的指南，比如[如何制作自己的印刷电路板](https://i.imgur.com/MSZ2MhC.mp4)和[如何从头开始设置树莓派](https://github.com/shekit/instagif/blob/master/README.md#setting-up-the-raspberry-pis)。如果你看到这个就想造一个，不要担心。[Abhishek]不仅发布了带有描述的照片，还提供了详细的 BoM 和链接，建造它所需的一切都可以从他的 [GitHub 库](https://github.com/shekit/instagif)获得。

如果你想看更多[Abhishek]的项目，看看 Peeqo， [Animatronic Head 回复动画 gif](https://hackaday.com/2016/12/10/animatronic-head-responds-with-animated-gifs/)。

谢谢你给我们这个提示，[霍布森]。

> [我做了一个可以即时打印 GIF 的相机](http://imgur.com/a/CG9w4)