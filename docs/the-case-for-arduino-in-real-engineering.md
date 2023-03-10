# “真实工程”中的 Arduino 案例

> 原文：<https://hackaday.com/2015/10/20/the-case-for-arduino-in-real-engineering/>

十多年来，Arduino 一直保持着它的受欢迎程度，因为“这个小开发板旨在让艺术家和电子爱好者对物理计算感兴趣。”一路上，它在大学课程中找到了一个角落，一次性的燃烧人装备，以及无数在这里着陆的项目。毫无疑问，Arduino 在爱好者中有一个舒适的家，但它也生活在其他地方。随着消费产品从功能迭代进入用户测试，Arduino 生活在工程设计实验室中。在化学实验室，科学家需要在必要时将一些传感器数据输入电脑。尽管皱眉，但我们会看到当有人用 Arduino 闪烁 LED 并将其放入项目框时，Arduino 会一直存在。我想我应该更深入地探究一下为什么艺术家和工程师都如此频繁地重访这块板。

### Arduino，我们真的喜欢恨它吗？

对于经验丰富的工程师来说，对最新的基于 Arduino 的喂猫 Kickstarter 投以目光并不罕见，他们无耻地将实际的 Arduino 板藏在 3D 打印的外壳内。草率？当然可以。粗糙的，还是未经打磨的？当然可以。值得卖吗？这取决于消费者的标准。尽管如此，这些挑剔的工程师可能也在为他们的下一个燃烧人视觉暂留 LED 显示屏出谋划策——你猜怎么着？它有一个 Arduino 大脑！看似伪善的事情实际上是完全合理的。在这两种情况下，每个设计师都在用 Arduino 做自己最擅长的事情:抽象出粗糙的细节，以便设计可以快速进行。怎么会？硬件抽象的魔力。

### 认识硬件抽象层 HAL

在一个“我们只想让事物闪烁”的世界里，Arduino 有一些漂亮的开箱即用的功能，可以让我们快速启动和运行。当然，开发工具是跨平台的。当然，编程是通过一个方便的 usb 接口进行的。然而，这些功能都无法与 Arduino 的最大优势——硬件抽象层(HAL)相媲美。

