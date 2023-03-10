# 谷歌的双重人工智能与人类的对话没有区别

> 原文：<https://hackaday.com/2018/05/10/googles-duplex-ai-has-conversation-indistinguishable-from-humans/>

首先，谷歌逐渐改进其 WaveNet 文本到语音神经网络，使其听起来几乎完全像人类。然后他们推出了[智能回复](https://ai.googleblog.com/2017/05/efficient-smart-reply-now-for-gmail.html)，它会建议你回复邮件。因此，毫不奇怪，他们宣布了一项名为[双工](https://ai.googleblog.com/2018/05/duplex-ai-system-for-natural-conversation.html)的谷歌助手增强功能，可以为你进行电话交谈。

令人惊讶的是它的工作效率，正如你在下面听到的。第一个是双工电话预约发廊，第二个是预约餐厅。

<http://www.gstatic.com/b-g/DMS03IIQXU3TY2FD6DLPLOMBBBJ2CH188143148.mp3?_=1>

[http://www.gstatic.com/b-g/DMS03IIQXU3TY2FD6DLPLOMBBBJ2CH188143148.mp3](http://www.gstatic.com/b-g/DMS03IIQXU3TY2FD6DLPLOMBBBJ2CH188143148.mp3)

<http://www.gstatic.com/b-g/KOK4HAMTAPH5Z96154F6GKUM74A3Z1576269077.mp3?_=2>

[http://www.gstatic.com/b-g/KOK4HAMTAPH5Z96154F6GKUM74A3Z1576269077.mp3](http://www.gstatic.com/b-g/KOK4HAMTAPH5Z96154F6GKUM74A3Z1576269077.mp3)

请注意，在电话中与计算机交谈时，这将颠倒角色。电脑是调用业务的客户，人是在业务端。计算机的目标是预约理发或在餐馆预定座位。计算机必须知道如何在人类不知道他们在与计算机对话的情况下与人类进行对话。这是为了与那些没有在线预订系统，而是使用人工接线员打电话的企业进行沟通。

由于不知道他们是在与计算机对话，因此人类会像与另一个人一样说话，有所有的停顿，“嗯”和“啊”，语速，省略单词，甚至在句子中间改变上下文。一个短语还有多重含义的问题。“Ok for four”中的“四”可以指下午 4 点或四个人。

决定说什么的组件是一个在许多匿名电话上训练的递归神经网络(RNN)。输入是:音频、谷歌自动语音识别(ASR)软件的输出，以及上下文，如对话的历史和对话的参数(例如，预订餐馆的位置、多少人、何时)等等。

产生语音是使用谷歌的文本到语音技术、 [Wavenet](https://hackaday.com/2016/12/03/talking-neural-nets/) 和 Tacotron 完成的。插入“嗯”和“啊”以获得更自然的声音。时间也是考虑的因素。“喂？”获得即时响应。但当回答更复杂的问题时，它们会带来延迟，因为回答得太快听起来不自然。

尽管有一些限制。如果它认为自己无法完成任务，那么它会将对话交给人工操作员。此外，双工不能处理一般的对话。相反，多个实例在不同的域上被训练。所以这不是我们之前讨论过的奇点。但是，如果你厌倦了在工作中与计算机交谈，也许这将通过让计算机与企业交谈来提供一点回报。

更严肃地说，你会想知道和你说话的人实际上是不是一台电脑吗？也许谷歌应该以“嗨！这是谷歌助手打来的。”即使知道了这一点，你还想和一台计算机进行人类对话吗？即使知道它是人工的。这可以为代表通话的人节省时间，但被通话的人可能希望计算机更像计算机，说话更有效率。请在下面的评论中告诉我们你的想法。或者看看下面的谷歌 I/O’18 主题演讲视频，这一切都是在那里宣布的。

 [https://www.youtube.com/embed/ogfYd705cRs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2109&wmode=transparent](https://www.youtube.com/embed/ogfYd705cRs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2109&wmode=transparent)

