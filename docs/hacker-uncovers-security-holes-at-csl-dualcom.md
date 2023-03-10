# 黑客发现 CSL Dualcom 的安全漏洞

> 原文：<https://hackaday.com/2015/11/26/hacker-uncovers-security-holes-at-csl-dualcom/>

英国一家著名的安全系统制造商 CSL·杜亚康公司反驳了[赛博·吉本斯]关于他们的 CS2300-R 模型漏洞百出的说法。正在讨论的特定设备是位于报警系统和他们的监控设备之间的通信链路。它的工作是让这两个系统通过互联网、有线电视或手机信号塔相互交流。不用说，它内置了一些强大的安全功能来防止篡改。然而，安全似乎[不太安全](http://cybergibbons.com/security-2/csl-dualcom-cs2300-signalling-unit-vulnerabilities/)。[Cybergibbons]有条不紊地戳戳 CS2300-R 的位和字节，直到它放弃了它的秘密。事实证明，它所使用的加密技术只比基本的凯撒密码高了几步。

凯撒密码只是将数据移动一个数值。该值是密钥。例如，代码 IBDLBEBZ 是用凯撒密码加密的。不难看出“1”的移位会暴露黑客日。这…不是安全性，相当于一个 [TSA 锁](http://hackaday.com/2015/09/18/dear-tsa-this-is-why-you-shouldnt-post-pictures-of-your-keys-online/)，如果那样的话。CS2300-R 采用 Caesar 密码并对其进行修改，这样，当您向下移动数据字符串时，密码密钥会发生变化。[Cybergibbons]能够找出密钥是如何变化的，正如他所说，这揭示了“通往王国的钥匙”。

这个故事还有更多的内容。请务必阅读[他的详细报告](http://cybergibbons.com/wp-content/uploads/2015/11/CSL-Dualcom-CS2300-Security-Analysis-2015-v4.pdf) (pdf)，并在下面的评论中让我们知道你的想法。

我们提到过 CSL·杜亚康对调查结果有争议。他们的回应可以[在这里阅读](http://cybergibbons.com/wp-content/uploads/2015/11/CSL_statement.txt)。