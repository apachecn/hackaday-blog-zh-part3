# 夺旗挑战是最好的礼物

> 原文：<https://hackaday.com/2018/01/18/capture-the-flag-challenge-is-your-perfect-gift/>

没有什么比未知地形上的逆向工程挑战更能代表友谊了。当[Rikaard]今年早些时候 25 岁时，他的朋友[Veydh]为他在 ESP8266 上组织了一次“夺旗”挑战。作为一个没有电子背景的软件人员，[Rikaard]不知道他面对的是什么，[但他渴望找到并记录他的旅程](http://rikaard.io/post/2018-bday-reversing/)。

离开时没有指导或指示，[Rikaard]继续了解更多关于 ESP8266 的信息，目标是转储其 flash 内容，希望从中找到一些线索。发现开发板正在运行 NodeMCU 并包含一些编译好的 Lua 文件，他踏入了另一个未知的领域，这使他陷入了 Lua 字节码的陷阱。在描述了他对他使用的反编译器的 ESP 的 eLua 实现的调整后，他对捕捉旗帜的追求开始了。

虽然这次[不是【Rikaard】的第一次逆向工程挑战](http://rikaard.io/post/)，但这是他第一次在舒适区之外的完全未知的环境中——他表现出的耐力令人钦佩。当然，在一个[开发芯片](https://hackaday.com/2017/05/02/how-to-reverse-engineer-a-chip/)或[在稍微复杂一点的系统中计算晶体管](https://hackaday.com/2014/12/18/counting-transistors-in-the-playstation/)之前，还有很长的路要走。