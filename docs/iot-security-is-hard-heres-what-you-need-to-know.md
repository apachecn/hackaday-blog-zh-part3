# 物联网安全很难:以下是你需要知道的

> 原文：<https://hackaday.com/2017/04/21/iot-security-is-hard-heres-what-you-need-to-know/>

连接到互联网的任何东西的安全性都很重要。把这些设备想象成入口。它们要么允许访问服务，要么为其他人提供服务。门口需要安全——如果你住在一个繁忙城市的坏地段，你不会不锁门的，对吗？每一个互联网连接都是繁忙城市中不好的部分。问题是，构建连接到互联网的硬件是这些天的新热点。因此，让我们来了解一下您需要知道的基础知识，以便开始考虑项目的安全性。

如果你曾经运行过一个服务器并检查过你的日志，你可能会注意到有大量的自动流量试图持续访问你的服务器。网络上不安全的设备不仅会危及自身安全，还会给所有其他联网设备带来风险。

保护设备最简单的方法就是关机，但是假设你想开机。你可以做很多事情来保护你的物联网设备。开始时这可能看起来令人生畏，但是当你开始变得更有安全意识时，事情就像拼图一样开始组合起来，这就变得容易多了。

## 有哪些问题，你如何解决？

### 密码和密码安全

在我们开始之前，请记住更改您使用的每个软件包和设备的默认密码。对于任何连接的设备，这是您应该做的第一件事。Web 安全取决于两个目标:防止未经授权的人访问资源和确保授权的人访问他们需要的资源。如果你的设备向不同的人提供不同的信息，你需要有一些方法让你的设备区分不同的人，例如登录系统。这可以通过多种不同的方式来实现，例如将会话 ID 和[安全 cookie](http://blog.teamtreehouse.com/how-to-create-totally-secure-cookies)与密码结合使用。

非常重要的一点是，不要将密码或会话 ID 存储在 cookies 中，因为它们很容易被中间人攻击、恶意软件或实际访问最终用户计算机的人截获。密码应该总是经过哈希处理。这是一个单向过程，如果使用“加盐”处理得当，是无法逆转的。Salting 是使用一个字符串，所以当你散列密码时，salt 被用来创建一个唯一的散列。这阻止了攻击者使用彩虹表来破解你的密码，如果他们得到了你的数据库。几周前，Pedro Umbelino 在他的 Hackaday 文章中详细介绍了密码安全性。

[密码散列的安全加盐](https://crackstation.net/hashing-security.htm)是这个数字时代的发展方向点击链接了解更多信息。密码很重要，最好是你不知道你的用户的密码，因为他们可能会在其他账户上使用。如果你只是加密它们，那么你有办法解密它们，因为加密是一个双向的加密/解密过程。这就是我们哈希不加密的原因。

### 具有已知漏洞的旧软件

![](img/466d33c4ffdd089d12a8b29c0ea66b92.png)

ATMs are notorious for lagging behind on software updates. This makes them [easy targets](https://www.theregister.co.uk/2016/04/26/atm_hacking_all_too_easy/).

这是显而易见的，但很值得一说。避免使用有已知漏洞的旧软件，不要使用旧版本的软件。软件更新有正当理由。使用最新版本，即使变更日志没有提到具体的安全补丁。

有一些网站记录了[最常见的漏洞](https://cve.mitre.org/)，这对于你打算使用的软件包来说是值得一试的。您可能认为列出所有已知的漏洞是在帮助坏人，但这些实际上是好人。是的，它确实可以帮助潜在攻击者找到攻击旧的 web 脚本或软件的方法，但是如果您使用可信供应商的最新版本，他们将有希望修复他们产品以前出现的任何问题。列出漏洞给了公司一个理由来获得更新，并阻止攻击者捕食有缺陷的软件，因为你的软件供应商是懒惰的。这也有助于开发人员避开最坏的罪犯。

### 如果不需要，为什么要留着？

让我们假设你的设备正在运行某种形式的 Linux。有许多协议可用于与设备通信。例如，您可能有中小型企业，SSH，远程登录，FTP，VNC 等。但是你需要决定哪些协议是你需要的，哪些是你不需要的。如果你不使用一个协议，为什么首先要启用它呢？

这些就像是你设备的入口，你的入口越少，计算机“黑客”获得的攻击途径就越少。这确实是常识，但经常被忽视。另一个好建议是[禁用 SSH 的 root 登录](http://www.tecmint.com/disable-or-enable-ssh-root-login-and-limit-ssh-access-in-linux/)并创建另一个帐户来使用。您的 root 帐户最有可能被暴力破解。如果你需要远程登录使用至少 8 位数的密码，并使其随机和奇怪的字符，大写字母，数字等。如果你使用一个单词，也许结尾是 123，黑客用字典[进行暴力攻击](http://hackaday.com/2013/01/21/brute-force-finds-the-lost-password-for-an-electronic-safe/)几乎需要几分钟。

### 泄露太多信息

暴露可能帮助攻击者形成更复杂攻击的信息是一大禁忌。您的物联网服务器可能会提供比您想象的更多的信息，甚至是您认为不重要的信息。

例如，自写网站可能直接链接到服务器上的文件，而不是隐藏其实际位置。应该避免这种情况。你有一个“网络目录”是有原因的；您的设备软件希望您的文件位于此位置，并且设置了权限以防止超出此目录。不要打开后端(非 HTTP 部分),因为这可能会导致攻击者通过 web 脚本中的一个简单错误获得权限，该脚本应该是您设备的安全部分。

不要太担心这个，因为这是一个很小的问题。你仍然需要使用你的网络目录，但你也可以隐藏网址的使用。使用 Apache HTTP 服务器访问。如果您使用另一个 HTTP 服务器，它将有一个类似的配置系统。要了解更多信息，请在网上搜索“您的 http-server url 重写名称”。

您不希望任何潜在攻击者掌握的信息超过您的服务器运行所需的最低信息。泄露信息可能会帮助攻击者了解您的文件结构以及您在 HTTP 层下运行的内容。大多数攻击都是自动化的，旨在让您的服务器停机，因为它们注意到您使用了特定的软件。让发现变得困难有助于对抗这种自动化。

在你的网站目录中，你也要确保你的文件不在目录索引中，在每个目录中放一个简单的 index.html 文件会阻止窥探。如果你的服务器有一个数据库，把它放在另一个设备上(最佳实践)，或者如果不可能，确保把它放在防火墙后面。也不要把数据库放在你的“web”目录中。想了解更多关于[锁定你的服务器](https://null-byte.wonderhowto.com/news/lock-down-your-web-server-10-easy-steps-stop-hackers-from-attacking-0133721/)的信息，请点击链接。

### 跨站点脚本

![](img/d84ecf6cb42bf0a0641eeb5e4971f89c.png)

Samy Kamkar, creator of the Samy worm; photo via [The Amp Hour interview from 2016](http://theamphour.com/308-an-interview-with-samy-kamkar/)

XSS 或跨站脚本攻击是更常见的攻击媒介之一。这是攻击者利用脚本的地方，例如这个页面底部的 Hackaday 评论部分。攻击者可能试图留下带有脚本标记的注释。如果成功，这将在评论中发布恶意代码，每当有人访问此页面时，该代码就会在用户的浏览器上运行。当然，Hackaday 不会受到这种类型的攻击，但这个例子适用于确实存在 XSS 漏洞的网站。威尔·斯韦特曼写了一个关于 XSS 的速成班，值得一看。

也许最著名的 XSS 攻击是萨米蠕虫病毒。Samy Kamkar 发现了 MySpace 的一个漏洞，该漏洞会导致每个查看他页面的人将他添加为好友，并在他们的个人资料页面上显示一条消息。它是自我传播的，所以任何浏览过带有该信息的网页的人都成为了传染新访客的载体。几乎一夜之间，MySpace 上的每个人都在关注萨米。从那以后，他成为了一名安全研究员，并且[成为了 Hackaday](http://hackaday.com/2016/12/19/samy-kamkar-illustrates-how-to-be-a-hardware-hacker/) 的好朋友。

当托管你自己的网络服务，提供提交表格来控制你的黑客一起物联网的事情，确保你考虑 XSS。解决这个问题的方法就是我们所说的净化数据。当然，您应该限制 web 表单包含的内容(删除“脚本”和其他 HTML 标签)。XSS 攻击非常普遍，物联网设备的 web 界面也会接受输入，现在是[去尽可能多地了解 XSS](https://excess-xss.com/) 的好时机。

### 物理访问攻击

物理访问也可能是一个问题。您可能将您的设备放在公共场所或容易接近的地方。你需要确保没有人过来推一个 [USB 黑仔](http://hackaday.com/2017/02/19/the-usb-killer-now-faster-better-more-anonymous/)或 USB 黑客工具，例如一个像键盘一样显示为 HID(人机界面设备)并开始从预先配置的脚本中发出命令的工具。如果你不需要 USB，让他们无法访问或通过软件关闭。如果你真的有安全意识，为什么不把它们从电路板上完全移除，或者把环氧树脂倒在上面？甚至 PS/2 端口也应该受到保护。你可能会看到这里出现了一种模式，一个好的安全哲学是，如果你不需要它，为什么要把它放在第一位。

### 使用久经考验的安全措施

默默无闻的安全感也不是一个好主意，总会有人比你更聪明或更幸运。尝试坚持尝试和测试的安全措施，不要因为你有一些奇怪的设备，市场规模可能在 100 人/公司以下，就认为你是安全的。没有什么是 100%防弹的，但如果你认为你的设备永远不会因为“原因”而受到攻击，那就再想想吧。重新评估你的位置，解决你的安全问题。

如果你遵循这个建议，只要你记得更改默认密码，你应该是相当安全的，并且记住这不是一个确定的指南，你总是可以做一些其他的事情来保护你的设备。到目前为止，最大的问题是完全没有考虑到安全性——我们可以做得更好！

## 未来预防

物联网设备现在正被疯狂追逐。你需要保持警惕，确保你的设备不会受到像 [brickerbot](http://hackaday.com/2017/04/08/brickerbot-takes-down-your-iot-devices-permanently/) 这样的攻击，或者成为[最新物联网僵尸网络](http://hackaday.com/2016/10/20/hajime-yet-another-iot-botnet/)的一部分。将来会有更多类似的袭击发生。通过了解安全知识并锁定您的设备，抢占先机。如果你对网络安全很认真，开始阅读最新的趋势，因为每天都有新的漏洞被发现。如果你为别人制造设备，那么你必须成为这些技能的专家。如果你自己都不能这么说，那就请一些专业人士吧。你不想打官司，你不想失去客户的信任，你也不想构建威胁我们互联世界的硬件。