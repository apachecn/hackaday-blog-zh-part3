# 云中的硬件加速

> 原文：<https://hackaday.com/2018/05/05/hardware-acceleration-in-the-cloud/>

电脑在很多方面都很棒。然而，通用计算机可以从某些任务的帮助中受益，这就是为什么你的显卡和声卡都有自己的专用硬件来卸载 CPU。如果 Accelize 成功了，你的一些硬件加速将会在云中完成。是的，我们知道。云是本周的流行语，我们也厌倦了听到它。然而，这项服务是一种特别有趣的方式，可以为任何联网的 CPU 增加 FPGA 能力。

目前，只有四种加速器可用，包括硬件辅助的随机数生成器、GZIP 加速器、快速搜索文本的引擎和 BMP 到 JPEG 转换器。例如，该公司声称，搜索引擎可以在 6 分钟内在 60 GB 的维基百科档案中找到 2500 个条目。他们声称一个传统的 CPU 需要 16 天才能完成同样的任务。BMP-JPEG 转换器的处理速度比实时高清视频所需的速度更快。

在这种情况下，云是托管在亚马逊云或 OVH 公共云中的 FPGA 资源。他们显然会在某个时候使用“硬币”系统对服务收费。然而，现在他们只允许你用一个电子邮件地址注册，并向你的账户存入 50，000 个硬币。很明显，硬币是一美元一千个。

作为硬件，有一定的局限性。例如，搜索引擎不能处理超过 2500 个搜索词，每个词不能超过 36 个字符。不过，这已经很慷慨了。在亚马逊云上，搜索引擎每秒处理 145 MB，每 128 MB 花费一枚硬币。所以花一美元，你可以处理大约 128 GB 的数据。

您需要一个 API 密钥来使用该服务。据推测，这就是他们如何知道在哪里扣除硬币。你可以在使用 Python 的 [GitHub](https://github.com/Accelize) 上找到使用每个服务的例子。Python 没有什么神奇的地方，尽管你不介意弄脏自己的手。Python API 提供了启动服务和传输文件的简单调用。但是任何可以处理 REST API 的东西都可以使用这个服务。

Accelize 产品有两个有趣的地方。首先，像 Raspberry Pi 这样的小型计算机从这样的加速中获益最多。在不了解实际成本的情况下，很难说它是否值得投资，但它仍然很有趣，并可能开辟新的可能应用。

另一个有趣的事情是，Accelize 显然意味着创建一个“类似应用商店”的环境。他们正在征求 FPGA 开发人员来创建加速器，使他们可用，并将其货币化。此外，他们正在建立另一个商店，以提供开发人员可以用来构建加速器的 IP 核心。例如，假设您在开发人员的商店(他们称之为 QuickStore)中放置了一个 FPGA“核心”来缩放视频。有人开发加速器做视频可以用这个核心。用户将使用加速器，这将花费一定数量的硬币。一些收入将归 Accelize，一些归加速器开发者，一些归视频缩放器开发者。

如果这个项目成功了，这将是一个很好的利用你的 FPGA 技能的方式。我们看到的唯一问题是这些 FPGA 加速器的适用性。例如，使用 FPGA 的一个原因是为了处理实时处理。然而，将 FPGA 放在云中需要一定的开销以及时间和可用性的不确定性。如果开销与处理时间相比很小，那就是成功的。但是很明显，有些 FPGA 的用途不适合云计算。

如果你想了解更多关于 FPGAs 作为通过提供加速器功能致富的前奏，你可以从[我们的教程](https://hackaday.com/2015/08/19/learning-verilog-on-a-25-fpga-part-i/)开始。对了，我们通常会想到用 Verilog，VHDL，或者类似的东西来配置 FPGAs。你可以用加速器中的 FPGAs 来实现，但是你也可以[混合 C 代码](https://hackaday.com/2017/04/26/fpgas-in-c-with-cynth/)，这并不是没有听说过。