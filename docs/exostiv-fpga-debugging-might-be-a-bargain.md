# Exostiv FPGA 调试可能很划算

> 原文：<https://hackaday.com/2018/06/30/exostiv-fpga-debugging-might-be-a-bargain/>

有 4000 美元可以花吗？即使没有，也要继续阅读——尤其是如果你是用 FPGAs 开发的话。Exostiv 的 FPGA 调试设置成本约为$4K，但如果你需要调试一个复杂的 FPGA 设计，并且你的时间有任何价值，这可能不是很贵。话说回来，我们大多数人都很难证明 4000 美元的测试设备是合理的。但是我们想思考 Exostiv 在做什么，为什么我们看不到更多。传统上，调试 FPGAs 意味着使用 JTAG，可能还需要一些自定义模块，这些模块就像逻辑分析仪一样，会占用你的设备空间。Exostiv 也使用你的一些设备，但不是建立一个 JTAG 通信逻辑分析仪它…嗯，这里是他们的网站上说:

> EXOSTIV IP 使用 mgt(多千兆收发器)将捕获的数据从 FPGA 传输到外部存储器。EXOSTIV IP 支持以 FPGA 的运行速度(16 个数据集 x 2，048 位)同时重复捕获多达 32，768 个内部节点。
> 
> EXOSTIV IP 提供动态多路复用器控制，无需重新编译即可捕捉更多数据集。数据集的动态开/关控制可让您选择数据集并保留 MGT 带宽，以备需要更深入地捕获精简数据集时使用。

简而言之，这意味着他们使用高速通信将原始数据发送到一个有内存的盒子，并连接回 PC。这意味着它们可以存储更多的数据，在一定时间内从芯片中输出更多的数据，并进行复杂的处理。你可以在下面看到关于这款设备的视频，在他们的频道上也有更详细的视频。

有两件事你可能想知道。首先，为什么不直接将数据发送到 PC，而不是一个中间盒。注意这个盒子有一个 USB 3 接口连接到电脑。这很快，但还不够快。

另一件你可能会疑惑的事情是，既然你的开发板没有 mgt，你也没有 4000 美元去买调试工具，为什么你会读到这里。但是我们想到，虽然这个想法的实现看起来非常健壮，但是我们没有理由不能将其应用到我们的 FPGA 设计中。为什么我们没有看到一个黑客设计使用一个相当便宜和快速的 I/O(也许是 LVDS)将数据传输到一个有一些内存的 Arm 板。事实上，您可能会认为可以将 FPGA 的模块分开，这样就有了一个内核和一个通信通道，可以支持不同的功能。

当然，[开源调试内核](https://github.com/enjoy-digital/litescope)并非闻所未闻，但它们往往像传统的 JTAG 调试器一样工作，本质上是在 FPGA 的备件上构建[一个逻辑分析器](https://opencores.org/project/wbscope)。我们还没有见过类似 Exostiv 的解决方案。可能我们见过的最接近的是[康乃尔](https://hackaday.com/2017/05/17/logic-analyzer-on-chips/)的这个设备，但是它显示在 VGA 监视器上。也不缺少使用 FPGAs 的独立逻辑分析仪。

 [https://www.youtube.com/embed/wBU_wRri05Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wBU_wRri05Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

