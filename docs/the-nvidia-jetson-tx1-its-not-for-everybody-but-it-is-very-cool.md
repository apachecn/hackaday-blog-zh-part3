# Nvidia Jetson TX1:它并不适合所有人，但它非常酷

> 原文：<https://hackaday.com/2015/11/24/the-nvidia-jetson-tx1-its-not-for-everybody-but-it-is-very-cool/>

上周， [Nvidia Jetson TX1 发布](http://hackaday.com/2015/11/10/nvidia-brings-computer-vision-and-deep-learning-to-the-embedded-world/)。这个信用卡大小的模块是一台“超级计算机”，号称比最新的英特尔酷睿 i7 处理器处理能力更强，而运行功率不到 10 瓦。据推测，这是一款将为下一代产品提供动力的设备，采用了嵌入式领域前所未闻的技术。

现代智能手机可能是 10 年或 15 年前制造的。毫无疑问，笔记本电脑 CPU 的处理能力是存在的，最初 iPod 中的微型机械硬盘足够容纳 Napster 的 MP3 和所有电话联系人。另一方面，这款使用了 15 年的智能手机的电池是不可能的。未来依赖于电池和低功耗计算。Jetson TX1 是引领我们走向未来的主板吗？需要亲自动手才能找到答案。

![Nvidia-2](img/9585618c8eb5708eed9c084981a80304.png)

The Nvidia Jetson TX1 and Carrier Board

### TX1 是什么

Jetson TX1 是一个 50x87mm 毫米的微型模块，封装在一个散热器中，体积大约相当于一包香烟。在一块铝下面是一个 Nvidia Tegra X1，这是一个结合了 64 位四核 ARM Cortex-A57 CPU 和 256 核 Maxwell GPU 的模块。该模块配备了 4GB 的 LPDDR4-3200，16GB 的 eMMC 闪存，802.11ac WiFi 和蓝牙。

该模块通过一个 400 引脚连接器(来自 [Samtec](https://www.samtec.com/connectors/high-speed-board-to-board/high-density-arrays/searay) ，顺便说一下，该公司对产品样品非常开放)与外界连接，为半打 Raspberry Pi 风格的相机提供 6 个 CSI 输出，2 个 DSI 输出，1 个 eDP 1.4，1 个 eDP 1.2 和 HDMI 2.0 用于显示器。存储通过 SD 卡或 SATA 提供。其他端口包括三个 USB 3.0、三个 USB 2.0、千兆以太网、一个 PCIe x1 和 PCIe x4，以及一系列 GPIOs、UARTs、SPI 和 I2C 总线。

目前，获得所有这些额外端口的唯一方法是 Jetson TX1 载板，这是一种有效的 MiniITX 主板。把这个载板装在一个盒子里，改装电源，弄清楚如何连接前面板按钮，你就有了一台体面的台式电脑。

不过，这不是一台台式电脑，也不是树莓派或 Beaglebone 的替代品。这是一个工程工具——一个为处理未来先进机器人工作而建造的设备。

### 基准

没有基准测试，任何技术评估都是不完整的，因为这是一款 Nvidia 主板，这意味着对图形性能的深入研究。

Nvidia 送来的评测单元带来了令人难以置信的大量文档，指引我前往 [GFXBench 4.0 Manhattan 3.1](https://www.youtube.com/watch?v=F1_1Zyq3M7Y) (以及 T-rex one)测试图形性能。

[![Manhattan](img/cd11ac766b2b7b8bd1482e15fb3f8080.png)](https://hackaday.com/wp-content/uploads/2015/11/manhattan.png)

就图形性能而言，TX1 与几年前的普通移动芯片组没有太大区别。这是可以预料的；指望英伟达在 10 瓦模块里放一个泰坦是不合理的；泰坦本身吸收大约 250 瓦。

[![test suite](img/bea84d5a89d247e1897eb75c9c892271.png)](https://hackaday.com/wp-content/uploads/2015/11/test-suite.png)CPU 性能怎么样？ARM Cortex A57 在小型信用卡大小的开发板中并不常见，但也有一些实际的产品使用它。TX1 无论如何都不是一个发电站，但它在测试中以大约三倍的系数击败了 Raspberry Pi 2 Model B。

与台式机/x86 性能相比，最佳性能指标评测再次将 Nvidia TX1 置于几年前的中等台式机的同一领域。不过，这款台式机的总功耗可能约为 300 瓦，而 TX1 的功耗仅为 10 瓦。

如果你在挖掘比特币，这不是你想要的板，如果你需要一个强大的便携式设备，可以连接到任何东西，这也不是你应该使用的板。这是定制设计。Nvidia TX1 是一个旨在集成到产品中的模块。这不是一个为“创客”设计的主板，也不是为他们设计的。这是一款面向工程师的主板，需要在一个合理的小封装中提供足够的功率，并且不会耗尽电池。

Nvidia TX1 配备了运行速度接近 2 GHz 的 ARM Cortex A57 四核、4gb RAM 和功率预算合理的强大显卡，远远超过了常见的小型 Linux 主板。它远远超过了 Raspi，最新的 Beagleboard，[给了英特尔 NUC 主板一个机会。](http://www.intel.com/content/www/us/en/nuc/overview.html)

[![That huge and heavy heatsink is useful; while benchmarking the TX1, temperatures were only one or two degrees above ambient](img/835747622db1d28edb50bbdada7d8455.png)](https://hackaday.com/wp-content/uploads/2015/11/dsc_0023.jpg)

That huge and heavy heatsink is useful; while benchmarking the TX1, temperatures were only one or two degrees above ambient

就绝对功率而言，TX1 大约相当于三四年前的入门级笔记本电脑。

Jetson TX1 的核心是性能功耗比。这是非凡的，新的，令人兴奋的；这是以前从未有人做过的事情。如果你相信 Nvidia 授权我访问的大量技术文件，这是迈向真正智能的嵌入式设备世界的第一步，这些设备掌握了计算机视觉、机器学习和其他一系列尚未真正进入嵌入式世界的东西。

[![Alexnex images processed per second per watt. No, Joules do not exist.](img/67577da240111d0ea9535a15f92a4611.png)](https://hackaday.com/wp-content/uploads/2015/11/energy.png)

Alexnex images processed per second per Watt. No, Joules do not exist.

这就是杰特森 TX1 的问题所在；因为以前没有这样的平台，所以开发堆栈、示例和用户社区根本就不存在。为 Nvidia 嵌入式系统论坛投稿的人数很少——我们的 Hackaday 文章获得的评论比 Nvidia 论坛上的一个帖子还多。像所有的新平台一样，唯一缺少的是社区，将 Nvidia 置于鸡和蛋的场景中。

这是工程师的平台。具体来说，建造自动高尔夫球车和汽车的工程师，跟随你的四轴飞行器，以及可以通过图灵测试至少 30 秒的机器人。这是一个令人难以置信的硬件，但不是一个被设计成坐在电视旁边的电脑。TX1 是一个工程工具，它意味着进入其他设备。

### 另类应用，比如 Gamecube

也就是说，我可以看到 TX1 有一些非常有趣的应用。我的车需要一个新的车头单元，用 TX1 制造一个车头单元至少可以再跑 20 万英里。对于非常熟练的业余工程师来说，TX1 模块打开了许多大门。六个网络摄像头可能是许多艺术家都想尝试的东西，两个 DSI 输出和一个显卡将允许一些非常有趣的用户界面。

也就是说，TX1 载板不是这些应用的分线板。我希望看到类似于[spark fun 为英特尔 Edison](https://www.sparkfun.com/categories/272) 组装的东西——为每一个可以想象的用例提供几十个分线板。TX1 载板的 PCB 文件可以通过 [Nvidia 开发者门户](https://developer.nvidia.com/embedded/downloads)获得(希望你喜欢 OrCAD)，用于该模块的 400 针连接器供应商 Samtec 非常容易合作。对于一个拥有回流焊烤箱的人来说，为 TX1 创造一个比迷你 ITX 主板方便得多的突破并不是不合理的。

目前，没有多少电脑配备 ARM 处理器，也没有这么大的马力。令人印象深刻的强大的 ARM 板，如新的 BeagleBoard X15 和那些遵循 [96Boards 规范](https://www.96boards.org/products/)的存在，但这些没有将现代显卡烘焙到模块中。

如果没有人在 TX1 上做一些让应用程序具有大众吸引力的单调工作，就很难说这个板在模拟 GameCube 或任何其他通用应用程序方面表现得有多好。硬件可能已经准备好了，但 TX1 的评审人员只有不到一周的时间来为最苛刻的应用程序构建兼容的版本，而这种板*不是为*设计的。

### 一切都是为了效率

TX1 是“模块上的超级计算机”吗？是的，也不是。尽管与最新的 core-i7 CPU 相比，Alexnet 在机器学习任务上表现得相当好，但 Alex net 机器学习任务是最适合 GPU 的任务。这就像问塞斯纳 172 和布加迪威龙哪个飞得更好？塞斯纳是迄今为止更好的飞行器，但如果你正在寻找一台“超级计算机”，你可能会想看看 747 或 C-5 银河。

另一方面，在高功率 ARM 板*与*GPU*和*的交叉点上，没有多少板或模块在 10 瓦的功率预算上。这是建造未来的机器、机器人和自主设备所需要的东西。但即使这样，它仍然是一个利基产品。

我迫不及待地想看到 TX1 周围出现一个社区。打几个电话给 Samtec，在 KiCad 呆上几个小时，然后团购模块本身(1000 片装 299 美元)，这可能是非常非常有趣的事情的开始。