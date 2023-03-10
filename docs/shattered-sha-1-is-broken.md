# 破碎——SHA-1 被打破了

> 原文：<https://hackaday.com/2017/02/23/shattered-sha-1-is-broken/>

来自谷歌和 CWI 阿姆斯特丹的团队刚刚宣布:他们[制造了第一个 SHA-1 哈希碰撞](https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html)。该攻击需要超过 9，223，372，036，854，775，808 次 SHA-1 计算，相当于 6，500 年单 CPU 计算和 110 年单 GPU 计算的处理能力。虽然这可能看起来势不可挡，但如果你是一个国家支持的攻击者，这是一个实际的攻击。或者你控制了一个足够大的僵尸网络。或者你只是能够在云计算上花一些钱。这是可行的。毫无疑问，这不是一次暴力攻击，这将需要大约 12，000，000 个单 GPU 年才能完成。

SHA-1 是一种 160 位标准加密哈希函数，广泛用于数字签名和文件完整性验证，如数字证书、PGP/GPG 签名、软件更新、备份系统等。很久以前，它被提议作为 MD5 的安全替代品，MD5 自 1996 年以来就被认为是有缺陷的。2004 年的研究表明，MD5 不具有抗冲突性，不适合 SSL 证书或数字签名等应用。2008 年，一组研究人员使用 200 台 Playstations 3 演示了如何破解基于 MD5 的 SSL。

早在 2005 年，针对 SHA-1 的理论攻击就已经众所周知。2015 年，一场针对整个 SHA-1 的袭击被展示出来(命名为 *the SHAppening* )。虽然由于一些技术方面的原因，这没有直接转化为对完整 SHA-1 散列函数的碰撞，但是它破坏了对 SHA-1 的安全声明。通过这种被称为*粉碎*的新攻击，该团队展示了对 SHA-1 算法的实际攻击，产生了两个具有相同校验和的不同 PDF 文件。

按照谷歌的漏洞披露政策，完整的工作代码将在三个月内发布，它将允许任何人在给定两个不同图像和一些尚未指定的先决条件的情况下，创建一对散列到相同 SHA-1 和的 pdf。

现在，建议在你的软件上开始使用 SHA-256 或 SHA-3。Chrome 浏览器已经警告说，如果一个网站有 SHA-1 证书，Firefox 和其他浏览器肯定会跟进。与此同时，与往常一样，传统系统和物联网类设备的日子将会更加艰难。