# hacklet 77——发推特的项目

> 原文：<https://hackaday.com/2015/09/25/hacklet-77-projects-that-tweet/>

自 2006 年推出以来，Twitter 已经成为吸引技术人员的磁石。也许是简单的界面，也许是 140 个字符的限制。不管是什么原因，你可以发现许多黑客、制造者和工程师在推特上谈论他们的日常活动。没过多久，人们就开始将 Twitter 整合到他们的项目中。Ladyada 的 [Tweet-a-watt](https://learn.adafruit.com/tweet-a-watt/) 就是一个很好的早期例子。本周的 Hacklet 是关于 Hackaday.io 上一些最好的推文项目的！

[![dogbark](img/5021c15ed9f20830bfbcd6b68d7ab323.png)](https://hackaday.io/project/7316) 我们从【亨利·康克林】和[我的狗](https://hackaday.io/project/7316)的推特账户开始。[Henry]的狗[Oliver]喜欢吠叫，找到解决方法成了他参加 Hackaday 奖的参赛作品。与其让西泽·米兰参与进来，[亨利]决定拥抱[奥利弗]的发声法，将它们送上云端。带有 USB 麦克风的 Raspberry Pi 使用一些定制的 Python 代码来检测吠叫和皱领。然后 Pi 使用 python-twitter 库将这些数据发送到 Twitter。Pi 通过 USB WiFi 加密狗连接到互联网。你可以在[【奥利弗】自己的推特页面](https://twitter.com/OliverBarkBark)上看到【亨利】的工作成果！

[![dectalker](img/9229c0037e68e10e5da9031fa21b9c24.png)](https://hackaday.io/project/1566) 接下来是【troy.forster】和 [tweetie-pi](https://hackaday.io/project/1566) 。[Troy]想要一个设备来阅读他的推文，而不是经常检查他的手机或电脑。一点 NodeJS 代码之后，tweetie-pi 就诞生了。一个连接到互联网的 Raspberry Pi 通过 Twitter 流 API 获取数据。当发现指向预先配置的用户名的推文时，数据被发送到一个 Emic 2 文本到语音模块。主位以我们在电影中熟悉和喜爱的经典对话式声音朗读。[Troy]甚至添加了正确处理用户名和转发的代码。

[![homeauto](img/8e08b08c20e03349ee47a65e81917d4a.png)](https://hackaday.io/project/2231) 【三叶草】通过用 Twitter 创建[家庭自动化系统加入了物联网，这是他 2014 年 Hackaday 奖的参赛作品。这个家庭自动化系统基于 Arduino Leonardo 和以太网屏蔽。[SirClover]推出了自己的定制 PCB 来处理继电器、Cds 电池和 2×16 字符 LCD。该系统可以通过一个简单的网络界面进行访问。这允许用户打开或关闭百叶窗，打开灯，所有这些伟大的智能家居的东西。每次执行命令时，家庭自动化系统都会向 Twitter 报告状态。](https://hackaday.io/project/2231)

[![das-cube](img/cff7315ef8a3bc68f3fb432e07cfcbf7.png)](https://hackaday.io/project/6593) 最后我们有【雅各布·安德烈】和[一个可跳舞的通知立方体](https://hackaday.io/project/6593)，这是【雅各布的】2015 年黑客日奖的参赛作品。立方体本身是一个半透明的盒子，里面装有一米长的发光二极管。准确地说是 148 个新像素和 12 个 3W 功率 led。所有这些 led 都由 Teensy 3.1 驱动，它是整个系统的主处理器。Teensy 从 MPU6040 IMU 读取位置数据。这使得它可以在盒子移动或“跳舞”时改变亮度和颜色。ESP8266 为立方体提供来自互联网的数据，特别是脸书和推特。每当立方体收到信息时，它就会亮起并闪烁。

如果你想看到更多的推文项目，请查看我们新的推文列表的[项目。我错过你的项目了吗？不要害羞，](https://hackaday.io/list/7823-projects-that-tweet)[在 Hackaday.io 上给我留言就行了](https://hackaday.io/adam)。这就是本周的 Hacklet，一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！