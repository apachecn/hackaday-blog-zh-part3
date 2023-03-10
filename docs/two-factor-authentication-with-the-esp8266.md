# 使用 ESP8266 进行双因素认证

> 原文：<https://hackaday.com/2018/01/04/two-factor-authentication-with-the-esp8266/>

Google Authenticator 是一个特别受欢迎的智能手机应用程序，它可以通过生成基于时间的一次性密码(称为 TOTP)来用作许多双因素身份验证(2FA)系统的令牌。使用 Google Authenticator，您的用户名和密码以及应用程序生成的一次性代码的组合允许您以一种攻击者难以复制的方式安全地验证自己。

这听起来很棒，但是如果你没有智能手机呢？这就是[Lady Ada]最近发现自己处于的情况，她没有走捷径，而是购买一个与 Google Authenticator 兼容的硬件 2FA 令牌，[她决定自己基于 ESP8266](https://learn.adafruit.com/circuitpython-totp-otp-2fa-authy-authenticator-friend/introduction) 构建一个。她的网站上记录了硬件和源代码，任何感兴趣的人都可以使用开源 Google Authenticator 硬件令牌。

[![](img/c93d29020a57995dacd66c1ce40fd0f5.png)](https://hackaday.com/wp-content/uploads/2018/01/ada2fa_detail1-e1514918105791.png)

Generated codes can also be viewed via serial.

对于硬件，您需要的只是 ESP8266 和一个显示器。当然，如果你想创造一个相同的设备，你可以购买这两个设备，但这个概念将在你可能已经在零件箱中得到的通用硬件上同样工作。软件方面，代码是用 CircuitPython 编写的，[是 MicroPython](https://hackaday.com/2016/07/21/micropython-on-the-esp8266-kicking-the-tires/) 的衍生物，旨在使微控制器开发更容易。如果你以前没有尝试过 MicroPython，就拿一个 ESP 来试试吧。

从概念上讲，TOTP 相对简单。你只需要知道现在是什么时间，然后运行一个 SHA1 散列。时间部分非常简单，因为 ESP8266 可以连接到网络并从 NTP 获取当前时间。一旦您向 Python 代码提供了从 Google Authenticator 应用程序中提取的“秘密”, Python 代码就会处理 TOTP 的计算。这里值得注意的是，这意味着你的 2FA 秘密将以明文形式保存在 ESP8266 的闪存上，所以尽量不要用它来保护任何核发射系统或任何东西，好吗？话说回来，如果你丢失了它，双因素的好处是你可以使这个秘密无效并生成一个新的。

除了[之前为谷歌认证器开发](https://hackaday.com/2013/09/14/using-google-authenticator-with-an-arduino/)硬件令牌[的努力之外，如果你想了解更多关于这个概念的信息，我们在 Hackaday 之前已经讨论过 2FA 应用](https://hackaday.com/2015/07/20/hackaday-prize-entry-two-factor-authentication-key/)的来龙去脉。