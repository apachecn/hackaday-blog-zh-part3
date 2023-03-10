# LastPass 很乐意放弃简单 Javascript 的密码

> 原文：<https://hackaday.com/2016/08/01/lastpass-happily-forfeits-passwords-to-simple-javascript/>

就方便性而言，Lastpass 是一款很棒的软件，但是最近的一次简单的黑客攻击显示了像它这样的软件是多么的不安全。[Mathias Karlsson]因为它的发现获得了 1000 美元的奖金。

Lastpass 的自动填充功能是通过在你访问的网站中注入一些 html 来实现的。它运行一点 Javascript 来解析 URL。然而，解析脚本含糊得可笑。通过改变页面的 URL，在 URL 中插入一些对服务器没有意义的 slugs，攻击者可以让 Lastpass 为其提供任何网站的密码和用户名组合。

在 [HackerNews 评论区](https://news.ycombinator.com/item?id=12171547)的讨论或多或少地单方面同意，像这样的大多数系统都有其明显的缺陷，但与在多个网站上使用几个常用的重复使用的密码相比，由软件生成和管理安全密码的总体好处仍然值得冒险。

人们可以通过使用 KeePass 这样的软件获得更安全的密钥管理器，但是它缺少基于远程的服务的一些便利因素，并且依赖于用户充分保护他们的密钥文件。

然而，尽管它们很可怕，但在负责任的披露之后公开讨论这样的黑客行为是好的，因为它们迫使像 Lastpass 这样的公司，他们有一些非常大的客户，更加认真地对待他们的代码审查和透明度。