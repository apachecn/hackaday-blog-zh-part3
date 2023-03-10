# 做一个像谷歌的 Duplex AI 一样的自然语言手机机器人

> 原文：<https://hackaday.com/2018/06/21/make-a-natural-language-phone-bot-like-googles-duplex-ai/>

在看到谷歌的 Duplex 人工智能如何通过愚弄一位人类大师，让他以为是人类，从而能够在一家餐馆预定一张桌子之后，我想知道我们这些单纯的黑客是否有可能实现同样的壮举。如果没有谷歌的王牌人工智能程序员和神经网络训练硬件，你或我能做什么？让我们看看我们可以用什么方法来制造我们自己的自然语言机器人。正如你将看到的，这是完全可行的。

## 分解解决方案

设计解决方案的第一步是将它分解成更小的步骤。任何对话都包括两个人之间的来回，或者在我们的例子中是一个人和一块硅。

假设我们想创建一个可以通过电话为我们订购披萨的机器人。披萨店首先对我们说了些什么。然后，一些软件将该语音转换成文本或分解成其他有用的形式。更多的软件然后制定一个反应。最后，文本转语音软件或预先录制的声音片段通过手机扬声器回复比萨饼店。

解决方案的前半部分属于自然语言处理的范畴，其中至少有一部分涉及到将语音转换成软件容易理解的形式。

## 将语音转换为文本

虽然有很多开放的软件选项可以将文本转换为语音，但从语音到文本的转换却不多。它们通常也是库的形式，这对我们的使用很好。开放的例子是 CMU 狮身人面像，朱利叶斯和卡尔迪。

