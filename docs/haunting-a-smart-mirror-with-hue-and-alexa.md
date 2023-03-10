# 用 Hue 和 Alexa 纠缠智能镜

> 原文：<https://hackaday.com/2017/10/28/haunting-a-smart-mirror-with-hue-and-alexa/>

所以，你的智能镜子已经运行了一段时间，但万圣节快到了，你想拿出一些很酷的万圣节用品在镜子上展示。如果你正在寻找灵感，请查看[Ben Eagan]的酷[闹鬼智能镜子](http://www.cyber-omelette.com/2017/10/haunted-home-automation.html)，它通过树莓 Pi 将镜子与亚马逊 Alexa 和 Phillips Hue lighting 连接起来。

[Ben]为那些对使用智能镜子设置 Alexa 的细微差别感兴趣的读者指出了他的另一个博客页面，同时在这篇文章中专注于与 Hue bridge 的通信并为新的 Alexa 命令创建设置。处理 Phillips Hue API 似乎相当简单:从路由器获得 Hue 网桥的 IP 地址，从 Hue 应用程序获得灯的 ID，然后就可以通过 HTTP 发送命令了。[Ben]包括一个 Python 脚本来使灯光闪烁，你可以根据自己的意愿修改灯光。一旦完成，您将需要设置 Alexa 监听的意图，然后修改 AWS lambda 函数，该函数向 Pi 发送命令。当命令出现在 Pi 的队列中时，任何[Ben]想要播放的命令都会被触发——在这种情况下，会播放一段视频，并且色调灯开始闪烁。

文章中没有提到安全性，所以这可能值得 Alexa 和色调的一点注意，但随着万圣节的到来，即使你还没有建立一个魔镜，如果你有色调灯，这将是一个伟大的，快速的万圣节想法。尤其是如果你能把它和外面的灯结合起来，让“不给糖就捣蛋”的人也能加入进来。也许你更喜欢[用 Alexa 查找路过的飞机](https://hackaday.com/2017/07/02/alexa-what-plane-is-that/)？或者[让你的鱼说话](https://hackaday.com/2016/11/08/alexa-brings-back-singing-fish-this-time-its-a-good-thing/)怎么样？

 [https://www.youtube.com/embed/Vm3WBFDKKPI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Vm3WBFDKKPI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

