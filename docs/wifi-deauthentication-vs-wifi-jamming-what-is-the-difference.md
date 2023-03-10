# WiFi 去认证 VS WiFi 干扰:有什么区别？

> 原文：<https://hackaday.com/2017/08/13/wifi-deauthentication-vs-wifi-jamming-what-is-the-difference/>

术语在某些时候会让我们混淆。[Seytonic]在下面嵌入的视频中很好地解释了【WiFi 干扰器和解除认证器之间的区别。你们中的许多人已经知道这种区别，但是指出这种区别是很有用的，因为很多人把 deauth 设备称为“WiFi 干扰器”。

在他们的 YouTube 视频中，他们继续解释说，干扰器基本上在所有 WiFi 频道上抛出大量噪声，使频率在距离干扰器给定的距离内不可用。干扰器通常也很贵，大多是非法的，因此很难找到，除非你自己制造。

[另一方面，WiFi 去认证](http://hackaday.com/2011/10/04/wifi-jamming-via-deauthentication-packets/)以一种非常不同的方式工作。WiFi 发送未加密的数据包，称为管理帧。因为这些是未加密的，所以即使网络使用 WPA2，恶意方也可以发送解除认证命令，将用户从接入点上引导下来。不过加密管理帧的 802.11w 还是有希望的。它已经存在了一段时间，但是制造商似乎并不介意，也没有实施它，即使它可以提高 WiFi 设备的安全性，免受这些类型的攻击。

 [https://www.youtube.com/embed/6m2vY2HXU60?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6m2vY2HXU60?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