在嵌入式世界里，HAL 并不是什么新鲜事物，但是简单地拥有一个 HAL 就可以让世界变得不同，它可以让艺术家和嵌入式工程师实现相同的最终目标，即通过微控制器快速、有计划地与物理世界进行交互。在 Arduino 中， *HAL* 只不过是覆盖在 C++编程语言之上的类和函数调用的集合，在某种意义上，“把它变成 Arduino 编程语言”(我知道，[没有 Arduino 语言](http://hackaday.com/2015/07/28/embed-with-elliot-there-is-no-arduino-language/))。如果你想知道这些功能是如何实现的，看看 Arduino 源代码中的 [AVR 目录](https://github.com/arduino/Arduino/tree/master/hardware/arduino/avr/cores/arduino)。

有了硬件抽象层，我们不需要知道我们程序的函数调用如何翻译成 Uno 的 ATMEGA328p 芯片上可用的各种外设的细节。当 Serial.available()为真时，我们不需要知道数据是如何接收的。我们不“需要知道”Wire.begin()对从设备使用的是 7 位寻址还是 10 位寻址。使这些高级调用成为可能所需的大量设置已经通过 HAL 为我们处理好了。结果呢？如果我们只是试图与物理世界进行一些简单的交互，我们可以节省时间来阅读芯片的数据手册，编写帮助函数来实现芯片功能，以及了解微控制器的独特特性和怪癖。

### 跨平台兼容性

![Teensy 3.2 keeps form factor but adds hardware features](img/018bd8880f5d64d3dff18d56233ddef6.png)

[Teensy 3.2](https://www.pjrc.com/store/teensy32.html) keeps form factor but adds on-chip hardware features compared to 3.1

在某些情况下，HAL 开始崩溃。也许微控制器没有必要的硬件来同时驱动 16 个伺服系统，同时轮询串行端口和解码串行数据。在某些情况下，我们可以通过切换 Arduino 平台来解决这个问题。也许我们确实需要三个串口，而不是一个(Teensy 3.2)。也许我们*确实*需要每个管脚都有脉宽调制(PWM)能力(Due)。因为有了硬件抽象层，源代码的其余部分可以基本保持不变，尽管在这个过程中我们可能会切换芯片架构甚至编译器！当然，在一个为目标平台*开发代码*很重要的环境中，努力编写我们在 Arduino 中看到的通用代码是没有意义的，如果 Arduino 不具备最终目标所需的必要功能，甚至一开始就使用 Arduino 也是没有意义的。尽管如此，对于产生一个“结果很重要，但是实现的方法不重要”的端到端解决方案，如果在达到最终目标之前需要改变目标硬件，那么编写 Arduino 代码可以节省时间。

### 哈尔的缺点

当然，使用 HAL 加快开发速度也是要付出代价的，有时转换平台并不能解决问题。首先，阅读 Arduino 编程语言文档并不能告诉我们任何关于运行它的硬件的限制。比方说，如果串行数据不断到达，但我们没有使用 Serial.read()读取它，直到数百个字节被发送出去，会发生什么情况？如果我们*需要和一个要求 10 位寻址的 I2C 设备对话，会发生什么？不看原始源代码，我们不知道这些问题的答案。第二，如果我们选择使用通过 HAL 给我们的函数，我们会受到它们的实现的限制，当然，除非我们想改变核心库的源代码。原来，Serial 类实现了一个 64 字节的环形缓冲区来保存最近接收到的串行数据。对于我们的应用程序来说，64 字节够大吗？除非我们改变核心库源代码，否则我们将不得不使用它们的实现。*

 *以上两个限制都涉及到理解最初的 HAL 是如何工作的，然后通过改变 Arduino 核心库源代码来改变它。尽管有这种自由，但大多数人不会定制它！这个奇怪的事实证明了核心库是如何满足目标用户(艺术家)的需求的，因此 Arduino 赢得了大量的用户。

### 裸机发言的优点

![digitalWrite takes a whopping 52-55 cycles to change pin direction! [image source]](img/53ff71b1663d09a98b17d5e94d37c450.png)

digitalWrite 要花多达 52-55 个周期来改变引脚方向！【[图片来源](https://billgrundmann.wordpress.com/2009/03/03/to-use-or-not-use-writedigital/)

直接调用硬件有好处吗？绝对的。在我们之前，一些好奇的调查者用 digital write 测量了最大引脚切换频率，大约为 100 KHz，而直接操作硬件导致引脚切换频率大约为 2 MHz，快了大约 20 倍。也就是说，直接调用硬件值得吗？视情况而定，但是在许多情况下，时间紧迫不是什么大问题，功能性端到端系统的目标比“我们如何到达那里”更重要，那么可能不是！当然，在有些情况下，时间紧迫的*并不重要，Arduino 无法满足要求，但在这种情况下，这是嵌入式工程师的工作。*

### 用哈尔，卢克！

为了实现端到端的解决方案，其中“我们如何到达那里”的过程并不重要，Arduino 在许多简单的场景中表现出色。请记住，虽然 HAL 使我们无法了解我们的微控制器的太多细节，否则我们可能会在数据手册中找到这些细节，但我并不主张所有人都从此放弃自己的数据手册。然而，我*是*的支持者，我主张“为了把工作做好，知道的不比你需要知道的多。”如果我试图将一些传感器数据记录到 PC 中，并且我发现我可以节省几天时间来阅读数据手册和配置 SPI 端口，因为有人已经编写了 SPI.begin()，请给我一个 Arduino。

如果你已经卷起袖子拿出一个 Arduino 作为你工作的第一选择，我们很想听听除了偶尔的副业之外，你还想到了什么用途。请在下面的评论中告诉我们。*