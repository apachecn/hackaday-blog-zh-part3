# 星毯以皇家进行曲迎接游客

> 原文：<https://hackaday.com/2016/01/04/starmat-greets-visitors-with-the-imperial-march/>

有了这个学徒，原力就强大了。为了配合来自一个遥远星系的持续传奇的最新部分，[罗希特·古普塔]建造了一个以《星球大战》为主题的互动门垫。门垫使用电容感应检测脚步声，并播放随机的《星球大战》音频剪辑，如开场主题或《帝国进行曲》或电影中的一句名言。请看休息时间下面的视频。

目前的设置暂时是试验性的，但我们相信它会受到他的访问者的欢迎，让他整理它。硬件包括一个 Arduino，带有连接到一对扬声器的音频屏蔽。垫子下面的电容线圈和调谐到垫子尺寸导线的电容传感器负责检测。

当地球人踩在垫子上时，传感器会触发 Arduino 播放 SD 卡中的随机音频片段。电容感测由 [TP223 单键触摸板检测器芯片](http://www.seeedstudio.com/depot/datasheet/TTP223_SPEC.pdf) (PDF)负责，他将其安装在一个带有 SMD 部件的家用蚀刻板上。整个包由一个小的“能量银行”电池组供电，就像用来给手机充电的那种。

 [https://www.youtube.com/embed/A_ZnKR84uk4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/A_ZnKR84uk4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

