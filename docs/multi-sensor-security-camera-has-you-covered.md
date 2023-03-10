# 多传感器安全摄像头覆盖你

> 原文：<https://hackaday.com/2016/08/21/multi-sensor-security-camera-has-you-covered/>

家庭安全——尤其是新家的安全——是许多人最关心的问题。市场上有许多安全系统可供选择，但对于那些需要技能的人来说，当受到自己设计的系统保护时，将事情掌握在自己手中可以增加内心的平静。[Armagan C.]创造了他们近乎完美的[多传感器安全模块](https://hackaday.io/project/13054-home-security-system-v2)来警惕潜在的窃贼。

从他们以前的 Arduino +以太网摄像头(喜欢触发假警报)升级而来,[Armagan]这次选择了一个二手的 Raspberry Pi model B+摄像头模块和 WiFi 连接。他们还升级了该装置，配备了热传感器、液化石油气和二氧化碳气体传感器以及运动跟踪报警器。[Armagan]还建立了一个直播功能，以 1 小时为单位记录视频——每天删除它们——并通过使用坠毁无人机的飞行控制器通过串行端口路由传感器数据来规避文件描述符泄露的问题。事实证明，它也优于传统的报警器，因为定制的软件不需要在午夜去洗手间时解除安全区域。

 [https://www.youtube.com/embed/-mNEIxaxuPI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-mNEIxaxuPI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



承认热传感器目前工作不太好，如果多普勒雷达可以廉价获得，它可能会被取代。关于该项目的更多细节可以在找到[。这主要是一个室内安全摄像头选项，所以你仍然需要](http://psychip.net/video/new-gadget-wireless-sensor-station)[一个室外摄像头](http://hackaday.com/2016/05/23/16-megapixel-outdoor-security-camera-on-the-cheap/)来真正加强你家的防御。

【感谢提示阿玛！]