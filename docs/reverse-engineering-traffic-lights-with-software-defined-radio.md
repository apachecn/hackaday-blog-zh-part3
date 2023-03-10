# 用软件无线电对交通灯进行逆向工程

> 原文：<https://hackaday.com/2015/09/20/reverse-engineering-traffic-lights-with-software-defined-radio/>

建筑工人在街道上铺设新的互联网光纤电缆，这为巴斯蒂安·布洛斯创造了一个独特的机会。工人们带来了两个移动交通灯，以帮助他们在工作时保持道路安全。[Bastian]听说这些灯使用 2 米波段无线电，[所以他拿起他的 RTL-SDRu 盘，开始入侵](http://www.bastibl.net/traffic-lights/)。移动交通灯在欧洲变得越来越普遍。它们可以通过时钟、车载摄像头、电线或无线电控制交通流量。它们还传输状态数据，这正是[Bastian]希望接收到的。

用 GQRX 快速扫描显示在 170.760 MHz 上有强信号。使用 baudline 和 audacity，[Bastian]能够确定[音频频移键控](https://en.wikipedia.org/wiki/Frequency-shift_keying)用于调制数据。他在 GNU radio 中创建了一个简单的接收器链，并收到了来自灯光的稳定数据流。通过观察灯光和数据帧，[Bastian]能够确定哪些位包含当前的灯光状态。一个快速创建的网络界面让他可以实时显示交通灯的状态。

数据以明文形式发送有点可怕，但这只是状态数据。我们希望任何命令数据都通过更安全的通道加密发送。

 [https://www.youtube.com/embed/1hb10T3aP4g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1hb10T3aP4g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

