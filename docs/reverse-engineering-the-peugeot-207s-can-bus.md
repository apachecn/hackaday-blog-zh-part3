# 对标致 207 的 CAN 总线进行逆向工程

> 原文：<https://hackaday.com/2017/05/04/reverse-engineering-the-peugeot-207s-can-bus/>

这是一个经典的“一件事导致另一件事”的汽车黑客。[亚历山大·布兰]想要为他的旧标致 207 安装倒车摄像头，结果掉进了兔子洞，这让他用 Arduino 和 iOS 做了一些极端的 [CAN 总线逆向工程。买了一个昂贵的挡板，一个便宜的 HDMI 显示器，一个 Arduino，一个 CAN 总线屏蔽，一个带贫民窟串行接口电缆的 iPod touch，一个 HM-10 BLE 模块，一个 iPad 4S，相机本身，断断续续地工作了大约一年半，他最终变穷了大约 275€，但在工作中取得了胜利。公司改造不仅会让他花费更多，还会剥夺他在这个过程中学到的一切。](https://medium.com/@alexandreblin/can-bus-reverse-engineering-with-arduino-and-ios-5627f2b1709a)

当他找到一个专门为他的 207 车型定制的售后版本时，安装摄像头是这项工作中最简单的部分。原来的非图形显示器必须为新的 HDMI 显示器和新的边框腾出空间，这使他的成本远远高于显示器。除了倒车时显示摄像头图像，新显示屏还需要显示所有其他娱乐系统信息。这无法从 OBD-II 端口获得，但 CAN 总线看起来很有希望，尽管他最初无法找到他的模型的任何细节。但是随着超过 250 万辆 207 上路，没过多久[Alexandre]就在一个法国大学生项目中赚了大钱，他用一辆 207 来研究 CAN 总线。207 的 CAN 总线系统被细分为三条独立的总线,“舒适”总线提供了他需要的所有数据。为了解码 CAN 帧，他使用了一个 Arduino、一个 CAN 总线盾和一个 python 脚本来可视化数据，检查当他执行某些功能时哪些帧发生了变化——例如，改变音量或倒挡。

Arduino 不能直接驱动 HDMI 显示器，所以他需要额外的硬件来完成他的破解。虽然树莓派是最理想的，但[Alexandre]是 iOS 开发者，所以他自然会被苹果生态系统所吸引。他通过 iPod 上的 Dock 端口的串行连接将一台旧 iPod 连接到 Arduino。但是使用苹果 HDMI 适配器连接显示器破坏了串行连接，所以他不得不重新思考。这一次，他使用了连接到 Arduino 的 HM-10 BLE 模块，并用更现代的 iPhone 4S 取代了旧的 iPod Touch(不支持 BLE)。一旦他有了所有的零件，他很快就可以完成这个漫长的升级，但最终的结果看起来像工厂原装的一样好。休息之后请看视频。

很高兴看到这类黑客挖他的脚，直到它完成和尘埃不放弃。由于他的详细帖子，以及在他的 [GitHub 库](https://github.com/alexandreblin?tab=repositories)上分享的所有代码，对于那些想要升级他们的旧 207 的人来说，第二次复制这一点应该很容易。如果你正在寻找灵感，看看这个伟大的[自制斯巴鲁头单元升级](http://hackaday.com/2017/02/20/homemade-subaru-brz-head-unit-is-hidden-masterpiece/)。

 [https://www.youtube.com/embed/ucKHWWT728Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ucKHWWT728Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

