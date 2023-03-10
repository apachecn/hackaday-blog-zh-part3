# 使用 Glitch 在几分钟内定制 Alexa 技能

> 原文：<https://hackaday.com/2018/01/17/an-alexa-skill-among-other-things-in-a-few-minutes/>

作为黑客，我们喜欢把自己想象成一群有逻辑的人。但事实是，我们和普通大众一样容易受时尚的影响。曾经有一段时间，很酷的项目将绿色 led 换成蓝色 led，或者在别人没有的地方添加 WiFi 连接。现在最流行的是把你的项目和个人助理联系起来。问题是，这需要软件。软件存在于某个公共可访问的网络上，当你第一次玩自定义的 Alexa 技能时，谁会想要处理它呢？

如果你有一台面向互联网的电脑，那也行。如果你没有，你可以借用亚马逊的，但是你需要了解他们的基础设施，这本身就是一项工作。然而，有一个非常简单的方法来启动 Alexa 技能。我使用一个名为 [Glitch](https://glitch.com/) 的网站，很快就建立并运行了一个。故障是所有事情的一部分。它是一个 web 托管服务，一个 Node.js 的编程 IDE，一个代码库，以及其他一些东西。该网站来自为我们带来 Trello 并帮助启动 Stack Overflow 的公司。

Glitch 不是让 Alexa 掌握技能。它是关于轻松创建 web 应用程序和服务的。然而，这是制作一个 Alexa 技能所涉及的 90%的工作。你需要一个 Glitch 账户和一个亚马逊开发者账户。两者都是免费的，至少对于我们想要完成的事情是如此。Glitch 也有一些 Google Home 的模板。我都有，但决定专注于 Alexa，没有特别的原因。

诚然，我的示例技能并不是在执行一项特别困难的任务，但它是一个很好的开端，如果你想发展自己的技能，它会给你一个良好的开端。虽然我使用了一个特定的工具，但是如果您需要的话，没有理由不从这个工具转移到您自己的基础设施上。Glitch 的一个好处是，你可以实时共享代码，人们可以对其进行重新组合。想象一个 GitHub fork，但是在那里你可以试着运行我的副本，你的副本也可以立即运行。事实证明，对于 Alexa 技能来说，拥有它并不像你希望的那样有用，因为你仍然需要告诉亚马逊。但这确实意味着你可以借用一些 Alexa 技能(包括我的)来开始你的学习，就像我借用一个来开始我的学习一样。

## 你需要它吗？

你可能会问自己的第一个问题是，你需要 Alexa 技能吗？我最近让 Alexa 用 IFTTT 控制了我的 3D 打印机，完全不需要软件开发。然而，如果你真的想声称你和一个虚拟助手一起工作，你将不得不在某个地方写一些代码。

当然，还有一个更大的哲学问题:你需要做这些吗？我承认，我发现让我的 3D 打印机进行语音控制很有用，因为我可能会用双手进行调整，而且我不必摸索按钮来让机器进行自动循环。我不太相信我需要一个虚拟助手来启动我的无人机。话又说回来，也许这就是你想做的，这取决于你。

## 入门指南

如果你还没有，你也可以去注册一个亚马逊开发者账户。然后去格林奇那里注册。建立一个 Alexa 技能至少有两个模板。有一个[最基本的](https://barebones-alexa-skill.glitch.me)和一个更复杂的[检索天气预报](https://alexa-skill.glitch.me/)。如果你在看网页，它可能没有多大意义。请记住，网络服务器是为了与 Alexa 交谈，而不是与人交谈。右上角是一个有一对鱼的图标。如果你点击那里，你可以查看源或你可以重新混合。

[![](img/fb34ec723d715212495e45d0424527fb.png)](https://hackaday.com/wp-content/uploads/2017/12/glitch.png)

我决定重新混合天气预报服务，因为我认为这是一个更好的例子。然后我去掉了所有与天气相关的代码(除了一些文档)，写了一个简单的 Javascript 函数:

```

function get_fact() {
  var factArray = [
  'Hackers read Hackaday every day',
  'You know you are 3D printing too much when you tell someone you are extruding mustard on your hot dog',
  'The best microcontroller is the one already programmed to do what you want',
  'We can all agree. All software has bugs. All software can be made simpler. Therefore, all programs can be reduced to one line of code that does not work.',
  'I hate talking to flying robots. They just drone on.',
  'If you call your morning cup of coffee installing Java, you need a hobby',
  'I have heard that in C functions should not call each other because they usually have arguments',
  'I refused to learn C plus plus. I saw see-out being shifted left hello world times and gave up',
  'If cavemen had thought of binary we could all count to 1023 on our fingers',
  'If you can\'t hack it, you don\'t own it.'
  ];
  var randomNumber = Math.floor(Math.random()*factArray.length);
  return factArray[randomNumber];
}

```

剩下唯一要做的就是将代码挂接到 Web 服务框架上。

## 表达

Glitch 在这个项目中自动建立了一个名为 Express 的库。它本质上是一个简单的网络服务器。一旦创建了主 app 对象，您就可以设置路由，以便在有人调用特定的 web 服务时执行您的代码。它还包括一个表示 Alexa 服务的对象。我不需要编写代码来设置它，但它就在这里:

```

app = express(),
// Setup the alexa app and attach it to express before anything else.
alexaApp = new alexa.app(&quot;&quot;);

// POST calls to / in express will be handled by the app.request() function
alexaApp.express({
  expressApp: app,
  checkCert: true,
// sets up a GET route when set to true. This is handy for testing in
// development, but not recommended for production.
  debug: true
});

```

我想提供两种方法。一个是当有人打开我的技能时(顺便说一下，我称之为黑客事实——它给出了关于黑客和相关事物的幽默事实)。当有人说“Alexa，告诉 Hacker Fact 给我一个事实”时，另一个方法将会启动或者类似的东西。

最后一位被称为意图。意图可以有表述(比如“给我一个事实”)，也可以有槽。我没有使用任何插槽(但是天气示例使用了)。使用吃角子老虎机，你可以把这个人的命令的一部分作为一个参数提供给你。例如，我可以让你说，“Alexa，告诉 Hacker Fact 给我一个关于 Arduinos 的事实。”然后我可以构建意图，使它听到“about”后的下一个单词是一个 slot，并在我的代码中解析它。

你可能不需要它，但如果你好奇想了解更多关于 Express 的信息，[看看这个视频](https://www.youtube.com/watch?v=gnsO8-xJ8rs)。

## 这两种方法

这里有两种方法:

```

alexaApp.launch(function(request, response) {
 console.log({"App launched");
 response.say('Hi from your friends at Hackaday. Ask me for a fact to learn something interesting or possibly funny.');
});

alexaApp.intent("HackerFact", {
 "slots": { },
 "utterances": [
 "Tell me a hacker fact",
 "Give me a hacker fact",
 "tell me a fact",
 "give me a fact",
 "go",
 "fact"
 ]
 },
 function(request, response) {
 console.log("In Fact intent");
 response.say(get_fact());
 }
) <span data-mce-type="bookmark" style="display: inline-block; width: 0px; overflow: hidden; line-height: 0"; class="mce_SELRES_start"></span>;

```

注意,“HackerFact”意图有一组将被发送到 Amazon 的话语。你可以在网上找到完整的 HackerFact 代码。别忘了，你可以通过页面右上角的两条鱼图标来查看源代码或混音。

所有代码都在 index.js 文件中。还有一些其他的文件，但是对于这个任务，除了修改包文件或文档中的一些文本之外，您可能不会对它们进行任何修改。

## 在亚马逊上

奇怪的是，接下来的部分可能更难。在亚马逊开发者网站的首页，你需要选择 Alexa 技能，然后点击“添加新技能”按钮。你将看到的许多条目都与更复杂的技能有关。另外，我不打算发布我的技能，但它仍然会显示在我的帐户中。如果你做一些文书工作，你可以把你的技能提交给选定的用户进行测试，甚至直接发布。

以下是您需要在技能信息选项卡上填写的字段的概要:

*   技能类型=自定义交互模型
*   Name =您喜欢的任何显示名称
*   调用名称=这是人们会要求 Alexa 使用的名称(例如，“Alexa，告诉黑客事实…”意味着我的调用名称是黑客事实)

[![](img/b22ed26f6081a33a9ee7d3ca20ee6dca.png)](https://hackaday.com/wp-content/uploads/2018/01/amz.png)

顺便说一句，我运气不好，在调用名设置好之后更改它，所以要好好考虑这个问题。

下一页(交互模型)看起来很复杂，但实际上并不复杂，这要感谢 Glitch 提供的库。打开你的故障项目。如果您正在查看信号源，请单击屏幕上部的“显示”。默认项目会导致数据转储出现在主页上(通常情况下，没有人会看到它),其中包含了该页面所需的信息。

意图模式框需要主页中“模式:”之后和“话语:”之前的所有内容。包括牙套。我的意图模式如下所示:

```

{
 "intents": [
 {
 "intent": "HackerFact"
 },
 {
 "intent": "AMAZON.CancelIntent"
 },
 {
 "intent": "AMAZON.StopIntent"
 }
 ]
}

```

页面的其余部分在“话语”之后有一些行，这些行是最后一个框所需要的。对于这个例子，中间的框可以保持为空。

## 连接 Glitch 和 Amazon 的更多步骤

在配置选项卡中，您可以选择 HTTPS，然后输入来自 Glitch 的 URL。要找到那个 URL，打开屏幕左上方的项目名称，你会看到它和一个复制按钮。比如我的是 https://hacker-fact.glitch.me，不允许账号链接，可以把所有可选框都留着。

在下一个屏幕上，您将希望选择“我的开发端点是一个域的子域，该域具有来自证书颁发机构的通配符证书”，因为这就是 Glitch 的工作方式。这就是你在那一页上所需要的。

此时，你的技能应该会出现在与你的账户相关的任何 Alexa 上(包括手机上的 Reverb 之类的 Alexa 应用)。您也可以在控制台中进行测试，看看事情是否正常。

## 释放猎犬

这足以让你的代码与你的 Alexa 一起工作。我不会公开这个技能给其他人使用，但是如果你想继续自己的话，这是一个选择。您也可以将 Glitch 用于其他事情，包括一些 Raspberry Pi 和一些其他物联网类型的平台。如果你四处看看，你可能会发现一些有趣的东西。

当然，您可以设置自己的服务器来完成 Glitch 为您做的所有事情——甚至可以在树莓 Pi 上完成。你也可以让 Amazon 将你的代码托管为[一个 Lambda 函数](https://developer.amazon.com/docs/custom-skills/host-a-custom-skill-as-an-aws-lambda-function.html)(即没有固定 web 服务器的 web 服务；见视频，如下)。如果您喜欢写作技巧，Amazon 文档并不坏，但是有时直接投入工作是有价值的。

 [https://www.youtube.com/embed/zt9WdE5kR6g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zt9WdE5kR6g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

