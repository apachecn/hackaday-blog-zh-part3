# 物联网的白帽病毒

> 原文：<https://hackaday.com/2015/10/02/a-white-hat-virus-for-the-internet-of-things/>

尽管没人知道物联网的确切用途，但它正在大受欢迎。投入物联网设备的营销资金比百事可乐的新汽水还多。这是一项新技术，随之而来的是一些问题:这些设备非常不安全，你只需要看看网上的一些闭路电视摄像头就能证明这一点。

对于易受攻击的物联网事物，显而易见的解决方案是让人们改变他们设备上的登录凭证，但事实证明这对大多数人来说太难了。一个更好的解决方案，如果其意图有问题，将是一种病毒，它会关闭路由器上所有打开的端口，杀死 Telnet，并提醒用户更改密码。[赛门铁克发现了这样一种病毒](http://www.symantec.com/connect/blogs/there-internet-things-vigilante-out-there)。它被称为 Wifatch，它将恶意软件的概念转化为一种向善的力量。

Wifatch 是一段代码，它可以溜进路由器和其他物联网设备的后门，关闭 Telnet 以防止进一步感染，并留下消息告诉主人更改密码和更新设备固件。Wifatch 也没有保守任何秘密:大部分代码都是用不模糊的 Perl 编写的，并且有调试消息可以方便地分析代码。这是一段应该被拆开的代码，这段代码包含了一条针对国家安全局和联邦调查局特工的评论:

```
To any NSA and FBI agents reading this: please consider whether defending
the US Constitution against all enemies, foreign or domestic, requires you
to follow Snowden's example.
```

虽然 Wifatch 的设计者将所有代码都公开，并且可以说做了*件好事*，但是这种白帽病毒也有可能存在阴暗面。Wifatch 连接到用于分发威胁更新的对等网络。通过代码中的后门，wi patch 的作者可以想象出将 wi patch 感染设备的整个网络变成一个个人僵尸网络。

虽然只需简单的重启就可以轻松地从路由器上删除 Wifatch，并且可以通过更改默认密码来防止再次感染，但这是一个有趣的虚拟警戒案例。这可能不是告诉人们需要更改路由器密码的最佳方式，但很难对结果提出异议。

[图片来源:[表头](http://www.symantec.com/connect/blogs/there-internet-things-vigilante-out-there)，[大拇指](http://maditsmadfunny.wikia.com/wiki/Spy_vs._Spy)