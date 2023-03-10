# 分布式审查还是敲诈？物联网 Vs 布莱恩·克雷布斯

> 原文：<https://hackaday.com/2016/09/29/distributed-censorship-or-extortion-the-iot-vs-brian-krebs/>

现在是正式的了。我们几天前报道过的被破纪录的分布式拒绝服务(DDOS)攻击击中的特定网站是白帽安全记者【Brian Krebs】:[Krebs on Security](https://krebsonsecurity.com/2016/09/krebsonsecurity-hit-with-record-ddos/)。

在 DDOS 攻击期间，他的网站获得了每秒 600 千兆的流量。它不涉及[放大或反射攻击](https://www.us-cert.gov/ncas/alerts/TA13-088A)，而是一个僵尸家用电器的分布式网络:路由器、IP 网络摄像头和数字录像机(DVR)。他们所做的只是为他的网站创建 HTTP 请求，但这些机器人的数量远远超过 100，000 个。

最后，[克雷布斯的] ISP，Akamai 不得不把他掉了。一开始，他从他们那里获得了无偿服务，尽管他们过去曾为他抵御过 DDOS 攻击，但在这种情况下，他们继续下去的成本太高了。Akamai 的一名高管估计，如果继续防御的话,[将花费数百万](https://www.bostonglobe.com/business/2016/09/23/cybercrooks-akamai/qOAhvHoohJcmkxIwg5ChKO/story.html),而【布莱恩】并不责怪他们。但当 Akamai 放弃屏蔽时，他的主机提供商就会受到抨击。[Krebs]告诉 Akamai 将他的域名重定向到[本地主机](https://en.wikipedia.org/wiki/Localhost)，然后他就消失了。

## 审查制度的民主化

[Krebs]从整个事件中得到的启示可以在他的博客文章中总结出来(现在他又上线了):“[审查制度的民主化](https://krebsonsecurity.com/2016/09/the-democratization-of-censorship/)”。这值得一读，我们不会试图超越布莱恩·克雷布斯。然而，他的基本观点是，过去需要一个民族国家来审查网络上的信息——强人政权或在大型互联网服务提供商中有幽灵般联系人的机构。但是，如果任何脚本小子能够利用具有硬编码密码的物联网设备将选定的网站从网络上拉下来，游戏就发生了根本性的变化。

你必须是一个相当敬业的无政府主义者，才能说这是一个好的发展。毕竟，我们没有用政府审查和监视来换取私人审查。舞台上还有一个演员，更糟糕的是，那个演员是罪犯。我们知道[克雷布斯]的意思是讽刺，但“民主化”是一个如此美好的词，我们讨厌看到它在这里使用。

[![projectshield-580x381](img/990d218ea90a71e75bc5f507f9c5ec90.png)](https://hackaday.com/wp-content/uploads/2016/09/projectshield-580x381.png) 【克雷布斯】也证明了动机充分的团体现在可以有效地压制记者，并证明了我们如何才能保护互联网上的言论自由。对他来说，[Krebs]现在是谷歌项目( [Project Shield](https://jigsaw.google.com/projects/#project-shield) )的一部分，旨在减轻这种攻击。(具有讽刺意味的是，谷歌仍然认为它的对手是“强大的机构”，而不是“地下室里的某个家伙”。)

### 组织犯罪

从时间上看，似乎是“vDOS”在出售 DDOS 服务，其中两人现在已经入狱。他们和[布莱恩]有过节，他们把他拿下了。但是，虽然在[克雷布斯]案中，T2 可能是个人问题和审查问题，但在大多数情况下，这只是钱的问题。

[![725_ly9jb2ludgvszwdyyxbolmnvbs9zdg9yywdll3vwbg9hzhmvdmlldy8wzmmxzmq2m2iyzjiwm2izywmwmjhlzgvlmjjimwrinc5wbmc](img/df8c0cb98a21052763161a73557ae277.png)](https://hackaday.com/wp-content/uploads/2016/09/725_ly9jb2ludgvszwdyyxbolmnvbs9zdg9yywdll3vwbg9hzhmvdmlldy8wzmmxzmq2m2iyzjiwm2izywmwmjhlzgvlmjjimwrinc5wbmc.jpg) 在过去的几年里，[勒索软件](http://arstechnica.com/security/2015/06/fbi-says-crypto-ransomware-has-raked-in-18-million-for-cybercriminals/)已经变得如此普遍，安全社区之外的人甚至都听说过它。但是 DDOS 赎金攻击才是真正的增长行业。这些勒索者现在甚至有了可爱的绰号:“booters”或“stressers”。

[Krebs]估计，获得在类似攻击事件中保护他的 DNS 服务将使他每年花费 10 万到 30 万美元。很明显，他不能为合法的保护支付那么多，但是针对这种攻击的保护成本应该提供这些罪犯可以要求多少赎金的上限。作为另一个数据点，交付给 [ProtonMail](https://protonmail.com/) 的勒索信表明，实际的[市场价低至 20 比特币](https://blog.radware.com/security/2016/05/ransom-ransom-everywhere/#comments)——大约 12000 美元。(他们受到打击，顾客抱怨，而[他们支付了](https://cointelegraph.com/news/protonmail-pays-bitcoin-ransom-to-stop-ddos-attack)。)

关键是，一个人可以通过运行一个 DVR 僵尸网络，威胁网站关闭一两天，过上好日子。我们认为这比(克雷布斯的)对审查的恐惧更有可能构成威胁。DDOS 勒索是非法和错误的，但是哪里有钱，哪里就有适合犯罪的罪犯。

## 为什么？为什么不呢？

鉴于 DVR 的僵尸网络可以转换成现金，有人问他为什么会有人这么做。在攻击之前，无论是谁在运行物联网僵尸网络，他们都控制着 100，000 多台计算机，所有这些都完全在雷达的监控之下。但是现在所有这些机器的 IP 地址都是已知的，也许有一天有人会着手修补这些设备。谁会烧一个巨大的僵尸网络来让布莱恩发疯呢？

[![deathstar](img/8e23b8be4c18bd8d14a220fe922c2391.png)](https://hackaday.com/wp-content/uploads/2016/09/deathstar.png) 【克雷布斯’】的回答很恐怖，但很可能是恰到好处的。谁发动了袭击并不重要。外面有数千万不安全的物联网设备。在这里用掉 10 万英镑，否则就是沧海一粟。在今年上线的数十亿物联网设备中，有多少现在已经有了硬编码的管理员密码？在不久的将来，有多少*会被发现易受未知的攻击？*

我们还愤世嫉俗地认为，打击[Brian Krebs]对销售 DDOS 敲诈的团体来说是一个很好的广告——如果有一个系统管理员没有听说过这个概念，他们现在应该听说了。Akamai 吹捧抵御这种攻击的成本是“启动者”可能希望的最好宣传。扩大你的僵尸网络，击中一个富有的目标，也许你可以接近 10 万美元的回报。(不是实际建议。)

不管动机是什么，有数百万未打补丁的路由器和硬盘录像机等着加入下一个僵尸网络。2016 年 6 月，苏库里写了一篇关于防御一个只有 25000 台闭路电视设备的[“大型”僵尸网络](https://blog.sucuri.net/2016/06/large-cctv-botnet-leveraged-ddos-attacks.html)的文章。8 月，Level 3 写了一个品牌的 DVR 超过 100 万台的[漏洞。被认为是“大型”僵尸网络的数量在几个月内翻了两番，而一个人所能产生的流量也保持不变。而这一切只是冰山一角。](http://blog.level3.com/security/attack-of-things/)

### 到处都是微型无头服务器

[![twoservers](img/53d8491d3c66b059b3ced9edff9193f8.png)](https://hackaday.com/wp-content/uploads/2016/09/twoservers.png) 这个问题是我们在之前[已经写过的，或多或少](http://hackaday.com/2015/09/17/tiny-headless-servers-everywhere/)[拐弯抹角](http://hackaday.com/2015/10/08/get-your-internet-out-of-my-things/)。物联网设备包含连接到互联网的无头计算机，可以在没有人类监督的情况下与外界对话。他们是外行认为的服务器:一个没有图形用户界面的“盒子”，远程访问，24/7 提供数据。物联网设备和传统服务器之间的重要区别在于，更大的服务器有一个管理员，他/她可以应用补丁和软件工具来帮助他/她监视事物。

对于物联网设备，更新、升级、审计和管理的能力仍处于初级阶段。此次攻击中使用的一些 DVR 设备的 root 密码自 2013 年以来就已为人所知，针对这些设备的可脚本化攻击被包含为一个 [Metasploit 模块](https://www.rapid7.com/db/modules/auxiliary/scanner/misc/cctv_dvr_login)。有能力的系统管理员现在应该已经修补好了。(一个有能力的制造商绝不会让这种情况发生。)

相反，这些设备是由(数百万)人管理的，他们甚至不知道里面有一台微型计算机。这些人不知道下载和刷新固件升级，或者不明白他们需要为一个*网络摄像头*这样做。

刻板印象比比皆是，作为相对成熟的用户，我们可能会沾沾自喜。但是你 100%确定在过去的几个月里你的路由器没有固件更新吗？我们有比照看我们的设备更好的事情要做。

## 怎么修？

[![vDOS's Website, with prices](img/ee894b5486e95fcdbcb43c3781b31118.png)](https://hackaday.com/wp-content/uploads/2016/09/vdoshome.png)

vDOS’s Website, with prices

物联网家电的安全问题是真实存在的，和大哥用你的窝告诉你客厅现在是什么温度无关，也不是我们喜欢那样。利用物联网设备的僵尸网络已经成为一种可行的犯罪选择。未打补丁的物联网设备是目前的 Windows XP 机器:它们是公共威胁，因为它们支持犯罪活动。这需要行业的参与和用户教育来帮助我们走出困境。

一种解决方案是远程推送固件升级。当然，这也是恶意软件传播的一种方式，但比起保留硬编码的管理员密码，或者运行带有已知可利用漏洞的过时软件，这种方式的危险性可能要小一些。有许多已知的坏方法来实现这一点:例如，所有“隐藏”在 EEPROM 中的设备只有一个密钥。有哪些好的方法？

人们不喜欢改变，虽然，和沉重的手(你好，Windows 10！)、延迟或失败的推送更新给整个机制带来了不好的名声。公司倒闭或者干脆决定不再支持他们的产品。其他公司根本不在乎。我们不能指望企业永远保护我们的设备，因为他们没有经济动机这么做。

简而言之，消费者物联网僵尸网络问题是一个棘手的问题，而且我们还没有听说过这个问题。我们该怎么办？