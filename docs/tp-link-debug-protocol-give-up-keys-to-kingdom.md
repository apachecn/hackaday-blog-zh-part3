# TP-Link 调试协议将密钥交给了王国

> 原文：<https://hackaday.com/2016/12/14/tp-link-debug-protocol-give-up-keys-to-kingdom/>

如果标题让今天的黑客攻击听起来很容易，请放心，它不是。但是如果你对嵌入式设备黑客感兴趣，请继续阅读。

[Andres]想在一台便宜的家用路由器上安装一个定制的操作系统固件，所以他买了一台已知可刷新的路由器，却发现新版本的固件让安装变得很困难。我们都经历过。但是，安德烈斯没有把这款设备扔进壁橱，而是让它屈服，发现固件中的一个错误，利用它，[把它写给制造商。(就在我们即将发布的时候:在这里发布降级漏洞利用](https://cxsecurity.com/issue/WLB-2016110201)的[代码。)](https://github.com/P0lako/tl-wa5210gV2_Downgrade)

这不是一个周末的黑客活动——这需要一个专业人员花费许多小时的认真劳动。但是这变得容易多了，因为 TP-Link 使调试协议保持活动状态，监听 LAN 接口，并且不需要认证。[Andres]在专利中找到了他需要的大部分信息，并很快对正在运行的设备进行了调试。

在根据他从制造商网站上下载的固件进行了一些重型静态逆向工程后，他在代码中发现了缓冲区溢出的机会，并设法通过调试链接运行了自己的代码。

因为(安德烈斯)是一名安全专家，他因发现这样的漏洞而获得报酬，但也因为让它们听起来不吉利而获得报酬。不过，他指出，你只能通过本地局域网达到调试协议，而不能通过整个网络。所以你更有可能利用这个漏洞来刷新你选择的固件，而不是任何坏人会这么做。(不是 bug，是特性！)但是，这仍然是一个可怕的黑客！

感谢[诺伯]的提示！