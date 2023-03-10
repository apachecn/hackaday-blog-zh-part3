# 如何开始使用 ESP32

> 原文：<https://hackaday.com/2016/10/04/how-to-get-started-with-the-esp32/>

ESP32 是最热门的新无线芯片，提供 WiFi 和蓝牙低能耗无线电，配备双核 32 位处理器，并配有各种外设。我们得到了一些评估样片开发板， [Adafruit](https://www.adafruit.com/product/3269) 和 [Seeed Studio](https://www.seeedstudio.com/ESP3212-Wifi-Bluetooth-Combo-Module-p-2706.html) 有一段时间都有库存，AI-Thinker——制造最受欢迎的 ESP8266 模块的公司——将于 10 月 1 日开始全面生产。这意味着你们中的一些人现在就有了新的热点，而其余的人不用再等几个星期了。

正如我们在新芯片的第一次审查中所说，软件方面的许多事情都处于不断变化的状态，但编写、编译和刷新芯片代码的基本过程将保持稳定。是时候开始一些教程了！

## 概观

ESP32 模块预装了一个带有 AT 命令集的 ROM 映像，就像 ESP8266 一样。如果你想浪费这个芯片 95%的潜力，把它当作一个美化了的串行到 WiFi 调制解调器，你已经准备好了！但你们都想吃，对吧？对！

用 C 编写 ESP32 的工具链非常简单。您将需要 Espressif 的软件库(`esp-idf),`)、特定于芯片的交叉编译器和构建工具(`xtensa-esp32-*)`)，以及将生成的二进制文件闪存到设备的实用程序。我将引导您这样想，然后我们将编译并刷新 Espressif 的演示应用程序，此时一切都已启动并运行。

## 组装工具链

[![esp32-repo](img/d68d64c7e0e176b7b03d44f315d20131.png)](https://hackaday.com/wp-content/uploads/2016/10/esp32-repo.png) 你的第一站是 [Espressif 物联网开发框架(`esp-idf` ) GitHub](https://github.com/espressif/esp-idf) 。我们强烈建议将存储库克隆到您的本地计算机上，因为它经常更新，并且您希望保持它最新。下面是在我的 Linux 机器上运行的命令。

`git clone --recursive [https://github.com/espressif/esp-idf.git](https://github.com/espressif/esp-idf.git)`

请注意`recursive`选项，它下拉框架所依赖的所有子模块:在这种情况下，`components/esp32/lib`和`components/bt/lib`中的一些二进制 blob 库，以及将为我们实际刷新芯片的`esptool.py`程序。

如果你只是从 GitHub 下载 zip 文件，它会缺少这些重要的部分。由于子模块的原因，您还需要分两步来保持所有内容都是最新的。`git pull`用于顶层，`git submodule update --recursive`更新所有子模块。

现在开始获取交叉编译器工具链。在`docs`里面有你特定操作系统的说明。对于 [Linux](https://github.com/espressif/esp-idf/blob/master/docs/linux-setup.rst) 、 [MacOS](https://github.com/espressif/esp-idf/blob/master/docs/macos-setup.rst) 和 [Windows](https://github.com/espressif/esp-idf/blob/master/docs/windows-setup.rst) 来说，启动和运行的最快方法是从安装文件中列出的位置下载二进制 blob。对于 Windows 来说尤其如此，Espressif 的优秀人员已经预先打包了您将需要的所有命令行工具。下载工具链 zip 文件，解压，就差不多了。

### 环境变量，第一部分

计算机需要知道你把交叉编译器组件存储在哪里，不管你用的是哪种操作系统，你都必须告诉它。(现在是 2016 年:我的操作系统不能简单地找到并运行请求的程序吗？！)在 Linux 和 Mac 上，`export PATH=$PATH:/path/to/esp/xtensa-esp32-elf/bin`将起作用，其中`/path/to/esp`是您解压缩交叉编译器二进制文件的位置。在 Windows 上，你可以通过将`export IDF_PATH="C:/path/to/esp-idf`写入一个名为`C:/msys32/etc/profile.d/esp-path`的文件来永久设置路径，或者在每次运行`C:\msys32\msys2_shell.cmd`时输入相同的导出命令。

## 编码，闪烁，你好世界！

此时，您应该将所有的工具链片段放在一起。是时候检查一下[模板应用](https://github.com/espressif/esp-idf-template) : `git clone [https://github.com/espressif/esp-idf-template](https://github.com/espressif/esp-idf-template)`了。现在只需打开一个终端，`cd`进入应用程序的目录并输入`make`。什么都没发生。

### 环境变量，第二部分

没错，更多路径。示例应用程序中的 makefile 需要知道主 makefile 框架(在`esp-idf`中)的位置。模板应用程序附带的文档建议定义一个环境变量:`export IDF_PATH=/path/to/esp-idf`。在这一点上，所有系统都是一样的。您可能希望编写一个 shell 脚本或批处理文件来完成这项工作，并将它包含在您的项目中。

### Menuconfig

[![esp32-menuconfig](img/93b59e8abdc68955c437ba0ae29b71c9.png)](https://hackaday.com/wp-content/uploads/2016/10/esp32-menuconfig.png)IDF 的一个非常棒的功能就是菜单驱动的配置。在我们审查 ESP32 芯片时，菜单选项已经发生了变化，随着更多功能的实现，我们确信它将继续变化。然而，在这里您可以控制许多特定于平台的设置:使用哪个 TTY 或 COM 端口、波特率、希望 ESP32 内核运行的速度等。注意“串行闪光器配置”,至少浏览“组件配置”。

因为这是一个移动的目标，我们不能给你太多在一两周内仍然有效的建议。你只需要仔细检查每一个菜单项，确保它与你的系统相匹配。当您点击“保存”选项时，此配置的结果将存储在一个`sdkconfig`文件中。如果你不想从头再来一遍菜单，你可以在不同的项目间拷贝这个。

### 还有一点

现在你差不多准备好了。如果你现在刷新演示应用，它将无法在没有你的凭据的情况下连接到你的 WiFi 网络。打开`main/main.c`，找到“SSID”和“密码”字段，输入您家庭网络的详细信息。由于这只是对工具链的测试，所以是可选的，但知道 ESP32 可以上线感觉很好。

### 闪烁芯片

[![763sd4c5rglqwhctcxn88s7qg](img/e9958aadf99230a3d5ad669c4cde377d.png)](https://asciinema.org/a/763sd4c5rglqwhctcxn88s7qg) 配置完成后，你就可以连接串口并刷新程序了。要将芯片置于引导模式，需要将引导模式引脚`GPIO0`接地，同时将使能引脚`EN`接地并释放。如果您在运行终端应用程序的情况下这样做，您会看到打出“等待下载”。关闭你的终端程序，输入`make flash`，然后重新打开终端程序，你应该会看到很多调试信息，因为它试图连接到你的 WiFi。

现在你进入了编码、刷新和调试的循环。当然，演示应用程序并不真正*做任何事情*。关键是，如果你已经做到这一步，你可以在设备上编译、刷新和运行代码。这是第一步！

## 概述

起床跑步很“容易”。用`esp-idf`库克隆存储库，下载并解压缩二进制工具链，克隆模板应用程序。您必须定义两个环境变量:一个是工具链二进制文件的路径，另一个是库的位置。在模板应用程序中运行`make menuconfig`和`make flash`，您应该可以开始比赛了。

如果你在 Linux 系统上，[这里有一个安装脚本](https://gist.github.com/hexagon5un/cd8a86c32d0da45e2ae214c24957180a)，它可以完成本教程中提到的所有事情。创建一个你想安装所有东西的目录，把这个文件复制到那里，输入`. getESP32.sh`然后看着它走。如果你以前安装过，它会从 GitHub 下载所有东西的最新版本，并为你重新定义环境变量。即使你不想使用它或有一个奇怪的设置，通读它是一个方便的清单，以确保你已经得到了一切。如果对您不起作用，请告诉我，我们会解决它。

请注意，虽然这听起来工作量很大，但这都是一次性的设置成本。对于您的下一个程序，您只需复制演示应用程序文件夹，进入`main/main.c`并开始编码。根据您的配置，您可能需要再次设置这两个环境变量(创建一个脚本/批处理文件！)但也就这样了。

关于编码这个话题，让双核微控制器与实时操作系统一起运行有着不小的魔力。如果你从未这样做过，那么升级到 ESP32 将会是一段学习经历。下一次我们将介绍 FreeRTOS 及其应用于 ESP32 的一些编程约定。请继续关注，如果你想尝试一下，或者想看看其他的，请在评论中告诉我们。