# 你应该阅读的圣经:poco || gtfo

> 原文：<https://hackaday.com/2017/08/14/bibles-you-should-read-poc-gtfo/>

牧师 LAPHROAIG 宣布将会折磨机器人之城的信徒们！任何人都不能幸免，宗教裁判所将立即开始！

在过去的几年里，Manul Laphroaig 牧师和他的朋友们出版了国际 PoC 杂志|| GTFO。这是提交给 GTFO PoC | |的 Tract Association 的一系列论文和成果，每一篇都展示了电子领域中一个有趣的成果、技术或软件玩具。想象一下，如果 *2600* 或者*多布博士的期刊*是专业的学术刊物。加入一些威士忌，你就有了 PoC || GTFO。

这是我们期待已久的事情。《国际杂志》 [PoC || GTFO 现在真正的](https://www.nostarch.com/gtfo) [~~书~~圣经](https://www.nostarch.com/gtfo)由无淀粉出版社出版。这种放纵的代价是什么？30 美元，或者如果你只想要电子书版本的话，还可以再便宜一点。枯树版 PoC 的吸引力包括人造革封面、镀金边缘，以及可以放入其他优秀零售商提供的圣经封面的能力。没有传言说会有一个以蔬菜为主的角色的儿童版。

 [![PoCHeaderFull](img/870b623e8fdefec36d12a4f1646a68ee.png "PoCHeaderFull")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/08/pocheaderfull.jpg?ssl=1)  [![poc2-wb2](img/9b3bde4433445963259f63da92c51ba1.png "poc2-wb2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/08/poc2-wb2.jpg?ssl=1)  [![PoC1](img/2b173111f14b271faacfe0781fc0d3e1.png "PoC1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2017/08/poc1.jpg?ssl=1) 

事实上，PoC || GTFO 是一个几乎三年一期的杂志，内容涉及逆向工程、计算机科学和其他随机电子计算魔法，论文(概念证明)由 Dan Kaminsky、Colin O'Flynn、Joe FitzPatrick、Micah Elisabeth Scott、Joe Grand 和其他黑客世界的英雄撰写。PoC || GTFO *将*本身呈现为什么？宗教小册子中的应用电子。舌头牢牢地种在脸颊这里，很牛逼。

![](img/df87d9413ec2b3c3dd6108812892f2ab.png)

### Laphroaig 牧师说的是什么？

需要一个在 GTFO 国际 PoC 杂志上发表的例子吗？第四版 (PDF)是一个很好的基准，包含了从高级逆向工程技术到基础化学的一切。

[![](img/1fc8e5851d1c9e6e53db0c761bf16191.png)](https://hackaday.com/wp-content/uploads/2017/08/bunsen.png)

Figure 4.8: The clamp stand holds the test-tube next to the SMD rework station

在 PoC 的第 4 版中，包含 Travis Goodspeed 的*回流解封装和芯片摄影介绍*。这就是你如何简单地通过*看着*微电子开始逆向工程，并且整个设置对于任何一个有通风良好的实验室并且知道如何在易贝寻找金相显微镜的人来说都是合理可行的。

回流拆封的过程相对简单，但需要一些危险的化学品。你当然需要一些硝酸和硫酸，但唯一需要的其他设备是试管、环形支架、廉价的 SMD 热风站、超声波清洗机，当然还有一些显微镜设备。

难道*这个*就可以轻松解封拍摄微电子？是的，但是你需要带来一些东西。你需要知道向水中添加酸，你需要小心观察你的回流，你可能会有很多乐趣将芯片的照片拼接成一张图像。这是可以做到的，不过，特拉维斯给你的概念证明。如果他不说，我们会有话跟他说。

### ![](img/cbf75f8fa8af59097b98a204adf0d039.png)

在 PoC || GTFO 和朋友的 Tract Association 的第四份出版物中，还有世界领先的电子鸡固件专家 Natalie Silvanovich 对电子鸡的利用。娜塔莉在第四版中的工作是她在第二版中讨论的探索的延续，第二版本身在某种程度上是对她在 29C3 的演讲[的重述。](https://media.ccc.de/v/29c3-5088-en-many_tamagotchis_were_harmed_in_the_making_of_this_presentation_h264)

![](img/b2e0ab27ecff060c42b29c717efd159e.png)

HEY KIDS! Can you reverse engineer shellcode from the picture?

娜塔莉因利用现代电子鸡而出名。自 1999 年以来，电子鸡的世界发生了很大的变化，新的型号具有 IR、RFID，但仍然是围绕 6502 核心构建的。6502 在玩具中非常受欢迎。

第四版中介绍的论文是通过电源故障转储电子鸡固件的概念证明。6502 是一个奇怪的怪兽，通过在一个非常特定的时间段内干扰输入功率，寄存器将被破坏(将程序计数器设置为零)，但 SRAM 将保持不变。使用 Arduino 来干扰电源，Natalie 能够一次转储 54 字节的电子鸡的完整固件。如果你曾经想了解电力故障，或者电子鸡尖叫的恐怖，这是一本必读的书。

国际 PoC 杂志|| GTFO 的每一篇论文都是工程学的杰作。这些是地球上真正最有能力的逆向工程师，在一个充满方言的奇怪的赛博朋克杂志中呈现，其中包括短语“楠塔基特雪橇”。这本杂志本身就是一件艺术品，我不能推荐它更多。如果你看到 Laphroaig 牧师，告诉他为我保存下一版的枯树版本。

[![](img/4aa058a629c2bfed8874442d6ee9de6a.png)](https://hackaday.com/wp-content/uploads/2017/08/poc3.jpg)

### 1 和 0 版本

在《死亡之树 PoC || GTFO》出版之前，获得纸质版的唯一途径是在黑客或安全会议上找到 Manul Laphroaig 牧师(Laphroaig 的真实身份似乎是一个公开的秘密，但我们用这个来制造喜剧效果)。副本已在 DerbyCon、ShmooCon 和 ToorCon 或 camp 分发。

或者，PoC || GTFO 可以从任何一个专门用一点服务器空间来托管几百兆 pdf 的人那里在线获得。事实上，鼓励从您自己的服务器分发 PoC。比特罗将以无情的侮辱焚烧图书馆，即使是宠物网站也不配。请镜像—不要只是链接！——PoC | | GTFO 各地的所有副本。”你可以在[alchemistowl.org](https://www.alchemistowl.org/pocorgtfo/)找到所有版本的 PoC，由 [Great Scott Gadgets](https://greatscottgadgets.com/) 和其他优秀的网络服务器托管。

虽然抓住一个死树的 PoC 副本，牧师 Laphroaig 在 Kinkos 印刷满足了每个人对怪异的技术杂志和宗教书籍出版物的需求，但有理由玩 pdf:大多数版本的 PoC 都是多语言文件。PoC 卷 4 是一个 TrueCrypt 卷。第 7 卷是一个 PDF，一个 Zip 文件，一个 BPG(更好的便携式图形)和一个 HTML 文件都在一个。这可能是数字媒体的局限性，通过十六进制编辑和隐写术来实现。

但不可否认的是，以圣经形式印刷 PoC 非常适合该出版物。这是一本你想永远放在咖啡桌上的杂志。

[![](img/e8a4dca85cfb5f407a3b0b28cba9b84c.png)](https://hackaday.com/wp-content/uploads/2017/08/stunthacking.jpg)

### 那么，你真的应该买这个吗？

就像我之前说的，这是一本要回顾的奇怪的书。所有的内容都已经可以在网上获得，即使没有淀粉出版社提供免费电子书(PDF、epub 和。mobi)对于每一个印刷版本，No Starch 提供的 PDF 版本都不包含*一个怪异的操作系统*隐藏到 PDF 中。出版社的官方 PDF 版本只有 17 兆；仅官方 0x15 一期就将近 50 兆。

然而，这是正在迅速成为有史以来最伟大的硬件、黑客和逆向工程出版物之一的物理表现。PoC || GTFO 值得在工程文学中占有一席之地；它可能已经和出版物不相上下了，即使它在组织和文化上不如 T2。

那么，你该不该买 Laphroaig 牧师的好话呢？当然，如果你喜欢死树的话。至少有一对夫妇已经把 PoC || GTFO 当做圣经结婚了。它放在架子上看起来很棒，如果你在公共交通上阅读 PoC || GTFO，人们会远离你。