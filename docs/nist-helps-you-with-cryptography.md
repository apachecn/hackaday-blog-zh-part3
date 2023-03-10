# NIST 帮助你学习密码学

> 原文：<https://hackaday.com/2017/05/25/nist-helps-you-with-cryptography/>

正确使用加密技术并不容易，在微控制器等受限设备上更是如此。RAM 通常是瓶颈——在 AVR 上计算阿沙-2 哈希时，您会粉碎您的堆栈——但计算能力和闪存代码存储空间等其他资源也很宝贵。削减标准算法以在这些约束下工作，打开了特定于实现的缺陷的潘多拉盒子。

NIST 挺身而出，在 2013 年启动了一个轻量级加密项目，现在[已经发布了第一份报告](https://www.nist.gov/publications/report-lightweight-cryptography)，而[也发布了 PDF 格式的报告](http://nvlpubs.nist.gov/nistpubs/ir/2017/NIST.IR.8114.pdf)。该项目正在进行中，所以不要指望如何指导。事实上，报告的大部分内容是描述小型设备上的加密问题。鉴于物联网安全的现状，仅仅定义问题就是一个巨大的贡献。

尽管如此，还是有一些具体的建议。下面是一些剧透。对于加密，他们推荐了 AES-128 的精简版本，这是一种在大型机器上经过充分测试的分组密码。对于消息认证，他们乐于使用[伽罗瓦/计数器模式](https://en.wikipedia.org/wiki/Galois/Counter_Mode)和 AES-128。

我最感兴趣的是哈希，失望而归；结论是，SHA-2 和 SHA-3 家族只是需要太多的状态(和 RAM)，它们不做推荐，让你在不太为人知的函数中挑选:看看 [PHOTON](https://sites.google.com/site/photonhashfunction/design) 或 [SPONGENT](https://sites.google.com/site/spongenthash/) ，它们仍在积极研究中。

如果你认为小型设备的安全很容易，通读从第 12 页开始的 22 个问题的清单。如果你正在寻找一个好的起点来阅读最新的技术，参考书目是广泛的。

你的税金在起作用。谢谢，NIST！

感谢[acs]的提示！