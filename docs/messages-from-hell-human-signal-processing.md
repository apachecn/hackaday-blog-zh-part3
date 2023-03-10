# 来自地狱的信息:人类信号处理

> 原文：<https://hackaday.com/2015/12/30/messages-from-hell-human-signal-processing/>

尽管有这个标题，这篇文章没有宗教内容。这个地狱就是德国发明家[【鲁道夫地狱】](https://en.wikipedia.org/wiki/Rudolf_Hell)。虽然他的职业生涯令人印象深刻，但大多数人记住他的是 hell schreiber——当我试图说明工程优雅时，我经常提到这个设备。地狱男爵是什么？又为什么优雅？

[![](img/4e15cfdcbc7328ffbdb02d3743480d89.png)](https://hackaday.com/wp-content/uploads/2015/12/541px-hellschreiber-machine-at-bletchley-park-e1451059381361.jpg) 第一个问题很容易回答:Hellschreiber 几乎就像一台电传打字机。它通过无线电发送打印信息，但它的工作方式不同于传统的电传打字机。这就是优雅发挥作用的地方。不过，要理解这一点，你需要一些背景知识。

## 巨型大脑和色情

你不像过去那样经常听到它，但是曾经有一段时间人们称计算机为“电子大脑”在 20 世纪 70 年代，美国无线电公司有一个招聘广告说(如果我没记错):“最好的电子大脑是人类。”这句口号给我留下了深刻的印象，我发现它在很多情况下都是正确的。

不用看多远就能看到例子。电话在语音识别方面已经变得非常好，但是小孩子至少也一样好。例如，电脑可以写小说，但是人类写得更好。即使在计算机比我们做得更好的地方，比如国际象棋，也需要一台非常大的计算机。

[![Racknitz_-_The_Turk_3](img/3bab3d01163482383fafd0e8b21bf539.png)](https://hackaday.com/wp-content/uploads/2015/12/racknitz_-_the_turk_3.jpg) 当然，我们的电脑在一些我们不擅长做的事情上表现出色。这就是为什么，对我来说，最优雅的系统使用计算机的力量以及人脑的能力。最奇怪的例子之一是亚马逊的土耳其机器人服务。机械土耳其人(见左图)是 18 世纪一个著名的骗子，看起来像是一个下棋的机器人。它实际上是一个下棋的人操纵的木偶。

那一点也不优雅。然而，亚马逊的服务允许公司从人们那里获得人工服务，以换取小额付款。例如，假设你有一个照片分享网站，你想过滤掉色情图片。正如美国最高法院大法官斯图尔特所说:

> 今天我不会试图进一步定义… [“核心色情”]…但是当我看到它的时候我就知道它…

很难(或者可能不可能)编写一个计算机算法来正确地将图片分类为色情或非色情，而没有假阳性或假阴性。然而，几乎任何人都可以看着一张照片，按下“是”或“否”按钮，并且几乎总是正确的。这种事你可以外包给土耳其服务公司。计算机擅长传输和存储图像。人类擅长对它们进行分类。

## 所以地狱男爵是黄片？

不，Hellschreiber 不是色情(除非你用它传输“50 度灰”的文本，我想)。然而，这是对计算机/人类共生关系的一种优雅的运用。想想传统的电传打字机。五位或八位代码调制无线电信号(通常通过频移键控)。接收器注意到频率偏移并重构代码以确定消息是什么。

如果发射机和接收机之间的链接是一条安静的线，那就太好了。当连接是通过嘈杂的无线电时，那就不同了。今天，我们可以使用数字信号处理获得比以往更好的结果。我们可以放入复杂的前向纠错码，我们可以使用更强大的调制。但是这需要更多的硬件，这在地狱时代是没有的。如果一个静态的崩溃或衰落带走了一点，结果是一个混乱的信息。

人类非常擅长恢复信息。如果我写道:

> ```
> The ouick brown fox jumps over the l!zy red do8.
> ```

[![smart](img/468b1d66f5a88833685ccbe7ed81fec3.png)](https://hackaday.com/wp-content/uploads/2015/12/smart.jpg) 你大概能算出来。你已经看到了社交媒体迷因(左边),其中一条信息将字母混在一起，你仍然可以阅读它。但是在这两种情况下，这些消息仍然与原始消息相似(并且您大概知道它们会说些什么)。如果你收到信息:

> ```
> Meet me at the ($sdfk82.
> ```

看着这条信息，你大概是想不通我的意思。有了地狱男爵，你有更好的机会。为什么？Hellschreiber 就像是电传打字机和传真机的混合体。该设备发送的是字母的图片，而不是代码。当你意识到鲁道夫·海尔有电视背景时，这并不奇怪。你的大脑可以更容易地解读一张图片，而不是一个被噪音随机改变的代码。

实际上，机器会发送两张文本图像来帮助识别。噪音或相位差可能会使它有点难以阅读，但它必须非常糟糕，因为你的耳朵之间的湿件无法理解它。你可以在下面看到一个例子:

[![Feldhell](img/b7fc9038dc8f539c6c99fc952a27417b.png)](https://hackaday.com/wp-content/uploads/2015/12/feldhell.jpg)

这台机器用一个 7×7 的格子来构成字母。字符只发送一次，但打印两次。正如你所看到的，有时(由于时间误差)两条线都是可见的。其他时候，一行在中间清晰可辨，另一行在顶部和底部被截断。

## 现代地狱

Hams 仍然使用 Hellschreiber 作为通信工具。今天当然是机械机器没了，你用的是带声卡的软件。使用软件允许字符集的广泛变化，甚至灰度作为增强。你可以在下面的视频中看到一些使用 Hellschreiber 的 qso(联系人的 ham-speak)的例子。

当然，使用前向纠错和其他复杂方法的数字模式可以利用计算机的能力(通常)确保无错误传输。但 Hell 的发明是一个很好的例子，说明了为什么 RCA 说最好的电子大脑仍然是人类。

作为设计师，我们经常喜欢我们设计的机器部件。然而，一个好的系统也许能够将人类的智能与机器融合，并超越两者。

 [https://www.youtube.com/embed/Bf7lAdOvRi0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Bf7lAdOvRi0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

