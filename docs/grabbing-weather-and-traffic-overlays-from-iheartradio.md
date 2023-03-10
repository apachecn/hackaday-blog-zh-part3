# 从 IHeartRadio 获取天气和交通覆盖图

> 原文：<https://hackaday.com/2017/12/20/grabbing-weather-and-traffic-overlays-from-iheartradio/>

当我们中年纪较大的人想到收音机时，我们会想到调频或调幅电台。散布在乡村的巨型广播塔向我们伟大的土地上发射由音乐、谈话和运动调制的电磁波。年轻人可能会惊讶于如此原始的技术仍然存在。虽然一个未调谐的 AM 接收器的静电噪音可能相当于一个 56K 调制解调器的拨号音，但它仍然是我们社会的一个主要部分。

像所有技术一样，无线电已经转变为更快更好的发送信息的方式。今天，我们有数字广播电台，其中最受欢迎的是 iHeartRadio。因为它是数字的，它还可以发送除音频以外的信息，如天气和交通信息。

在[KYDronePilot]的家伙们已经利用这个用 SDR 和一个小 Python 来显示实时天气和交通地图[。他们是 Python 的新手，所以一定要看看他们的 GitHub，拿一份代码，如果发现有改进的空间，就告诉他们。](https://github.com/KYDronePilot/hdfm)

这个黑客是基于[最近解码数字数据](https://hackaday.com/2017/06/21/receiving-nrsc-5-with-sdr/)的工作，如果你对 SDR、DSP 或任何其他无线电相关的缩写感兴趣，这是值得一试的。