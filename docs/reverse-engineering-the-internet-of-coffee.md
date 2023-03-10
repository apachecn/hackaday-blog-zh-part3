# 咖啡互联网的逆向工程

> 原文：<https://hackaday.com/2016/10/11/reverse-engineering-the-internet-of-coffee/>

多年前，当第一批记者发现物联网的概念并努力使其为大众所理解时，物联网的公开承诺是，你的厨房电器将与互联网相连，不知何故这会让我们的生活变得更好。我们被告知，冰箱会有屏幕，当供应不足时会神奇地订购更多的熏肉。

大约十年后，一些冰箱有了屏幕，但物联网应用的真正繁荣并不是在这种消费者可见的应用中。你的大多数电器仍然像 20 年前一样不受连接的影响，幸运的是，那个只会烤面包的红矮星会说话的烤面包机仍然在小说中。

不过，市场上并非没有物联网厨房电器。一个是 *Smarter Coffee* 咖啡机，一个联网的咖啡机，由一个应用程序控制。西蒙·玛格丽特里(Simone Margaritelli)买了一个，虽然他喜欢咖啡，但他真的不喜欢它没有控制台应用程序。[因此，他着手创建一个](https://www.evilsocket.net/2016/10/09/IoCOFFEE-Reversing-the-Smarter-Coffee-IoT-machine-protocol-to-make-coffee-using-terminal/)，首先通过反汇编其应用程序的安卓版本来逆向工程其协议。

遗憾的是，他发现的并不是 RFC 2324 的实现，而是使用一个非常简单的字节串来发布带有参数的命令，比如咖啡浓度。没有安全措施，他甚至可以触发固件升级。该应用程序需要注册和登录，尽管这似乎只是用于收集统计数据。因此，他的[咖啡](https://github.com/evilsocket/coffee)应用程序可以从他的终端命令机器的所有功能，他可以享受饮料，而不用伸手去拿应用程序。

从表面上看，你可能认为这台机器缺乏安全性可能无关紧要，因为它是在防火墙后面的私有网络上。但它代表了物联网设备完全忽视安全性的令人担忧的趋势的又一个例子。如果有人能接触到它，这台机器就是一本打开的书，恶作剧的可能性远远超过仅仅用一百杯多比欧浓缩咖啡捉弄它的主人。我们最近看到了第一次广泛宣传的使用物联网设备的 DDoS 攻击，是时候制造商开始认真对待这一威胁了。

如果你对咖啡黑客的前景感兴趣，[看看我们之前的报道](http://hackaday.com/2016/08/13/hacklet-120-coffee-hacks/)。

[通过[/r/家庭自动化](https://www.reddit.com/r/homeautomation/comments/56n9h8/reversing_the_smarter_coffee_iot_machine_protocol/)