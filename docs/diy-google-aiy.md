# 如何在没有工具包的情况下构建自己的谷歌 AIY

> 原文：<https://hackaday.com/2017/05/30/diy-google-aiy/>

谷歌的语音助手已经存在了一段时间，当亚马逊发布其 Alexa API 并将 PaaS 云代码移植到 Raspberry Pi 2 时，其他人跳上通往创客王国的快车只是时间问题。谷歌只是时髦地这么做了。

很少有人知道树莓 Pi 3 的谷歌助理 API 已经存在了一段时间，但当他们决定[在 2017 年 5 月的 MagPi 杂志上免费赠送一个工具包](http://hackaday.com/2017/05/04/google-aiy-artificial-intelligence-yourself/)时，他们给每个人都留下了印象。不幸的是，世界上有更多的制造者和黑客，而杂志的数量是有限的。

在这篇文章中，我为每个想和纸箱子说话的人设计了 DIY 版的 AIY 工具包。我仔细看看免费的工具包，把它拆开，放在一起，换成 DIY 魔法。为了更方便，我还设计了一个附件，你可以 3D 打印来完成工具包。让我们开始吧。

## 拆卸

![](img/775b8107386dea7116ac9cafb06e69e5.png)

感谢我在英国的朋友[Shabaz]寄给我一份 MagPi。“谷歌 AIY 项目语音工具包”(以下简称工具包)包含两个印刷电路板和一堆其他东西。这个声音帽看起来像一个节食中的声卡，它的组件数量非常有限。我将详细说明每个部分，并为其逐一绘制 KiCAD 示意图

### 伺服系统

 [![aiy-servos](img/8fcc3db0ddbd47d28e83c1050cd6a3a6.png "aiy-servos")](https://hackaday.com/2017/05/30/diy-google-aiy/aiy-servos/)  [![servos](img/ecf06f105c5fda08c1c9a3761b3c7e5d.png "servos")](https://hackaday.com/2017/05/30/diy-google-aiy/servos-2/) 

从左侧开始，有 6 组标有“伺服”的 3 针接头。使用 Raspberry Pi 3 的板载 PWM 模块可以实现预期的伺服控制。每组都有一个 GPIO 引脚、5V 和 GND 连接。GPIO 引脚不直接连接到 Raspberry Pi 3 的头部，而是通过 220 欧姆限流电阻(标有 R1-R6)连接。

### 电源

 [![aiy-power](img/89f4d405abb6125e488321d9b21292a4.png "aiy-power")](https://hackaday.com/2017/05/30/diy-google-aiy/aiy-power/)  [![power](img/96cae68ab5da9e4378c07053cc267c74.png "power")](https://hackaday.com/2017/05/30/diy-google-aiy/power-6/) 

这些器件的正南方是标有 Q5 和 Q6 的器件，我假设它们是电源选择电路的一部分。如果我错了，请纠正我，但这是我的估计。工作很简单，Q5 仅在来自 USB 端口的输入电压大于 5V 时开启。一个简单的比较器应该可以做到这一点，我使用 LM393 作为参考。

编辑:[Raivsr]指出，这可能相当于树莓 Pi 的“理想二极管”。

### 通信接口

“伺服”接头的北面是 J15 标记的 I2C，它直接连接到树莓 Pi 3 接头。这意味着这些不应连接到任何 5V 上拉电阻。它们没有在电路板上使用，但是我们将在后面详细讨论。紧挨着它的是 SPI 和 2 引脚 UART 接头。同样，这些电缆直接连接到主集管，仅用作分线点。

### DAC 和 EEPROM

 [![aiy-chips](img/c0aa4dab1baab399ea332c1d793106be.png "aiy-chips")](https://hackaday.com/2017/05/30/diy-google-aiy/aiy-chips/)  [![MAX98357A](img/14b4afd9b7bb39e4d6e72d5bcc65be7a.png "MAX98357A")](https://hackaday.com/2017/05/30/diy-google-aiy/max98357a/) 

再低一点，我们到达了标有“AKK·BDQ”的 16 针 QFN 的盒装电路。这是 Maxim MAX98357A( [PDF](https://datasheets.maximintegrated.com/en/ds/MAX98357A-MAX98357B.pdf) )，它是一款带有 D 类放大器的 I2S DAC。它直接驱动扬声器，但由于只有一个输出，它只能是单声道或组合立体声。对预算来说，这仍然是一个很大的挑战。

有趣的是 JP6 的出现，它似乎拥有 Maxim MAX98357A 和其他一些精选系列的所有 I2S 连接。结合连接第二个扬声器输出的两个过孔，您可以在顶部安装另一个 Maxim MAX98357A 分线板，以获得立体声。我要做原理图，并使它可以下载，如果你想尝试一下，让我知道结果。就当是可选作业吧。

DAC 旁边是一个 8 引脚 SSOP，它是一个 24C32 ( [PDF](http://www.st.com/content/ccc/resource/technical/document/datasheet/80/4e/8c/54/f2/63/4c/4a/CD00001012.pdf/files/CD00001012.pdf/jcr:content/translations/en.CD00001012.pdf) ) I2C EEPROM。它没有连接到我前面提到的 I2C 接头，而是连接到 Raspberry Pi 3 接头的 27 号和 28 号引脚。根据树莓派基金会的博客。

> “EEPROM 保存着主板制造商信息、GPIO 设置和一个叫做‘设备树’的片段——基本上是对连接硬件的描述，允许 Linux 自动加载所需的驱动程序。”

因此，它有一些额外的酱料，使事情滴答作响，我可以使用一个 BusPirate 转储数据，但我不确定谷歌是否认为这是知识产权，所以我不会。我也有一个替代方案，所以继续读下去。

### 司机

 [![aiy-drivers](img/627a701274ea03f297779b102376ca01.png "aiy-drivers")](https://hackaday.com/2017/05/30/diy-google-aiy/aiy-drivers-2/)  [![drivers](img/d895583890740be4fd822d79140e4bc8.png "drivers")](https://hackaday.com/2017/05/30/diy-google-aiy/drivers/) 

向右移动，我们发现 4 个标有“Drivers”的标题。这些是 MOSFET 电路，用于控制继电器等负载。[Shabaz]做了很好的工作来跟踪这个上的组件，3 个引脚是 GPIO、5V 和 Driver。

由于采用了 polyswitch，每个 MOSFETs 可以驱动高达 500mA 的负载，但 GPIOs 也可以直接使用。要驱动的负载应连接在标有“+”和“-”的引脚之间。左侧的接头引脚是从 Raspberry Pi 3 直接访问 GPIOs 接头引脚，原理图也是如此。

使用这些来连接 led 或类似设备，以指示继电器或负载的运行。

### 麦克风和按钮连接器

更有趣的事情发生在右边的右上角，有一个按钮和两个 JST 连接器。4 针连接器用于位于组装外壳顶部的按钮。安装在 PCB 上的小按钮与外部开关并联，在设置和测试时可以在它的位置上使用。5 针 JST 用于麦克风连接器，具有所有 I2S 针。

### 麦克风

 [![aiy-mic](img/0caf6eb463384e52ff7405e55896a228.png "aiy-mic")](https://hackaday.com/2017/05/30/diy-google-aiy/aiy-mic/)  [![mic](img/8a3a60cf8853820d7b7d19fd1cba73ae.png "mic")](https://hackaday.com/2017/05/30/diy-google-aiy/mic-5/) 

![](img/ccd9d07693886251998944810ea3b65d.png)最后，麦克风板标记为 432 QDF21G，配有 Knowles SPH0645LM4H MEMs 数字麦克风，可直接与 I2S 通话。

## 就是这样！

这大概就包括了拆卸和制作你自己的 AIY 工具包所需的所有信息。KiCAD 原理图文件可以从 [GitHub](https://github.com/inderpreet/DIY-AIY) 下载，但是我把有趣的部分留给你，那就是布局和布线。

这是一些值得思考的问题。某些部分可以省略，帽子的尺寸可以缩小到π零 pHat。

出于简单的原因，我使用来自谷歌 AIY 页面的预配置操作系统映像。它离 900MB 还差一点，可以直接从 Goolge ( [巨大文件](https://dl.google.com/dl/aiyprojects/voice/aiyprojects-latest.img.xz))下载。

## 添加关机按钮

你可能注意到了上图中绿色大按钮旁边的金色小按钮，这是练习的第一部分。这是一个关机按钮，添加它是因为我不想每次想安全关机时都 SSH 到这个框。

找到您想要使用的按钮，添加两根带母接头的电线。这一点，即使没有语音帽子的工作，所以请随意尝试。接下来，如果你有一个语音帽，添加男性头 I2C 部分。你可以选择任何其他引脚，它仍然会工作。将按钮连接到 SDA 或 GPIO 2，并启动 Pi 3。

打开您最喜欢的文本编辑器，将以下代码复制粘贴到其中。

```

#!/bin/python
# Simple script for shutting down the raspberry Pi at the press of a button.
# by Inderpreet Singh

import RPi.GPIO as GPIO
import time
import os

# Use the Broadcom SOC Pin numbers
# Setup the Pin with Internal pullups enabled and PIN in reading mode.
GPIO.setmode(GPIO.BCM)
GPIO.setup(02, GPIO.IN, pull_up_down = GPIO.PUD_UP)

# Our function on what to do when the button is pressed
def Shutdown(channel):
    os.system(&quot;sudo shutdown -h now&quot;)

# Add our function to execute when the button pressed event happens
GPIO.add_event_detect(02, GPIO.FALLING, callback = Shutdown, bouncetime = 2000)

# Now wait!
while 1:
    time.sleep(1)

```

将/home/pi 文件夹中的文件保存为 shutdown.py

在终端中键入以下命令

```
 chmod +x shutdown.py python shutdown.py &amp; 
```

这将使脚本在后台运行。如果您按下按钮，Pi 应立即关闭。您可以选择通过取消示例代码中休眠调用的注释来添加延迟。或者，您也可以通过替换 python 脚本中的适当数字来更改 GPIO。

酷！现在我们可以按下按钮关机。

## 添加 USB 声卡

谷歌 AIY 语音帽的明显替代方案是使用任何可从许多来源获得的 USB 声卡。最简单的方法是只插入一个，并配置软件来使用它而不是 hat，但当安装了两个驱动程序时，python 脚本需要重新配置以使一切无缝。

一旦你插上声卡，首先要做的就是检查它是否被识别。在终端窗口中，键入:

```
 aplay - l 
```

脚本使用‘播放’来朗读回复，因此您应该能够看到两个声音设备。请注意，板载声音已经在 config.txt ( [参见设备树参考](https://www.raspberrypi.org/documentation/configuration/device-tree.md))中被禁用，如果您计划使用 USB 麦克风而不是声卡，可以启用板载声音。windows 输出应该如下图所示。

我想将 USB 声卡设置为默认音频，为此我们需要修改/etc/asound.conf。

```

sudo nano /etc/asound.conf

```

![](img/1fce732481faf4222249d049b628b253.png)

删除现有内容，并替换为如下所示的文本。虽然这将默认的输入和输出设备设置为 USB 设备，但是还需要一个步骤来使其工作。(要退出 nano，请使用 Ctrl+x，y，return)

接下来，我们编辑 audio.py 文件，该文件处理所有音频播放和录制功能。为此，在你最喜欢的文本编辑器中打开文件；我的是纳米:

```
 sudo nano /home/pi/voice-recognizer-raspi/src/audio.py 
```

向下滚动到 __init__ 函数中显示“arecord”的部分。显然，有一个专门的过程来保持录像机运行，正如我将在视频中展示的那样。现在，我们想要编辑参数，以便它使用 USB 卡来捕获音频，而不是原来的语音帽。使用'-D '，' sysdefault:CARD=1 '的简单修改应该足够了，如下图所示。

![](img/5a8b36771f189d5049f5b9e7bde7922d.png)

在代码中，需要对 aplay 函数进行类似的修改。

![](img/9be4355e8b0143b3dac63682b96a4cd9.png)

至此，黑客攻击完成了！双击“test_audio.py ”,检查音频是否正常。但是我们只缺少了拼图的一部分——“听”按钮！因此，只需在 GPIO23 和相邻的接地引脚之间连接一个按钮，然后运行“src/main.py ”,就可以开始玩 DIY 谷歌 AIY 了。

### 演示

一个小的视频演示提议的黑客与 USB 声卡，外部扬声器和廉价的麦克风。

 [https://www.youtube.com/embed/2GDVqWCrzmM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2GDVqWCrzmM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 一个围栏

3D 打印外壳是在 Fusion360 中设计的，STL 文件是 GitHub 资源库的一部分。您可以在多个项目中使用同一个外壳，因为 Raspberry Pi 有支架，而且为了方便起见，端口也去掉了。里面有很多空间可以添加帽子和额外的电路。

我将机箱从中间分开，这样就很容易接触到 GPIOs。整个东西会压配合，包括有三个按钮孔的顶盖。我认为有更小的按钮是有意义的，因为结果预计会比纸板更坚硬。如果你选择加入一个稍有不同的话题，会有足够的空间给演讲者。

我还没有机会打印出来，一旦这个话题有任何进展，我会更新这个页面。这是设计的效果图。

![](img/f795b0b3a9ca97a645769a3e5827e41a.png)

## 摘要

Google 已经向公众开放了他们的 API，但是预配置的 Raspbian 映像将帮助很多人开始使用。我已经试着设计了声卡的基本原理，并且给出了一个等效的声卡的设计方案，如果你想做一个的话。对于其他人来说，使用外部声卡的选项得到了解释和演示，我希望它能激励人们真正进入这样的项目。这个世界需要更多的 AIY，这是你开始的机会，所以你还在等什么？开始黑吧。