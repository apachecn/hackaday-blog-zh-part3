# 使用 VPN 解除与您所在位置的联系

> 原文：<https://hackaday.com/2017/10/12/untether-from-your-location-with-a-vpn/>

到目前为止，我们大多数人都知道使用 VPN 的好处:它们使一个人的在线活动变得私密(至少从你的 ISP 的角度来看是这样)，它们还可以让你看起来好像是在一个不同的地方，而不是你实际所在的地方。这对于观看奥运会这样的赛事尤其重要，因为奥运会可能会在不同的时间、不同的国家播放不同的节目。这也开始成为像网飞这样的服务的一个问题，这些服务允许某些领域的内容，但不允许其他领域的内容。

虽然 VPN 可以帮助解决这个问题，但如果您必须经常这样做，为特定目的设置 VPN 可能会很繁琐。幸运的是，[clashtherage]已经创建了一个带有 Raspberry Pi 的[路由器，它可以自动处理所有复杂的 VPN 路由](http://mobiephonetech.ml/2017/10/07/unblock-netflix-using-raspberry-vpn-router/)。就像[我们看到的另一个 RPi 路由器](https://hackaday.com/2013/09/15/turning-a-raspi-into-adblock/)从你所有的互联网流量中清除广告一样，这个路由器接收你所有的流量，并将其发送到你选择的地点。(理论上，人们可以同时使用两者。)

显然，这对网飞公司来说是个问题，事实上，许多服务(比如 craigslist)如果检测到有人使用 VPN，就会开始屏蔽对他们网站的访问。当然，这只会导致 VPN 被阻塞的军备竞赛，它们会找到绕过障碍的方法，等等。如果最终实现了 IPv6，我们可能会有一个解决所有这些问题的方案。