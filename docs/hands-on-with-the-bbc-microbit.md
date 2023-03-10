# 英国广播公司的实践微:位

> 原文：<https://hackaday.com/2016/06/03/hands-on-with-the-bbc-microbit/>

漫长的等待，我们最新的复习用单板电脑终于来了！BBC micro:bit 免费提供给每个七年级的英国孩子，在教育界的一位朋友的帮助下，已经登陆 Hackaday。这个项目已经进行了一年的错误启动和延迟，但是学校在复活节假期前开始收到货物，学生们现在应该随时可以开始用它们上课，到本文付印时[你甚至可以为自己买一个](http://www.bbc.co.uk/news/technology-36416862)。

[![The micro:bit top view](img/503d385b17b388c6fe174f89d1e2090d.png)](https://hackaday.com/wp-content/uploads/2016/05/micro-bit-top-view.jpg)

The micro:bit top view

这是一个相当奇怪的提议，给一个基于 ARM 的单板计算机给程序员新手，希望他们可以学习一些关于计算机如何工作的知识，毕竟如果你习惯于其他类似的板，你可能会期望学习曲线相当陡峭。但我们的目标是将它定位为一个玩具，而不是我们可能习惯的那种开发板，因此需要进行一些调查，看看它取得了多大的成功。

打开包装，micro:bit 套件相当简约。主板本身、一根短 USB 导线、一个电池盒和一对 AAA 电池、一份说明书和主板本身。所有东西都是儿童尺寸，micro:bit 是一个 50 毫米乘 40 毫米的弯角印刷电路板。电路板的顶部有一个 5x 5 平方的 LED 矩阵和一对触摸开关，而底部有表面贴装处理器和其他组件，微型 USB 和电源连接器，以及一个复位按钮。沿着电路板的底部边缘是一个多路卡边连接器，用于 I/O 线，表面为 ENIG。在卡边缘连接器上，几个触点引出到用于鳄鱼夹的宽垫，鳄鱼夹带有电镀通孔以容纳 4 毫米香蕉插头，这些触点是接地和 3V 电源线，以及 3 条 I/O 线。

[![The micro:bit bottom view](img/8595ad88bef1a3337bc963afde39ea1f.png)](https://hackaday.com/wp-content/uploads/2016/05/micro-bit-bottom-view.jpg)

The micro:bit bottom view

与其他单板电脑相比，这款电脑显然是为 12 岁儿童设计的。这是一个 1.6 毫米厚的坚固电路板，没有引脚和尖钉连接器，显然已经采取措施确保尽可能低调。

在硬件方面，它有一个来自 Nordic Semiconductor 的 ARM Cortex M0 处理器、一个指南针、加速度计、蓝牙低能耗和 USB 以及前面提到的开关、led 和 GPIOs。

要使用该设备，您可以选择通过 USB 将其连接到您的计算机，或通过蓝牙低能耗连接到您的手机或平板电脑。遗憾的是，我们的设备都不支持 BLE，因此在本次评测中，我们将采用前一种方法。

所有编程都是通过选择基于 web 的环境来执行的，在线执行代码编辑和编译，并且在用户通过文件系统将其放置在 micro:bit 上之前，所得到的二进制文件作为下载文件到达。由于 micro:bit[也是一个 mbed](https://developer.mbed.org/platforms/Microbit/)，我们希望它可以使用 mbed 工具链进行编程，但这超出了本文的讨论范围。

开发环境都可以通过 [micro:bit 网站](http://www.microbit.co.uk)访问，在上面写代码不需要登录。点击“创建代码”按钮，你会看到四个选项，代码王国 JavaScript、微软块编辑器、微软触摸开发和 Python。micro:bit 传单上说你需要一台运行 Windows 7 或更高版本的 PC，或者一台运行 OS X 10.6 或更高版本的 Mac，然而我们在 Linux 桌面上使用 Chromium 没有遇到任何问题。每种不同的环境都有自己的风格和受众，因此值得依次考虑它们。

[![The Code Kingdoms Javascript editor](img/2376efd77d8a273a188f940553fecdd0.png)](https://hackaday.com/wp-content/uploads/2016/05/micro-bit-code-kingdoms-js.jpg)

The Code Kingdoms Javascript editor

首先是代码王国 Javascript。这不是你所期望的 Javascript 编辑器，相反，这是一个创建 Javascript 块的拖放式可视编码环境。左边是一系列包含可用代码块的菜单，中间是编码区，右边是软件微:位仿真器。在底部左边是在模拟器中运行你的代码的按钮，用你的其他脚本保存它，或者编译和下载它放在 micro:bit 上。

在使用中，代码王国编辑器是直截了当和直观的，你可以在我们的截图中看到一个简单的指南针的代码是非常快速的组装作为第一次努力。不幸的是，至少在我们的浏览器中，它非常慢，有时几乎到了无法使用的地步。特别是当你想删除一个代码块时，它会启动一个动画，显示它的垃圾箱打开了，这会让浏览器慢下来。当你加载一个网页并听到你的处理器风扇旋转时，这不是一个好的迹象。

[![The Microsoft Block editor](img/a7b10dbd9e62aa4cb56552e4a9c7b5ae.png)](https://hackaday.com/wp-content/uploads/2016/05/micro-bit-ms-block-editor.jpg)

The Microsoft Block editor

紧随代码王国编辑器之后的是微软的块编辑器。这是一个和 Code Kingdoms 编辑器一脉相承的拖放式可视化编辑器，除了没有假装构建一个更传统的编码语言之外，它是一个更快更流畅的体验。除了位于编码窗口上方顶部的编译和运行命令之外，该界面在布局上与 Code Kingdoms 编辑器大致相似。

在我们的截图中，你会看到一个非常简单的环境监视器，用来显示 micro:bit 的各种传感器的读数。然而，对于第一次使用该环境的人来说，这是一个简单而直观的软件。

[![Microsoft's Touch Develop editor](img/5558bc22d519323ac3484e3abc813808.png)](https://hackaday.com/wp-content/uploads/2016/05/micro-bit-ms-touch-develop.jpg)

Microsoft’s Touch Develop editor

第三个环境是来自微软的另一个环境，他们的触摸开发编辑器。这与其他编辑器不同，因为它是专门为平板电脑和手机上的触摸环境而设计的，所以我们在 Android 手机上测试了它。

虽然 Touch Develop editor 遵循与前两个构建代码相同的思想，从菜单中选择块，但它创建的内容更接近于文本代码，并要求用户手动输入函数参数等。我们发现它的帮助系统在这方面有点困难，如果你知道它的复杂性，它无疑是一个有用的编辑器，但对于第一次使用的用户来说，有一个相当大的学习曲线。

Touch Develop 团队已经尽他们所能在手机屏幕上做了很好的工作，它非常有用，但是由于有限的屏幕空间，它仍然有点笨拙和拥挤。幸运的话，这对平板电脑用户来说应该不是什么问题。

值得指出的是，这个编辑器可以存储为离线书签，这样就可以在没有互联网连接的情况下使用它，但是不清楚以这种方式编写的代码是如何编译的。

[![The micro:bit Python editor](img/f284997ea282a9dc354848bf8d76d4af.png)](https://hackaday.com/wp-content/uploads/2016/05/micro-bit-python.jpg)

The micro:bit Python editor

micro:bit 的最终编辑器选择是 Python，实际上是 MicroPython 的一个 micro:bit 构建。这个编辑器缺少软件 micro:bit 模拟器，但更像是黑客读者将会习惯的那种软件环境。主窗口是一个直接的文本编辑器，可以输入 Python 代码，没有预定义代码块的菜单。取而代之的是各种 micro:bit Python 库的全面介绍、教程和文档，一旦你掌握了这些，你就可以开始写代码了。

在使用中，如果你喜欢 Python，它非常简单。如果您的代码产生任何错误，它们会在 micro:bit 的 LED 矩阵中滚动显示，这可能会非常繁琐，但至少我们产生的错误是有信息的，并直接引导我们找到指南针代码中出现错误的点。

看看这个编辑器中可用的库，很明显 Python 是控制您的 micro:bit 的最强大的方法。除了其他编辑器中可用的简单函数，它还提供了 I2C、SPI、UART、Neopixels 等函数库。很明显，这就是 micro:bit 的“哇！”黑客最有可能被创造出来。

[![The micro:bit with its battery pack](img/cf90f8da9c09ac74a63ebbd7201ac01a.png)](https://hackaday.com/wp-content/uploads/2016/05/micro-bit-with-battery.jpg)

The micro:bit with its battery pack

看了所有的编辑器后，我们的选择是 Python 作为有经验的程序员的最强大的编码环境，而 Microsoft Block editor 作为初学者的最有用的拖放环境。代码王国编辑器很好，但非常慢，触摸开发编辑器有点复杂。值得一提的是，所有的编辑器都有一个本地保存代码的选项，这将生成一个 LZMA 压缩文件，原始代码采用 JSON 结构。

当然，虽然我们中的一些人可能会从中受益，但这个板不是为黑客读者而是为儿童制作的。如果它的配方正确，十年后，它将被一代新毕业生称为让他们进入软件行业的机器，但它达到目标了吗？因为有问题的孩子现在才开始上第一堂课，所以现在下结论还为时过早，但是老师借给我们这个复习的小片段告诉我们只有两个小问题。由于没有开关，他们以惊人的速度消耗电池，由于他们失败的程序没有显示 led，他们认为当他们的软件不工作时，他们已经杀死了它。第一种可能是孩子们会通过学习拔下包装来修复自己，也许 micro:bit 人可以通过软件更新来修复第二种。如果这是最糟糕的事情，尽管也不会有太多的错误。