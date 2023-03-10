# Samy Kamkar:安全未来的逆向工程

> 原文：<https://hackaday.com/2018/01/02/samy-kamkar-reverse-engineering-for-a-secure-future/>

举手表决:你们中有多少人把车停在车道上，走到你家门口，按下你的车的遥控钥匙按钮，以为它会打开前门？我们可能都做过，结果觉得有点迟钝，但当你想到它时，它会非常方便，特别是每个手臂上都挂着购物袋，牙齿之间咬着邮件。毕竟，我们生活在未来——难道你的房子不应该足够智能，知道你什么时候在家吗？

卓越的逆向工程师 Samy Kamkar 可能会这样认为，但鉴于他最近驾驶汽车的经历，他很可能会有所保留。萨米在 11 月参加了 2017 年黑客日超级会议，讨论了利用被动汽车进入系统安全漏洞的细节，并在我们的埃利奥特·威廉姆斯结束演讲后与他进行了一对一采访。Samy 对车辆网络安全有一些有趣的见解，但他在探索这些系统的限制时获得的实践知识为成为现实世界的逆向工程师提供了一些有力的教训。

 [https://www.youtube.com/embed/B2MvoBRzrm4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B2MvoBRzrm4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Samy 告诉 Elliot，他对车辆安全的兴趣源于一个朋友，她的车被撬了。她锁上车，然后走开了，但是不知何故，一个小偷能够利用被动进入和点火系统打开车，偷走一些东西。Samy 在他的演讲中深入探讨了这一漏洞，但尽管这很有意思，关键不在于他如何剖析这一漏洞，而在于他用来解决一般问题的方法。

Samy 是从软件领域进入硬件黑客领域的，他自己也承认，他没有电路设计背景，当他打开设备的盖子时，无法立即知道他在看什么。但是他将代码骑师的敏感带到了逆向工程过程中，这提供了某些优势。当遇到棘手的问题时，软件人员通常首先求助于互联网，因此对于硬件挑战，Samy 强烈建议在拿螺丝刀之前打开笔记本电脑做一些研究。他还提供了获取外壳上没有任何标识的零件数据表的技巧。

[![](img/21aabb54365761d9c6d6f876bbfba40e.png)](https://hackaday.com/wp-content/uploads/2017/12/samy2.png) 那么逆向工程师的工具箱里有什么呢？对于萨米来说，答案出奇的少。除了打开箱子的基本手动工具，Samy 还严重依赖 HackRF SDR 收发器进行无线开发。当然，对于初学者来说，更便宜的 RTL-SDR 加密狗就可以了。有趣的是，Samy 不一定会在他的荒岛工具包中包括示波器；作为一名软件背景的人，他多年来一直从数字的角度处理项目，避开事物的模拟方面，放弃对示波器的需求。随着经验的增加，他发现示波器帮助他处理诸如定时攻击之类的事情，逻辑分析仪也是一个有用的工具。

至于最初的密钥卡攻击，激起了他对车辆网络安全的兴趣，萨米在采访中对该项目的结果做了一些尝试。他能够制造一种设备来执行射频中间人攻击，以解锁和启动汽车，他在完整的演讲中讨论了[的细节。至于接下来会发生什么，萨米乐观地认为制造商将克服 MITM 的攻击，可能通过飞行时间分析来确保 RFID 信号来自车辆附近的合法所有者，而不是来自停车场对面带着欺骗设备的小偷。似乎萨米也期待着打破这些系统，我们很想看看他会提出什么。](https://youtu.be/RpD-yMcg4P4)

 [https://www.youtube.com/embed/RpD-yMcg4P4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RpD-yMcg4P4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

