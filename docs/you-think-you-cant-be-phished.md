# 你认为你不会被钓鱼吗？

> 原文：<https://hackaday.com/2017/04/19/you-think-you-cant-be-phished/>

好吧，再想想。至少如果你用的是 Chrome 或者 Firefox。不相信我们？那么，看看苹果的新网站，在 https://www.apple.com。注意到什么了吗？如果你没有使用受影响的浏览器，你只是在打开网页后看到一个奇怪的 URL，否则它是相当合法的。该页面展示了浏览器如何解释并向用户显示 URL 的一种 Unicode 漏洞。请注意有效的 HTTPS。当然域名不是来自苹果，其实是域名:“*[https://www . xn-80ak6aa92e.com/](https://www.xn--80ak6aa92e.com/)*”。如果打开页面，可以通过右键单击并选择 view-source 来查看实际的 URL。

这是怎么回事？这种类型的网络钓鱼攻击被称为 [IDN 同形异义词攻击](https://en.wikipedia.org/wiki/IDN_homograph_attack)，它依赖于浏览器将 URL 中的“xn -”前缀解释为 ASCII 兼容的编码前缀。它被称为 Punycode，是一种仅使用互联网主机名中使用的 ASCII 字符来表示 Unicode 的方法。想象一种域的 Base64。这允许注册带有国际字符的域名，例如，域名“xn - s7y.co”相当于“短。正如【郑旭东】[在他的博客中解释的那样。](https://www.xudongz.com/blog/2017/idn-phishing/)

不同的字母有不同的符号在这种攻击中起作用。以西里尔字母为例，它包含 11 个小写字母，与拉丁语字母相同或几乎相同。攻击者用一个字母替换其对应字母的这类攻击广为人知，通常可以通过浏览器缓解:

> 在 Chrome 和 Firefox 中，如果域标签包含多种不同语言的字符，Unicode 格式将被隐藏。可以注册“xn - pple-43d.com”等域名，相当于“аpple.com”。乍一看可能不太明显，但是“аpple.com”使用的是西里尔字母“а”(U+0430)，而不是 ASCII 的“a”(U+0041)。如上所述的“аpple.com”域名将以其 Punycode 形式显示为“xn - pple-43d.com ”,以避免与真正的“apple.com”混淆。

到目前为止，浏览器过滤了这些类型的对应字符替换。但是有一个问题。当 URL 中的所有字符使用相同的字母表时，缓解似乎会失败。域“аррlе。com”如之前显示的网站中，注册为“xn - 80ak6aa92e.com”，通过仅使用西里尔字符来绕过过滤器。我们可以理解为什么一个开发者会选择这种行为，尽管如此，正如所展示的那样，这也带来了一个问题。

这影响了 Chrome 浏览器的当前版本 57.0.2987 和 Firefox 的当前版本 52.0.2。这不会影响 Internet Explorer 或 Safari 浏览器。如果你使用的是 Firefox，你可以通过改变**网络来关闭 **about:config** 中的 Punycode 翻译。IDN_show_punycode** 对**真**。如果你使用的是 Chrome，你必须等待更新。或者在启用 HTTPS 的网站中手动检查 HTTPS 证书。

难道你不想注册一个域名去钓鱼吗？

[感谢 chrisatomix]