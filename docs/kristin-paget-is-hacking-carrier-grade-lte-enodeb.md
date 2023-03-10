# Kristin Paget 正在入侵电信级 LTE ENodeB

> 原文：<https://hackaday.com/2017/12/04/kristin-paget-is-hacking-carrier-grade-lte-enodeb/>

偶尔你运气好的话，会有一件很酷的装备落在你的工作台上，让你去拆卸和探索。就这一点而言，Kristin Paget 获得了当代手机基础设施的一个迷人部分，赚了大钱。她目前正在研究一种电信级 LTE eNodeB，并在 2017 年 Hackaday Superconference 的[关于物联网安全法律的演讲](https://www.youtube.com/watch?v=u5JLub4_gSs)中浏览了一些研究结果，以及两种物联网产品的安全研究结果。

演进节点 B (eNodeB)是 LTE 蜂窝网络的核心。它将天线连接到回程，这是你在公开市场上不会看到的东西，但 Kristin 设法在 DEF CON 上从一家供应商那里买到了一个。听她讲述硬件测试过程是一种真正的享受，我们马上就要谈到这一点。但首先，看看我们在克里斯汀演讲后的第二天早上对她的视频采访。我们了解了她的 eNodeB 研究的进展，并触及了物联网安全的状态，为硬件开发人员提供了前进的建议。

 [https://www.youtube.com/embed/P-gue_8PJMU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/P-gue_8PJMU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在采访中，Kristin 提到 WiFi 肯定不是联网设备最安全的选择，她在她的 Supercon talk 中明确阐述了这一点。

她带的三个硬件设备中的第一个是 WiFi 连接灯泡。我们都做过与 WiFi 连接的“智能”物品的舞蹈:用你的手机连接到它的 AP，加载一个网页，并在你的 AP 上输入你的 WiFi 凭证。在这种情况下，当你输入你的 WiFi 凭据后，灯泡会接入网络，但会继续提供它自己的 AP——带有一个易于搜索的默认密码。当然，问题是你的 WiFi 凭证是以明文的形式显示在灯泡的配置屏幕上的，因此任何人都可以在范围内获得你的家庭 WiFi 凭证。太棒了。

这里违反的物联网法律很容易理解，几乎普遍适用。不要分发纯文本凭据。选择使用唯一的配置凭据，这样不是任何人都可以访问配置界面。将用户权限与所有者权限分开。一旦设备连接到目标网络，不要让供应 AP 处于开启状态。

下一个砧板上是第一代亚马逊破折号按钮。自从它们问世以来，它们一直是黑客的最爱。但是 Kristin 当然不会乐意看到路由器显示 MAC 地址。她通过嗅探按钮上的流量，剖析所使用的证书验证。令人惊讶的发现是，所有第一代 Dash 按钮都期望 SSL 在 2015 年到期，否则它们将无法工作。设计者需要包括一种刷新密钥的方法，否则用户将最终被锁在设备之外。Dash 通过放弃所有使用的 SSL 安全性解决了这个问题。

[![LTE eNodeB hardware](img/00be35184c926a11a9565f3576c2a593.png)](https://hackaday.com/wp-content/uploads/2017/12/lte-enodeb-hacking.jpg)

这就把我们带到了话题的有趣部分:LTE eNodeB。由于这是电信级的，它被设计为使用 10 年或更长时间，在这种情况下，它是一种软件定义的无线电，可以随着新技术的出现而升级。进入操作系统几乎是滑稽的:Kristin 在一个串行端口上发现了 bootspew，并意识到它正在运行 uBoot。她是怎么意识到的？启动过程给你一个 5 秒钟的倒计时，然后按键进入。使用 uBoot 可以很容易地启动 shell，Kristin 对/etc/passwd 的检查包括共享 uid 的散列和多个帐户。看到她是如何熬过这一切的，真令人高兴。

 [https://www.youtube.com/embed/u5JLub4_gSs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u5JLub4_gSs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



设计更安全的硬件的第一步是理解已经变得太常见的错误。从简单廉价的灯泡到精英基础设施，Kristin 提出了一个很好的案例，即我们作为硬件开发人员必须编纂并遵循一套物联网安全法律，以使联网硬件成为我们的资产而不是负担。