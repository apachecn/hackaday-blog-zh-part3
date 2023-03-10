# 使用 SDR 加密狗对晶体进行分类

> 原文：<https://hackaday.com/2018/06/06/classifying-crystals-with-an-sdr-dongle/>

说到射频振荡器，晶体控制是你想要频率精度的方法。但是并不是每个装在银盒子里的石英都是一样的，所以在使用之前需要对水晶进行鉴定。这通常是示波器的工作，但是如果你聪明的话，[SDR 加密狗也可以做一个漂亮的晶体检测器](https://www.youtube.com/watch?v=F6pNEsxSvHQ)。

关于[OM0ET]小黑客的背景故事很有趣，我们希望能继续下去。斯洛伐克的 ham 正在建造一个看起来相当复杂的自制单边带高频收发器。这种装置需要良好的中频(IF)滤波器，这需要匹配的晶体组。他想要一种快速简单的方法来浏览他收集的晶体，并获得谐振频率的精确读数，所以他转向了他便宜的小 RTL-SDR 加密狗。插入运行 SDRSharp 的 PC，加密狗的天线输入连接到一个简单的单晶体管晶体振荡器的输出。没有给出原理图，但看看下面的视频布局表明，这只是一个科尔皮兹振荡器。插入受测晶体后，振荡器会在 SDRSharp 频谱分析仪显示屏上产生一个巨大的尖峰信号，[OM0ET]可以快速确定中心频率。我们建议用一个衰减器将削波后的平台变成更尖锐的峰值，但除此之外，它非常有效，他甚至发现了一些无用的晶体。

对石英晶体的机电感兴趣？我们也是，这就是为什么[【Jenny】的晶体振荡器初级读本](https://hackaday.com/2017/01/17/understanding-the-quartz-crystal-resonator/)是好奇者的第一站。

 [https://www.youtube.com/embed/F6pNEsxSvHQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F6pNEsxSvHQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via[RTL-SDR.com](https://www.rtl-sdr.com/using-the-rtl-sdr-as-a-tool-to-measure-crystals/)