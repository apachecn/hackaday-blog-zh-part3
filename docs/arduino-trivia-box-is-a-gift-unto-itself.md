# Arduino Trivia Box 是送给自己的礼物

> 原文：<https://hackaday.com/2017/12/29/arduino-trivia-box-is-a-gift-unto-itself/>

在互联网上给陌生人留下深刻印象会激发出我们最好的一面。老实说，否则我们不可能经营这个网站。这种现象的一个完美例子是一年一度的 Reddit 秘密圣诞老人，用户被要求为他们从未见过的人提供贴心的礼物。

为了参加这一年度创意展示，[哈里森·佩斯]想做一些展示他不断提高的电子技能的事情，同时也为接受者提供一些娱乐。因此，他想出了一个盒子，通过成功完成一个围绕他们的兴趣定制的内置琐事游戏来解锁。如果这就是他对待陌生人的方式，我们迫不及待地想看看他为他的朋友做了什么。

[![](img/129cf56905fa725de5e15d6a88d82142.png)](https://hackaday.com/wp-content/uploads/2017/12/giftbox_detail.jpg)

Hardware packed into the lid so the box itself remains empty.

这个令人眼花缭乱的礼品盒下隐藏着相当多的硬件。[盒子的主要功能由 Arduino Nano](https://github.com/thehaxxa/Reddit-Secret-Santa-Trivia-Game) 处理；它运行琐事游戏，并通过 16×2 LCD、三个按钮和一个蜂鸣器提供用户交互。一旦琐事游戏完成，一个伺服系统被用来打开盒子，并允许收件人获得实物礼物。

但这并不是这个盒子藏在里面的唯一诡计。一旦主要的琐事游戏完成，一个 ESP8266 开始行动，并公布一个用户可以连接的接入点。这开始了第二个层次的挑战和礼物，其中包括一个密码破解挑战和赠送的软件许可证。

然而，这个项目并不是一帆风顺的。[Harrison]承认他的技能仍在发展，在这个项目中他学到了一些经验教训，将来也不会忘记。当他将 5V Arduino 直接连接到 3.3V ESP8266 时，一些神奇的烟雾设法逃脱了，但至少这是一个相当便宜的错误，他手头上有备件，以完成项目。

这个项目[让人想起逆向地理藏宝箱](https://hackaday.com/2012/12/19/reverse-geocache-based-on-stm32-and-gps-wristwatch/)，[只有在移动到某个位置](https://hackaday.com/2012/01/20/a-talking-reverse-geocache-puzzle-box/)时才会打开，但琐事方面使它变得完美，即使对于我们这些[不想穿上裤子只是为了收到我们的互联网礼物](https://hackaday.com/2017/05/03/hack-your-hike-with-this-arduino-puzzle-geocache/)的人来说。

 [https://www.youtube.com/embed/Wn2nhj5GtTU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wn2nhj5GtTU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

