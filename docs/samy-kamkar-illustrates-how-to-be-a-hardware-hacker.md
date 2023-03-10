# Samy Kamkar 展示了如何成为一名硬件黑客

> 原文：<https://hackaday.com/2016/12/19/samy-kamkar-illustrates-how-to-be-a-hardware-hacker/>

Samy Kamkar 因许多事情而闻名，但最近他的硬件安全黑客才引人注目。值得一提的是，尽管没有硬件方面的背景，Samy 能够与最好的硬件研究人员一起工作。在 Hackaday 超级会议上，他为那些试图带着令人兴奋的新电子产品走上探索之路的人提供了建议。有人可能会说这是如何成为硬件黑客的速成班。

 [https://www.youtube.com/embed/tlwXmNnXeSY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tlwXmNnXeSY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 低成本开发工具

萨米的第一点建议是做研究。那里有大量免费的信息——首先要看的是你已经拿在手里的硬件。把它拆开，拆了，搞清楚它的工作原理，开始学习你不懂的部分。

谷歌是你的朋友，帮助你发现他人的工作，这样你就可以在他们的努力基础上再接再厉。专利搜索是了解一个设备如何工作的好方法。联邦通信委员会的文件也非常有用，几乎任何里面有收音机的东西都可以找到。有时你会发现整个原理图和通信方案作为该文件的一部分。有了这些信息，就可以使用简单的工具来监听无线网络。

说到工具，萨米不会在他的工具箱里囤积独角兽。他最喜欢去的地方之一是 Arduino。当它太小或太慢时，他会抓住一个 Teensy，他可能会伸手去拿 FPGA，但只用于极少数需要极快计时的情况。不，他几乎用了我们都很熟悉的工具。在他的工作台上，你会发现一个 Saleae 逻辑分析仪，数字万用表，示波器，和你的基本焊接工具。

### 技巧在哪里？

那么，如果这些工具简单而且广泛可用，Samy 怎么可能设计出如此神奇的黑客工具呢？我认为他的直觉很准，知道什么时候该走正确的路来解决问题。看来他的诀窍并不是什么都懂，而是知道应该走出去学习。他在演讲中展示的三种非常酷的黑客手法都体现了这种技巧。

### CC 欺骗

他用一卷电线和一个 ATtiny 微控制器制作了自己的信用卡磁条——他称之为 [MagSpoof](http://hackaday.com/2015/11/25/defeating-chip-and-pin-with-bits-of-wire/) 。这怎么可能呢？他的过程始于探索信用卡的实际运作方式。他演示了将一张卡浸在氧化铁中——粒子粘在磁条上，你可以用肉眼读出数据。这里的一个飞跃是:如果条纹是磁性的，我就不能用线圈来做吗？答案是肯定的。他制作了线圈，把它放在一个条形阅读器旁边，回放数据。有趣的是，在您采集的条带数据中翻转一点意味着读取器永远不会要求您使用芯片读取器。

### 固定码和滚动码

两个稍微相关的黑客是那些欺骗车库开门器和汽车钥匙的黑客。车库门开启器通常有一个固定的代码(由 DIP 开关设置),该代码总是从遥控器广播到接收器。很容易想象如何捕获和回放这些代码。萨米想在没有俘虏的情况下做这件事。没有那么多组合，30 分钟左右就能蛮力了。他通过消除传输之间的等待，进一步将时间缩短到三分钟。但正是对德布鲁因序列的深入研究让他在八秒钟内破解了任何一扇固定密码的车库门！这款叫做 [OpenSesame](https://samy.pl/opensesame/) ，使用了在这里看到的 IM-ME 儿童玩具[做了很多无线欺骗](https://hackaday.com/tag/im-me/)。

车辆更加坚固。密钥卡使用滚动代码序列，您不能捕获和重复使用，当然也不能暴力破解。诀窍是在你从发射机中捕获代码的同时干扰接收机。这样做两次，你就有了两个好的代码——第一个你可以发送出去解锁汽车，用户认为这是正常的行为。实际上，你有一个磁性附着在车辆上的设备，它总是比最新的代码落后一个代码。当攻击者想要进入车辆时，只需按下这个装置上的按钮。

最后一次攻击是通过一个 Teensy 3.1 和两个连接在试验板上的 CC1101 板完成的。太不可思议了！所有这些都可以作为路线图，帮助我们了解将我们的世界缝合在一起的底层技术。希望 Samy 的讲话以及他在工作中发现的硬件安全漏洞能够激励下一代工程师构建更好、更安全的系统，并激励下一代安全研究人员找到新的漏洞。