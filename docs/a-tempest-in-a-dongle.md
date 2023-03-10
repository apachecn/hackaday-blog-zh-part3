# 软件狗中的风暴

> 原文：<https://hackaday.com/2017/11/26/a-tempest-in-a-dongle/>

如果说几代间谍电影教会了我们什么，那就是特工得到了最好的玩具。虽然它可能不像配备雷达的阿斯顿·马丁或不可能的保险库盗窃用的钢丝飞行钻机那么酷，但这个 DIY 的 TEMPEST 系统可以让你利用二次射频辐射窥探计算机。

如果暴风雨这个术语听起来很熟悉，那是因为我们之前已经讨论过了。[埃利奥特·威廉姆斯]介绍了属于 TEMPEST 保护伞的多种模式[，这是美国国家安全局的一个总括代号，用于通过监控计算机的非故意射频、光甚至音频发射来弥合空气间隙。最近，[Brian Benchoff]讨论了一个 TEMPEST hack，它避免了需要数千美元的 RF 设备，将装备简化为](https://hackaday.com/2015/10/19/tempest-a-tin-foil-hat-for-your-electronics-and-their-secrets/)[一个 SDR 加密狗和一个简单的天线](https://hackaday.com/2017/06/25/tempest-in-a-software-defined-radio/)。现在甚至有了一个这样的应用程序: [TempestSDR](https://github.com/martinmarinov/TempestSDR) ，一个多平台的 Java 应用程序，可以让你根据显示器的射频信号对其进行屏幕抓取。问题是，让应用程序在 Windows 机器上运行一直是一个挑战，但 RTL-SDR.com 阅读器[flatfishfly]解决了一些主要问题，并友好地分享了魔法。下面的视频显示了 TempestSDR 的结果；很明显，高对比度的图像最容易被窥探，但它表明一个 20 美元的加密狗和一些开源软件可以弥合空气间隙。让你想知道更深的口袋里会有什么。

RF 嗅探只是从空气隙系统中获取数据的众多方法之一。从[电源线](https://hackaday.com/2017/08/01/getting-data-out-of-air-gapped-networks-through-the-power-cable/)到[安全摄像头](https://hackaday.com/2017/09/21/another-day-another-air-gap-breached/)，破解系统的方法似乎永无止境。

 [https://www.youtube.com/embed/mBJ6uQZsF9c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mBJ6uQZsF9c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

