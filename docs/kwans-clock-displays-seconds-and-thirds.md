# [关]的时钟显示秒和秒

> 原文：<https://hackaday.com/2017/03/18/kwans-clock-displays-seconds-and-thirds/>

我们不知道背景故事是真是假，但我们不会让“真实”这样的东西妨碍一个好故事。按照[Kwan3217]的说法，首先是日晷时间。然后，当这些被分成 60 分钟的部分，他们被称为“分钟”。“秒”来自于秒除以 60，变成“秒分钟”。除以 60 的“第三”除法将给出持续 60 分之一秒的时间单位。

[Kwan3217]建造了一个时钟，[显示这些第三分钟](https://hackaday.io/project/20292-project-precision)。每根指针的重量只有 16.6666 毫秒多一点，第三根指针会转得很快，所以他用了发光二极管。如果你要显示三分之一，你必须把它们弄对，所以他用全球定位系统支持时钟。有一个关于它的[完整视频播放列表](https://www.youtube.com/playlist?list=PLjAfGWZat_qaMTNIUiyQK7-VLgXCSohcj)，以及项目日志中惊人的细节。

[![](img/dc3897860354ace686e4687fbd78d2eb.png)](https://hackaday.com/wp-content/uploads/2017/03/ro_my8hkhgtdbe-g1gxc14jchqdjc84mb4pabr1cp4hvwbzvogg68pjt5kz7o9onlskvqi8frp0noqyto6kkc2kfwllmszpeohjg83pqlqvaxy524dh_qh2xj84zfvmwxmiw0fvq.png) 我们非常喜欢读取 GPS 字符串的状态机的实现。[Kwan3217]严重依赖等待下一个美元符号的崩溃状态，这标志着 GPS NMEA 数据块的开始。他的几乎所有解析 GPS 数据流的函数都知道下一步需要什么样的数据，如果没有得到，它们就会崩溃。因此，虽然他的挂钟错过了 GPS 信息可能并不重要，但至少它会很快回到准确的时间。如果您发现自己正在解析 GPS 字符串，请查看代码。

我们提到 PCB 上的圆形痕迹了吗？还是光管？

我们已经发布了很多关于时钟的帖子，但没有一个显示三分钟。有了 GPS 规范的微控制器，获得哪怕是一毫秒的精确定位都不成问题。问题是展示它们。所以毫不奇怪，许多人走相反的方向，要么近似地像文字钟一样报时，艺术地像这个 T2 柏林集合论钟一样报时，要么不可思议地像外面所有的电阻色钟一样报时。

 [https://www.youtube.com/embed/95fiuYUa4cI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/95fiuYUa4cI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

