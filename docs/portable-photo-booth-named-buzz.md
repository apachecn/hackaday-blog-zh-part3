# 名为 Buzz 的便携式照相亭

> 原文：<https://hackaday.com/2018/05/03/portable-photo-booth-named-buzz/>

我们都习惯于摆好姿势拍照——或者自拍——但是照相亭有一种特质，让拍照成为一件令人兴奋而又紧迫的事情。为了让这种体验更容易携带，Redditor [pedro_g_s]辛苦地从头开始建造了一个名为 Buzz 的移动照相亭。

他需要一个触摸屏，一个树莓皮，几乎肯定是一个网络摄像头，和一个 3D 打印机来制作一个案例——尽管你选择的任何媒体都可以——来建造这个“展位”也就是说，他以一种不需要触摸屏的方式构建了这款应用，但携带鼠标来连接和操作你的便携式照相亭似乎有点跑题。在后端，他使用 Electron 编写 photo booth 应用程序，React 帮助他构建触摸屏 UI，Yarn 将必要的依赖关系保持有序。

操作很简单，每次拍照都会发送到预先设置的电子邮件服务中进行整理。为了进行设置，[pedro_g_s]将指导您完成整个过程。

作为一个完整的免责声明，他说他的代码可能需要一些工作，所以考虑自己预先警告，但他写了一个详细的演练，让一个类似的照相亭为自己运行！对于潜在的建设者来说，这个项目需要一个 Firebase 帐户和一个相关的项目才能运行，但他也提供了如何实现这一点的步骤和链接。没有提到任何电源，所以我们希望这是留给个人来解决的——但我们希望 Hackaday 的读者能够更好地解决这个问题。

我们仍然想知道为什么照相亭如此棒，以至于[员工](https://hackaday.com/2015/06/05/smile-for-the-raspberry-pi-powered-photo-booth/)和[婚礼嘉宾](https://hackaday.com/2010/09/28/photo-booth-for-a-wedding/)都会花几秒钟对着镜头微笑。

[通过 [/r/raspberryDIY](https://www.reddit.com/r/raspberryDIY/comments/8e9rql/a_portable_photo_booth_built_on_top_of_electron/)