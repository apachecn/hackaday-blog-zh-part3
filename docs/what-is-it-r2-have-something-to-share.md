# 怎么了，R2？有什么要分享的吗？

> 原文：<https://hackaday.com/2017/10/27/what-is-it-r2-have-something-to-share/>

有时候伟大的项目会不断发展。[Bithead942]为自己造了一个 R2-D2，在他去军队的时候陪伴他——但是感觉有些不对劲。原来，R2 缺少它标志性的哔哔声戏谑，所以他通过[实现几个语音命令](https://bithead942.wordpress.com/2017/09/16/r2-d2-voice-control/)使它更具情境响应性。

[Bithead942]的主要服装是 X 翼飞行员的服装，复制头盔的效果非常完美；它已经有了一个假麦克风——很容易用一个工作模型来代替——还有一个完美的位置来把电子产品藏在“莫霍克发型”里。'

尽管头盔为电路提供了完美的隐藏点，但空间仍然非常宝贵。像 Alexa 这样的服务往往非常准确，但需要 WiFi 接入——这在会议大厅无法保证。相反，[bithead942]发现 EasyVR Shield 3.0 语音识别板提供了一个合适的替身。它需要一点训练才能正常工作(提示蒙太奇！)，但最终它会将新的音频命令与它存储的“训练”文件进行比较，如果匹配，就会触发相应的串行端口。它并不完美，但它肯定是有效的！

 [https://www.youtube.com/embed/idB_NsRkccc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/idB_NsRkccc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



为了传输命令，[bithead942]恢复了他们的老一套:Fio v3(atmega 32 u 4)和 XBee 1mW 有线天线，[bithead942]证明这两种天线都很可靠，并且几乎不需要电力。这两个加上 EasyVR Shiled 连接到麦克风耳机，并固定在头盔内。R2 有一个 Adafruit 迷你音频 FX 板来处理音频。一个电源开关，2000 毫安时电池和一个充电端口，新头盔已经为它的第一次任务做好了准备。愿原力与你同在，[bithead942]！

我们之前已经介绍过[bithead942]的这个 R2 控制器的版本[，来看看吧！这里有](https://hackaday.com/2017/07/19/this-isnt-the-r2-d2-controller-youre-looking-for/)[另一个有用的 R2 单位](https://hackaday.com/2016/03/20/r2-d2-keeps-this-university-bathroom-smelling-fresh/)在你意想不到的地方看着你。