# DNS 隧道:通过其他人的 WiFi 获取数据

> 原文：<https://hackaday.com/2016/08/07/getting-the-data-out-over-other-peoples-wifi/>

[KC Budd]想做一个跟踪汽车的 GPS 装置，他想让它能给家里打电话。给 GSM 手机添加数据套餐太容易了(也更贵)，所以他选择了黑客的方式:[每当设备发现一个开放的 WiFi 热点](http://www.phreakmonkey.com/2016/08/towl-telemetry-over-opportunistic-wifi.html)时，就通过 DNS 查询传输数据。结果是设备发送的数据很少，而且是零星地发送，但却能把信息发出去。

这个系统不太可靠——你受到该地区开放 WiFi 点的支配。这无疑落入了道德灰色地带，但造成的伤害很小。他发送了一个 16 字节的有效载荷，加上 DNS 调用开销。他又不是在下载猫玩键盘的动画 gif。例如，我们会很乐意每小时为数百台设备提供这项服务。

如果你是新来的，通过 DNS 请求隧道传输数据的想法就像山一样古老，甚至更古老，我们甚至已经在不同的场合介绍过这种黑客技术。但是[KC]增加的是在[的 GitHub](https://github.com/phreakmonkey/towl)上的一站式代码商店和 GPS 应用程序。

为什么我们没有在你的项目中看到更多的应用呢？还是你们都在通过 DNS 传输数据，只是不愿意公开承认？可以匿名在评论里发帖！