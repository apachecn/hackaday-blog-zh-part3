# 又一天，又一个“物联网”后门

> 原文：<https://hackaday.com/2017/03/06/another-day-another-iot-backdoor/>

如果你需要除了“只是为了好玩”之外的任何理由来侵入你自己的小工具，看起来几乎所有由 DBLTek 制造的 GSM-to-IP 桥接设备都内置了一个可远程访问的“秘密”后门帐户。我们通过 Slashdot 得到了链接[，这个链接又链接到了 Techradar](https://tech.slashdot.org/story/17/03/05/1828202/hidden-backdoor-discovered-in-chinese-iot-devices) 上的[这篇报道。两者都包括“中国”和“物联网”这两个可怕的词，尽管这些设备似乎是针对小企业的，但这些天来一切都是“物联网”，对不对？](http://www.techradar.com/news/dangerous-backdoor-exploit-found-on-popular-iot-devices)

然而，*可怕的是,*后门并不仅仅是一个草率的调试账户，而是只能通过精心设计的定制登录协议才能进入。更糟糕的是，当该公司被联系到后门帐户时，他们不是通过删除帐户来“修复”问题，而是通过使“秘密”登录程序更加复杂几个步骤。也就是说，他们根本没有解决问题。

这个问题是由安全公司 Trustwave 发现的，但是他们不能一直检查市场上的每一个设备。我们可能是在向唱诗班布道，但如果你曾经想知道为什么能够闯入你自己的东西是重要的，这里有另一个提醒。