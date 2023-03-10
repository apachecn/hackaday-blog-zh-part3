# 整个房子 HiFi 驯服没有大惊小怪

> 原文：<https://hackaday.com/2017/01/07/whole-house-hifi-tamed-without-fuss/>

随着越来越复杂的家庭娱乐系统的出现，随之而来的一个问题是在你的系统旁边出现的大量遥控器的复杂性。如果你有一个花哨的万能遥控器也没关系，在你坐下来享受音乐之前，你仍然有许多功能要执行。

[罗伯特·考恩]他的全屋音响系统有这个问题。演奏音乐需要摆弄遥控器，而那个时刻已经过去了。我们需要的是一个自动系统，它只需简单地向立体声系统发出相关命令，而无需大惊小怪。

他的解决方案是[当他的 Sonos Connect 流媒体播放器](https://www.youtube.com/watch?v=8nuQflp3iRA)检测到音频输出时，让一切都发生。他试图调整它的线路输出来检测音乐，但遇到了问题，所以改用了 SparkFun 音频检测模块。这进而与 Arduino 对话，Arduino 然后通过电平转换器与立体声系统的 RS232 端口对话。[Robert]在视频描述中包含了所有相关部件、原理图和软件链接。这个项目几乎应该成为一个像样的立体声系统的一个功能，但制造商更喜欢他们的遥控器的糟糕界面。

 [https://www.youtube.com/embed/8nuQflp3iRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8nuQflp3iRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们不禁想知道，他那一尘不染的工作台和整洁得令人怀疑的工作间，是真实的硬件黑客场景还是电视演播室，但我们会原谅他的好成绩。

毫不奇怪，在 Hackaday 之前，我们已经误入了这个领域，这里有一个红外通用远程项目的综述。如果你甚至不确定遥控器是否工作，[我们已经介绍了一个方便的测试器](http://hackaday.com/2015/06/15/a-simple-circuit-for-testing-infrared-remote-controls/)。

谢谢[丹·沃森]的提示。