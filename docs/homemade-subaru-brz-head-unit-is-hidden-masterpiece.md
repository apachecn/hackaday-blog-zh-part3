# 国产斯巴鲁头单元是隐藏的杰作

> 原文：<https://hackaday.com/2017/02/20/homemade-subaru-brz-head-unit-is-hidden-masterpiece/>

斯巴鲁 BRZ(也是为丰田生产的 GT86)是一款时髦的跑车，但[megahercas6]的美国老款有许多导航和娱乐系统功能，这些功能在他的祖国立陶宛没有用或不起作用。他本可以把内置屏幕换成一个大的 4G Android 平板电脑/手机，但这方面的冒险有限。相反，他继续前进，通过设计和集成一大堆硬件模块，构建了自己的自制导航系统。

该系统是围绕一款运行安卓系统、支持 GPS、GLONASS 以及中国北斗卫星导航系统的联想 4G 手机平板电脑构建的。他移除了平板电脑上处理 USB OTG 连接的原始子板，并用他的版本替换，以便他可以通过扁平带状电缆将其连接到外部 USB 板。USB 板包含一个 Cypress 4 端口 USB 集线器。一个端口用作 USB HID 设备，允许外部按钮进行系统控制——电源、音量调高/调低、快进/快退、播放/暂停和电话接听/挂断。第二个端口用作常规 USB 输入，允许连接闪存驱动器等外部设备。第三个端口连接倒车摄像头，第四个端口连接 USB DAC。

 [![subaru_2](img/eec3731f5cf88d9bab2fad7aa7b866f9.png "subaru_2")](https://hackaday.com/2017/02/20/homemade-subaru-brz-head-unit-is-hidden-masterpiece/subaru_2/)  [![4096441487256015818](img/3ce8a6ba1847f8d3e86e8f43ed1a07db.png "4096441487256015818")](https://hackaday.com/2017/02/20/homemade-subaru-brz-head-unit-is-hidden-masterpiece/attachment/4096441487256015818/) 

USB DAC 本身是另一个硬件板，还包括一个蓝牙模块，该模块将他的电话的音频和控制功能与板载系统集成在一起。还有一个音频混合器，允许他使用手机音频，而不必错过平板电脑的导航提示。两块电路板还包含几个外围电路，如放大器和 DC 电源。扬声器的音频通过六个基于 LM3886 的功率放大器板传输。GPS 模块接收自己的特殊低噪声放大器板，以确保在任何时候都有极强的接收能力。这是为这个项目定制的总共 10 块板。他还设法找到了所有原始的线束连接器，因此他的系统完全可以快速更换。最终的组装看起来相当漂亮。

出于某种奇怪的原因，联想平板电脑使用 4.35V 作为其 LiPo 的“完全充电”值，而不是更常见的 4.20V，因此即使整个系统连接到一个巨大的 12V 铅酸电池(他从该电池获得平板电脑的 4.20V 充电电压)，它仍然抱怨“电池电量低”——他正在寻求建议，如何通过使用更高的充电电压来解决这个问题，而不是炸毁 LiPo。除此之外，他是一名硬件设计师(显然是一名优秀的设计师),对软件和编程方面的东西有点生疏，他正在寻找来自社区的意见。他的[介绍视频](https://youtu.be/6oQAWzosxcs)几乎有 30 分钟长，但休息后的较短演示视频展示了安装在他汽车上的系统。他在项目页面上发布了他所有的 Altium 硬件源文件，但在他分享 PDF 版本之前，我们大多数人都很难看到他的作品。

 [https://www.youtube.com/embed/0uwk18LdOaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0uwk18LdOaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

