# 借助网络摄像头和 Raspberry Pi 实现低成本视频流

> 原文：<https://hackaday.com/2016/11/25/low-cost-video-streaming-with-a-webcam-and-raspberry-pi/>

有些人会告诉你，YouTube 已经像它之前的电视机一样，变成了一片巨大的娱乐荒地。直播对这种情况没有太大帮助，而且这款入门级网络摄像头直播服务器并没有准备好推进这项技术。

我们开玩笑，但只是一点点。[Mike Haldas]经营一家视频监控公司，销售各种网络摄像头，他想知道如何才能为直播设置一个低端摄像头。第一步是将 Zavio 网络摄像头流从 RTSP(实时流协议)转换为 YouTube 使用的标准 RTMP(实时消息协议)。幸运的是， [FFmpeg](https://www.ffmpeg.org/) 处理这种转换，所以他为他的 MacBook Pro 编译了它，并建立了一个概念验证。这很有效，但是他需要一个紧凑的解决方案来释放他的笔记本电脑。Raspberry Pi 来拯救——在加载了一堆库和四个小时的 FFmpeg 构建和安装之后，网络摄像头正在播放[Mike]销售办公室的 1080p 视频。他担心 Pi 没有工作所需的权力，而且会不稳定。但是在我写这篇文章的时候，下面的流已经活跃了六天了，非常有趣。

树莓 Pis 是音频流世界的主要产品，像[这种专业级 FM 广播流媒体架](https://hackaday.com/2013/11/20/raspis-and-arduinos-for-fm-broadcast-streaming/)或[这种微型互联网广播流媒体工具](https://hackaday.com/2015/12/10/audio-streaming-on-the-cheap-with-an-rpi-zero/)。当然还有[这个快速而肮脏，温暖而模糊的流式婴儿监视器](https://hackaday.com/2016/11/12/raspberry-pi-spies-on-err-monitors-baby/)。

 [https://www.youtube.com/embed/3k_AOArC-ec?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3k_AOArC-ec?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过[r/树莓派](https://www.reddit.com/r/raspberry_pi/comments/5dgwbf/simple_project_that_uses_a_raspberry_pi_ffmpeg/)