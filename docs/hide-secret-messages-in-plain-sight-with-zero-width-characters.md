# 用零宽度字符隐藏秘密信息

> 原文：<https://hackaday.com/2018/04/15/hide-secret-messages-in-plain-sight-with-zero-width-characters/>

指纹文本真的很俏皮；对字符串中的隐藏数据进行编码的能力带来了大量的机会。例如，你的团队中有人泄露机密信息，但你不知道是谁。只需向每个团队成员发送一些机密文本，其中包含他们的姓名。等待它被泄露，然后从文本中提取名字——经典的金丝雀陷阱。

![](img/9cfe9a69c0f27a08b5428fad38d9f39d.png)

这里有一个方法，[使用零宽度字符](https://github.com/vedhavyas/zwfp)隐藏文本中的数据。与其他各种文本指纹识别方式不同，如果格式被去除，零宽度字符不会被删除，这使得在不重新键入文本或使用特殊工具的情况下，几乎不可能删除它们。事实上，你将很难发现它们——甚至终端和代码编辑器都不会显示它们。

为了使这个过程易于执行，[Vedhavyas]创建了一个命令行实用程序来使用任何文本嵌入和提取有效负载。秘密消息中的每个字母都被转换成二进制，然后用零宽度字符编码。一个[零宽度非连接符](https://en.wikipedia.org/wiki/Zero-width_non-joiner)字符用于 0，一个[零宽度空格](https://en.wikipedia.org/wiki/Zero-width_space)字符用于 1。

[Vedhavyas']工具的灵感来自于[Tom] 的一篇[帖子，他使用了一个 javascript 示例(](https://medium.com/@umpox/be-careful-what-you-copy-invisibly-inserting-usernames-into-text-with-zero-width-characters-18b4e6f17b66)[和在线演示](https://umpox.github.io/zero-width-detection/))来解释正在发生的事情。这让您可以验证粘贴文本时不会丢失隐藏数据的说法。尝试将其粘贴到文本编辑器中。我们能够从那里再次复制它，并检索数据，但它没有保存下来，并被猫到命令行。

当然，为了让你的编码游戏*真正*紧凑，你应该考虑给自己买一块[英格玛手表](https://hackaday.com/2015/03/23/enigma-machine-wristwatch/) …

 [https://www.youtube.com/embed/3V6ohXMTP3Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3V6ohXMTP3Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

