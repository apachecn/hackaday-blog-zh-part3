# 测量廉价手持式收发器的杂散发射

> 原文：<https://hackaday.com/2016/12/14/measuring-spurious-emissions-of-cheap-handheld-transceivers/>

如果你买了一个足够便宜的业余无线电收发机，可以作为一个合理的礼物或礼物，你会得到你所付出的。如果对廉价无线电的广泛分析有任何意义的话，你在杂散发射部门得到的比你付出的多一点。

美国的业余无线电受 [FCC 的第 97 部分规则](http://www.ecfr.gov/cgi-bin/text-idx?c=ecfr&SID=336ab7469b61ecbfa15086dbf1bf2c59&rgn=div5&view=text&node=47:5.0.1.1.6&idno=47#se47.5.97_1307)监管，特别关注子部分 d 中的发射机技术规范。杂散发射需要远低于发射机基频的平均功率，并且【Megas3300】怀疑现成的[宝丰 UV-5RA 双频收发器](https://www.amazon.com/Baofeng-136-174-400-480-Dual-Band-Transceiver/dp/B009MAKWC0/ref=sr_1_3?s=electronics&ie=UTF8&qid=1481669135&sr=1-3&keywords=baofeng+uv5ra)有点不合规格。他让这台价值 20 美元的收音机接受了一系列测试，使用的设备很容易就比测试对象贵了两个数量级。用瓦特计验证功率输出，选择合适的衰减器，用频谱分析仪扫描输出信号。仔细的测量表明，宝丰的部分或全部谐波远远超过了 FCC 的限制。[Megas3300]测试了其他几款无线电，结果证明大部分都是兼容的，但无论结果如何，测试程序都有很好的记录和信息，非常值得一看。

这些收音机的预期市场更多的是未经许可的人群，而不是合规的火腿，所以它们不合规格也就不足为奇了。一个业余爱好者可能想让这些装备重新符合低通滤波器，为此目的[RF 饼干](http://hackaday.com/2016/03/26/rf-biscuit-is-a-versatile-filter-prototyping-board/)可能证明是有用的。

[通过[无线电/业余无线电](https://www.reddit.com/r/amateurradio/comments/5hz4h9/spurious_emissions_measurement_of_the_20_baofeng/)