最近，Mozilla 一直在开发一个名为 DeepSpeech 的产品，它使用了 TensorFlow 和深度学习。到目前为止，我们已经看到它被使用过一次，当时[【迈克尔·谢尔登】用它将语音转换成文本](https://hackaday.com/2018/01/17/speech-recognition-for-linux-gets-a-little-closer/)，然后他将文本注入到 X 应用程序中。

## 理解课文

一旦你把演讲转换成文本，你会怎么做？

在我们的图表中，比萨饼店的人问我们“就这些吗？”。这句话可以有很多其他的表达方式，例如:“就这样吗？”，“就这些？”。

![Pizza ordering chatbot decision tree](img/96d7cf2602fa9c356a838407d7a630b8.png)

处理所有这些可能性的一种方法是通过将一堆 if-then-else 语句放在一起编写 formulate-a-response 代码，或者编写一个由一些表支持的解析器。如果预期对话是结构化的，那么您可以创建一个决策树，并让代码以此为指导。

AIML(人工智能标记语言)使这种方法变得更容易。AIML 由理查德·华莱士在 1995 年至 2002 年期间创建，此后一直是许多聊天机器人的基础，包括一个名为 A.L.I.C.E 的获奖机器人。自 2013 年以来，A.L.I.C.E .基金会一直在致力于 AIML 2.0 的规范。

使用 AIML，您可以用比萨饼店可能说的所有可能的事情来填充 XML 文件。使用“Hi *”之类的模式可以最小化它们的数量，但是 AIML 中的模式语言是有限的。它还允许您提供回应，并在出现特定主题时将对话限制在特定主题。在它的许多其他功能中，它有能力通过向文件中写入新奇的东西来学习。

从 AIML 开始，见 pandorabots.com 的文档。还有一个比较老的解释器叫 [ProgramAB](https://code.google.com/archive/p/program-ab/) 。

这个视频展示了一个开源的 InMoov 机器人在使用 AIML。

 [https://www.youtube.com/embed/S59JlEdu4bU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S59JlEdu4bU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 确定意图

我们解决方案中的大部分流程语音部分基本上都涉及到理解披萨店所说内容的意图，除非我们的代码是一大堆 if-then-else 语句或决策树结构，否则看起来可能不是这样。最终，当披萨店以无数种方式中的一种询问我们是否只点这一种时，我们希望将所有的可能性归结为一个简单的意图，“问 _ 就是 _ 那 _ 全部”。

或者，意图可能会附带额外的数据供我们使用。他们可能会说“20 分钟后就好。”或者“你可以 20 分钟后来取。”。在这种情况下，我们可以将意向标记为“give_order_ready_time ”,并将持续时间(20 分钟)存储为附加数据。

## 在线服务

免费的在线服务既可以进行语音识别，也可以确定任何数据的意图和捕获。脸书旗下的 Wit.ai 就是这样一家公司。另一个是 [DialogFlow](https://dialogflow.com/) ，前身是 Api.ai，现归谷歌所有。DialogFlow 确实对一些东西收费，但没有黑客需要的东西。IBM 的[沃森助手](https://console.bluemix.net/docs/services/conversation/index.html)也是免费的，但有一些限制。

虽然 Wit.ai 进行语音识别和意图确定，但 DialogFlow 和 Watson 实现了完整的决策树，允许您使用他们的用户界面来编写整个对话。

## 使用 Wit.ai 订购披萨

我决定试用 Wit.ai，下面是由此产生的对话，用一个虚构的 Johnny's pizza 订购一个 Pizza。披露:实际上没有打电话，但在下面有更多。有两种方法可以和比萨饼店交谈。第一次使用预先录制的讲话:

<https://hackaday.com/wp-content/uploads/2018/06/wit_pizza_ordering_phone_conversation.wav?_=1>

[https://hackaday.com/wp-content/uploads/2018/06/wit_pizza_ordering_phone_conversation.wav](https://hackaday.com/wp-content/uploads/2018/06/wit_pizza_ordering_phone_conversation.wav)

第二种方法使用 [Festival 文本到语音转换软件](https://elinux.org/RPi_Text_to_Speech_(Speech_Synthesis))来即时创建语音。

<https://hackaday.com/wp-content/uploads/2018/06/wit_pizza_ordering_phone_conv_w_festival.wav?_=2>

[https://hackaday.com/wp-content/uploads/2018/06/wit_pizza_ordering_phone_conv_w_festival.wav](https://hackaday.com/wp-content/uploads/2018/06/wit_pizza_ordering_phone_conv_w_festival.wav)

简而言之，我是这样做的。首先，我写了一个脚本，里面包含了 Johnny's Pizza 可能会说的所有可能的组合，以及我的机器人应该如何回应。然后我上了 Wit.ai，创建了一个 App。这涉及到在我的脚本中给它所有的东西，Johnny's Pizza 说，对于每一个，分配意图并指出任何应该报告给我的代码的数据。

![Wit.ai expressions and entities](img/c384ea7b5f1e2e9587fd56d45b78c352.png)

在 Wit.ai 中，你实际上创建了实体，意图只是其中的一种类型，但是我发现如果我把所有东西都当作意图，我的代码会更容易编写。这里显示的是一些表达的快照，即比萨饼店可能会说的话。我扩展了“就这些了吗？”一个显示 intent 实体，值为“asking_is_that_all”，这是我将在代码中寻找的。它上面的表达式和下面的表达式共享同一个实体，所以对于它们中的任何一个，我的代码只需要查找“asking_is_that_all”。

之后，我只需要根据他们的文档和 Github 上的示例代码，在我的 Raspberry Pi 上编写一些 Python 代码。我有一个放大器(一个嘈杂的 DIY)和扬声器连接到 Pi。我为对话的每个部分录制了单独的声音剪辑，并分别保存。wav 文件。对于我为机器人使用预先录制的语音的版本，我加深了机器人的声音，因为我的声音用于对话的双方。

在代码中，我遍历比萨饼店的声音剪辑，就好像我刚刚从手机上收到它们一样，一次一个地将它们发送到 wit . ai。wit . ai 进行语音识别和分析，并返回意图和数据。我也给扬声器播放这个片段。然后，我使用 intent 来计算机器人播放哪些片段作为响应，或者将哪些文本转换为语音，这取决于我为机器人采取的方法。你在上面听到的是我从 Pi 的扬声器中听到的对话。

代码可以在我们的 Github 上找到[。](https://github.com/Hack-a-Day/pizza-ordering-bot-using-wit.ai)

## 终极:谷歌双工人工智能是如何做到的

再听一遍谷歌的双工人工智能的对话，你会对人工智能产生的语言感到震惊。令人印象深刻的是，更令人惊奇的是，它没有涉及“如果-那么-否则”或决策树。相反，所有这些逻辑都被训练成一个神经网络，使用大量的样本电话对话，这些对话都是在我们只能梦想的硬件上进行的(或者通过在线服务付费使用)。所以现在我们必须用老方法来做那部分。

## 向 AIML 添加自然语言

我们可以做的一件事，这将是一个伟大的开源项目，将像 DeepSpeech 和 AIML 这样的东西结合起来，产生一些更类似于 DialogFlow 或 IBM Watson 的东西。也许到那时，通过电话订购比萨饼将变成只需按一个按钮，或者我们可以把它连接到 Alexa，让她启动它。当然，我们可能希望在通话开始时宣布我们是一个机器人，并在对话出现问题时得到提醒进行干预。或者把对话录下来留给后人，让人工智能十年后也有笑料。