# 短程球面上的 540 个发光二极管

> 原文：<https://hackaday.com/2016/06/12/540-leds-on-a-geodesic-sphere/>

喜欢参加音乐节。他也是一个热爱 LED 的机械师。他认为他需要把所有这些放在一起，做一些疯狂的事情，所以他建造了一个巨大的，15 英寸的测地线球体，包含 540 个 WS2812B 可寻址 LED。他称之为溶胶粉碎机。当所有的 LED 都处于最大亮度时，它消耗 150 瓦，使它非常非常亮。

与大多数基于 WS2812B 的项目一样，这个项目在电气方面也相当简单。它由安装在 Octo WS2811 适配器板上的四块 Teensy 3.2 板控制。四个 10，000 mAh 22.2V LiPo 电池提供电力，通过 5V，30Amp 散热的 DC-DC 转换器传输。为了防止他的脂肪电池过度放电，他建立了四个电压监测模块。每个都有一个 TC54 电压检测器和一个 N 沟道 MOSFET，它在 LiPo 电压下降到 3V 以下之前关闭 LiPo。他捆绑了一个保险丝和一个指示器，并把它们放在一个整洁的 3D 打印外壳中。

机械设计非常完美。180 个基本模块中的每一个都是一个三角形 PCB，带有三个 WS2812B、滤波电容和用于电源连接的重型铜浇注。印刷电路板被组装成六个或五个单元的面板，然后将它们放在两个半球中形成整个球体。他的第一轮六个原型让他受挫，因为他在 LED 封装上犯了一个错误。但它仍然让他检查装配和电源连接。对于机械支撑，他设计了一个可以 3D 打印的内部骨骼。每个 PCB 面板都有一个安装框架和一个两件式中央球体。玻璃纤维棒将中央球体连接到每个 PCB 面板。这使得整个组件可以很容易地分成两半。

他花了六个多月时间和大量现金完成了这个项目。但是现在组装已经完成，并且通过了电气测试。接下来，他正在开发添加动画的软件。他通过 Reddit 上的[评论收到了添加麦克风和加速度计等传感器的建议。如果你想通过贡献动画建议来帮助他，他在 Dropbox 上设置了一个](https://www.reddit.com/r/DIY/comments/4mza8n/i_like_leds_so_i_put_540_of_them_on_a_ball_to/)[自述文件](https://www.dropbox.com/s/5ykxn2ujp1wyrxo/Readme.txt?dl=0)，和一个[提交表格](https://www.dropbox.com/request/UYffX3YlyBVSGNnfAnnB)。查看 SolCrusher 网站了解更多信息。

感谢[Vinny Cordeiro]让我们了解这个版本。

 [https://www.youtube.com/embed/j2KwD5Is1Z8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j2KwD5Is1Z8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

