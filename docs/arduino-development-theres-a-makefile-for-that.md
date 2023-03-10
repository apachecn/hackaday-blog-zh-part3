# Arduino 开发；这有一个 Makefile 文件

> 原文：<https://hackaday.com/2015/10/01/arduino-development-theres-a-makefile-for-that/>

硬件和软件相结合，Arduino 做了很多正确的事情。它通过一个漂亮的硬件抽象层降低了嵌入式系统开发的门槛。它旨在通过支持 Windows、Mac OSX 和 Linux 操作系统来实现跨平台兼容性。它不再需要外部程序员来让你快速启动和点亮这些 led。

然而，有一件事是我们大多数人永远不会停止诅咒的，那就是 IDE。许多人强烈反对基于 Java 的文本编辑器，因为它的编译和链接过程晦涩难懂，不能容纳 C 或 C++源文件，而且(嘘！)它缺少 Vim 键绑定。幸运的是，我们的呼声被听到了，就像许多基于社区的项目一样，社区用定制的解决方案进行了反击。

### 呼叫所有脾气暴躁的工程师:Arduino-Makefile

进入[Arduino Makefile](https://github.com/sudar/Arduino-Makefile)。

最初作为[Sudar]的[轻量级程序](http://hardwarefun.com/tutorials/compiling-arduino-sketches-using-makefile)来逃避 IDE，现在已经成为一个成熟的、功能丰富的 Makefile，它已经随着 Arduino 的变化而发展和适应。Makefile 有 47 个贡献者组成的社区，通过在您选择的轻松的文本编辑器中编写代码，并在您的终端中编译一个简单的咒语 *make* ，Makefile 使您能够完全脱离 IDE，无论您使用的是 Linux、Mac 还是 Windows。

事不宜迟，让我们来看看这个项目的亮点。

### 神秘的快捷方式——走开！

对于许多初学者来说，编写(甚至编辑)一个 Makefile 可能会与大多数 Makefile 作者无耻的快捷键使用产生一些严重的混淆。毫无疑问，许多 Makefiles 的神秘语法形成了编译和链接可执行文件的简明指令列表，但是对于外行来说，这个方法似乎有点难以解析。此外，Makefiles 还容易抛出奇怪的错误(尾随空格有人知道吗？)是很难找到的——特别是当我们想把大部分时间花在开发嵌入式系统上，而不理解 Makefile 的机制和语法时。幸运的是[Sudar]和开发团队的其他成员已经把界面变得非常易读。

他们的解决方案是:由两部分组成的 Makefile。对于一个简单的项目，您的 Makefile 不需要长于以下代码片段(*灵感来自于* [*Makefile 示例* s](https://github.com/sudar/Arduino-Makefile/blob/master/examples/HelloWorld/Makefile) ):

```
BOARD_TAG    = uno
include $(ARDMK_DIR)/Arduino.mk
```

这个简短的 Makefile 中概述了特定于项目的设置(比如您使用的是哪种板),然后包含了更大的 Makefile，其中包含了构建代码的实际细节。这里假设您已经定义了两个环境变量，分别是 **ARDMK_DIR** 和 **ARDUINO_DIR** ，它们指向(1) Arduino Makefile 目录和(2) Arduino 安装目录。此外，如果您有额外的库，您可以在顶层 Makefile 中包含一行定义文件路径的代码。

```
 USER_LIB_PATH += /home/my_username/my_libraries_directory
```

您还需要将正在使用的所有库(包括用户添加的和内置的)添加到库列表中，如下所示:

```
ARDUINO_LIBS += Wire \
                SPI \
                my_custom_lib
```

“split-Makefile”设置的好处是，简短的顶级 Makefile 隐藏了编译和链接默认和用户添加的 Arduino 库时所涉及的复杂的编译器工作。另一方面，这个“迷你”Makefile 变成了一些次要细节的简短、信息丰富的摘要，比如正在使用哪些 Arduino 库，这可能与作者和未来的开发人员更相关。

### 原始 C 和 C++很流行——如果你喜欢这样的东西

厌倦了。ino 文件扩展名？厌倦了不得不约束自己进入那些**设置**和**循环**功能？有了 Makefile，您可以很快地摆脱这些，用原始 C 或 C++编写代码。如果你想在普通的 C 或 C++中工作，甚至可以忽略掉**# include<Arduino . h>**，完全忽略 Arduino 库。

也就是说，如果您混合使用 C 和 C++，请记住，您需要在 C 头文件周围插入保护，如下所示:

```
#ifdef __cplusplus
extern "C" {
#endif

/// the rest of my C header file 

#ifdef __cplusplus
}
#endif
```

### 添加项目库

Arduino Makefile 可能是我最喜欢的方面，它可以灵活地容纳更丰富的文件结构，并轻松地将您的项目分成多个文件。假设我有一个一次性的项目，其中包含一个自定义库是有意义的。考虑到 Makefile 的灵活性，您可以定义:

```
    USER_LIB_PATH+=.
    ARDUINO_LIBS += my_custom_library

```

并生成一个目录树，如下所示。

```
 ├── main.ino
 ├── Makefile
 ├── my_custom_library
 ├── my_custom_library.cpp
 └── my_custom_library.h
```

如果您需要更大的灵活性，您还可以将您的源代码拆分到几个目录中，将 Makefile 保存在代码的同一个目录中，就像一个“main”(在这种情况下， **main.ino** 定义了**设置**和**循环**。)为此，您的 Makefile 将具有:

```
    USER_LIB_PATH+=../libs
    ARDUINO_LIBS += my_custom_library
```

在您的项目 Makefile 中，您的目录结构将如下所示:

```
 ├── libs
 │   └── my_custom_library
 │     ├── my_custom_library.cpp
 │     └── my_custom_library.h
 └── src
  ├── main.ino
  └── Makefile

```

最后，我们不需要约束自己只编写 C++类来将项目分割成多个文件。因为我们实际上使用的是普通的 C++，所以你可以自由地将你的项目分成多个源代码(*。c，*。cpp，*。伊诺，*。pde)和报头(*。h，*。hpp)文件，它们与 Makefile 文件位于同一目录，Makefile 会将它们编译成一个可执行文件。

### 其他微也是公平的游戏

最后，Arduino-Makefile 还与许多其他微控制器和程序员兼容，而不仅仅是 Uno 上的 ATMEGA328P。简而言之，这个特性是对 AVRDUDE 特性的阐述，AVR dude 是一个用于下载和上传代码到各种 AVR 微控制器的程序。最后，但并非最不重要的是，它也非常兼容。

### 定义我们的标准

如果你想熟悉 Arduino-Makefile 的工作流程，可以快速浏览一下他们的[示例目录](https://github.com/sudar/Arduino-Makefile/tree/master/examples)，其中有许多不同的用例。你也可以看一下我几周前从[得到的](http://hackaday.com/2015/08/12/i2c-bus-splitting-with-a-more-professional-touch/)[I2C _ 解复用 _ 演示](https://github.com/Poofjunior/i2c_demultiplexing_demo)来源的另一个例子。最终，Arduino 凭借其庞大的库集合，使得项目原型开发速度更快。然而，对于更大的项目，我们不倾向于看到文件组织的任何标准实践来使项目更容易导航。这就是你进来的地方。有了 Makefile 的灵活性，您就拥有了一切:您一直想要的文本编辑器、单独的头文件和实现文件、一个干净的目录…现在是时候使用这个工具将您的工作流改进成一个值得与我们其他人分享的方法了。