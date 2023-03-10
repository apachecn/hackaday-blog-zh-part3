# 构建电子鸡的无限矩阵

> 原文：<https://hackaday.com/2015/11/24/building-the-infinite-matrix-of-tamagotchis/>

电子鸡是一种电子宠物，生活在一个钥匙链大小的硬件中，并通过它得到照顾。90 年代中期的玩具生活在流行文化中，但现在它远远超越了流行文化。一个无限的 Tamagachi 网络已经被创造出来，它使用一些惊人的技巧来喂养、社交和监控现在被称为[Tamagachi 奇点](https://www.youtube.com/watch?v=3_-e_cJ1-Gs)的野兽。

上周末，在[黑客日超级大会](https://hackaday.io/superconference/)上，我们有幸得到了【耶鲁安·多姆伯格】(又名 [Sprite_tm](http://spritesmods.com/) )的演讲。[Sprite]是我们的最爱，多年来，他的黑客信誉包括从逆向工程硬盘控制器芯片到在键盘上安装视频游戏*的一切。*

[Sprite]也是一个建筑师，像所有的建筑师一样，他只想要对他创造的系统最好的东西。在这种情况下，它是一个电子鸡矩阵。[Sprite]创造了一群电子鸡，它们能够在各自独立的世界里相互交流。这个矩阵最好的部分是什么？在论述中没有违反热力学定律的暗示。

[![xkcd.com/1546](img/ba7fbf88f00808cbb73d22a0325ecc7e.png)](https://hackaday.com/wp-content/uploads/2015/11/tamagotchi_hive.png)

[xkcd.com/1546](https://xkcd.com/1546/)

像所有优秀的黑客一样，电子鸡矩阵不是凭空产生的。几年前，在 29C3，娜塔莉·席尔瓦诺维奇[抛弃了当前一代电子鸡](http://hackaday.com/2013/05/24/tamagotchi-rom-dump-and-reverse-engineering/)中的 ROM。这是逆向工程的一个令人难以置信的壮举，它允许任何人使用基于 6502 的微控制器来控制这些数字宠物的全部功能

在[Sprite]发现如何读取和运行电子鸡中的代码之后，迈向包含所有电子鸡的蛋形豆荚世界的下一个明显步骤是虚拟电子鸡。[Sprite]使用了一个硬编码的状态机，它负责便便、冲水、训练、喂食和睡觉时关灯。

由于一只电子鸡被描述为一台国家机器，建立另一只很简单。这就是事情变得有趣的地方。电子鸡不是独自生活的；他们有一个红外 LED 和接收器，允许他们相互交流，吃饭，玩耍，结婚，生孩子。模仿一只电子鸡是一回事，但控制多只电子鸡完全是另一回事；需要某种协议来培育电子鸡，让它们快乐、营养充足。

 [https://www.youtube.com/embed/3_-e_cJ1-Gs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3_-e_cJ1-Gs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![The Tamagotchi State Machine](img/560a13ffd03d9ddc240029ae718233a6.png)](https://hackaday.com/wp-content/uploads/2015/11/state-machine.png)

The Tamagotchi State Machine

进入电子服务器(Tamaserver),这是运行在服务器上的一小段代码，记录着十几只电子鸡。在这个服务器上，一小部分电子鸡一生都没有意识到它们只是一台巨大计算机的一部分。在这里，电子鸡生存、进食、恋爱和死亡，都没有违反《T2 黑客帝国》三部曲中提出的热力学定律。

到目前为止，在一个多月的时间里，Tamaserver 已经成为 13 只电子鸡的家，在没有任何外部干预的情况下，成为七代电子宠物的主人。最近 12 只雌性和 1 只雄性的事情变得不确定，迫使电子鸡矩阵稍微修改。[Sprite]只重置过一次 Tamaserver，但他仍然变得非常有效率。

### 最初的电子鸡硬件被重新设计

在服务器上运行一个电子鸡世界是一项值得追求的目标，但由于[Sprite]是在一次硬件会议上做这个演讲的，这需要硬件来展示。旧德国防空洞/服务器农场中的矩阵根本不行。因此，[Sprite]创造了 Tamanode，一个为蜂巢中的每个细胞提供 WiFi 功能的浏览器。

[![[Sprite]'s highly modified WiFi-enabled Tamagotchi](img/4811a4835309d8f83f4ff15c9110c81f.png)](https://hackaday.com/wp-content/uploads/2015/11/tamaviewer_internals.jpg) 

【雪碧】

【娜塔莉·席尔瓦诺维奇】几年前就已经完成了[在电子鸡上运行任意代码](http://www.kwartzlab.ca/2013/05/code-execution-tamagotchi/)的所有工作，通过包含 EEPROM 的小蛋蛋插件。这是通过向 LCD 显示器写入代码，然后将 CPU 跳转到无效地址来实现的。当 CPU 遇到无效地址时，它会跳到屏幕上的一个地址空间。这是一个非常聪明的方法，但是如果你没有硬件来做一些很酷的事情，它就没有什么用了。

[Sprite]在他的鸡蛋上做了一点手术，添加了一个 ESP8266 WiFi 模块和一个 EEPROM，其中包含连接到 WiFi 网络、访问他的蜂巢和滚动浏览每个居民的所有代码。这是颠覆性的电子鸡计算、数字宠物互联网和云计算电子鸡服务。

从各方面来看，这都是一项了不起的成就。[Sprite]在周六晚上发表了这篇演讲，就在 2015 年[黑客日奖](http://hackaday.com/2015/11/19/the-story-of-the-2015-hackaday-prize/)发表之前。当你在周日遇到他们时，这是他们最想谈论的事情。我们希望这段录音能对互联网上更广泛的受众产生同样的影响。他不是昙花一现的人物。[我们虔诚地查看【雪碧的】网站](http://spritesmods.com/)，寻找他发布的每个项目带来的兴奋感。

**更新:**【Sprite _ TM】在自己的网站上公布了[被黑](http://spritesmods.com/?art=tamasingularity)的全部细节。看看吧！