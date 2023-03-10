# ESP8266 上的 MicroPython:踢轮胎

> 原文：<https://hackaday.com/2016/07/21/micropython-on-the-esp8266-kicking-the-tires/>

脚本语言是用于大型计算机的，对吗？“真正的”嵌入式设备工作是一个地狱般的、永无止境的编码、编译和刷新循环。嗯，我过去也是这样认为的，但是随着脚本和其他交互式语言在过去几年中向微控制器的扩散，在小芯片上进行交互式开发的障碍已经降低了很多。

在 ESP8266 平台上，我试用过 [NodeMCU 的 Lua](http://hackaday.com/2016/05/17/minimal-mqtt-networked-nodes/) 和 [ESP8266 BASIC](http://hackaday.com/2015/08/29/basically-its-an-esp8266/) 。(在过去的半年里，我几乎只在 STM32F1xx 和 F4xx 芯片上使用了令人敬畏的 [Mecrisp-Stellaris](http://mecrisp.sourceforge.net/) ，但还没有接触过[ESP8266 fouth](https://github.com/CraigLindley/ESP8266Forth)。)

NodeMCU 非常棒，因为它内置了您想要的一切，并且通过[云服务](http://nodemcu-build.com/)可以轻松地定制版本，最大限度地为您的项目提供免费闪存。我只是不喜欢异步 Lua 的东西(你可以试试！).ESP BASIC 有一组不同的库，对于我来说缺少 MQTT。尽管如此，它还是很漂亮，值得一看。

所以当 MicroPython 的人宣布他们将发布 ESP 的二进制版本时，我认为是时候让它旋转一下了。我现在用 Python 已经快十二年了，所以它对我来说就像一只舒适的鞋子。ESP8266 上的 MicroPython 会是同样的吗？简单的回答是有也没有。

## 装置

安装再简单不过了，多亏了 MicroPython 的人[几天前发布了二进制文件](http://hackaday.com/2016/07/11/micropython-binaries-for-the-esp8266-to-be-released/)(特别感谢 Kickstarter 的支持者！).

只需[下载 ESP8266 二进制映像](https://micropython.org/download/)并将其闪存到芯片中。我用的是一直流行的 [esptool.py](https://github.com/themadinventor/esptool) ，意思是输入`esptool.py -p /dev/ttyUSB0 write_flash 0x0000000 esp8266-*.bin`就搞定了。几分钟后，我重置了 ESP，得到了一个串口。以 115，200 波特的速度连接它会出现一个 Python 提示符。

```

&gt;&gt;&gt; print(&quot;hello world&quot;)
hello world

```

那很容易。

## 安顿下来

如果你将 Python 代码输入到基于文本的东西中，比如 [iPython](http://ipython.org/) 或类似的东西，你会发现自己就在家里。MicroPython 的人确实在用户体验方面做对了:tab 键补全带来了一个对象的方法，上箭头键调出了最后一个编辑命令，等等。control-e 的一个优点是允许你一次粘贴一个文件中的整个代码块。简而言之，这是一个完全托管在 ESP8266 之外的很好的可工作的 Python 环境。太棒了。

物流控制住了，就该找教程了。MicroPython 网站上的[官方教程](https://docs.micropython.org/en/latest/esp8266/esp8266/tutorial/index.html)棒极了。如果您已经了解 Python，您将在半小时内熟悉 ESP8266 MicroPython。

## MicroPython 和 ESP8266 扩展

在串行终端上打印“hello world”很好，但是闪烁的 LED 微控制器组的“hello world”——怎么办？有一个可以导入的`machine`模块，它有一个`Pin`对象。

```

import machine
p = machine.Pin(2, machine.Pin.OUT)
p.low()
p.high()
# or
p.value(not p.value()) # toggles

```

如果你没有体验过微控制器上的交互环境，那么输入一个命令并得到即时响应会很酷。但是从长远来看，能够动态测试代码所带来的生产率提高会让你着迷。

另一个突出之处是可以轻松将 ESP8266 置于睡眠状态，例如，如果您试图使用电池，这是绝对必要的。休眠十秒钟——以微秒计。不要忘记将`WAKE`引脚 GPIO 16 连接到 reset 引脚。

### 网络和网络

但是你用 ESP8266 是因为你想要 WiFi，对吧？这就是`network`模块发挥作用的地方。您可以阅读文档了解更多细节，但是设置非常简单

```

import network
n = network.WLAN(network.STA_IF)
n.active(True)
n.connect('&lt;your ESSID&gt;', '&lt;your password&gt;')
# n.isconnected()
# n.ifconfig()

```

一旦网络建立起来，你就可以做网络上的事情了(一分钟后会有更多的介绍)。这个教程让你很快就能看完 [ASCII 码的星球大战](http://www.asciimation.co.nz/)。我不得不使用 ctrl-e 特性并一次粘贴所有命令来使它工作。谁会是第一个在独立设备的 LCD 屏幕上显示这个的人？

虽然它没有在文档中提到这一点，但这些设置似乎藏在 flash 的某个地方。每次我插上电源，ESP8266 就会出现在我的 WiFi 网络上。很好。

### 失望来袭！

我第一次真正失望是在研究`os`模块时——对于像我正在使用的这种小内存 ESP8266，没有足够的空间来存储文件系统。`os.listdir()`返回`OSError: [Errno 19] ENODEV`。查阅网站，您不能在 ESP8266 上内部保存和加载文件，除非该模块具有 1M 或更高的闪存。对于超级便宜的 ESP8266 设备，如 ESP-01 ~~甚至是我正在使用的 [Wemos D1](http://www.wemos.cc/) ，~~这是一个节目停止器。没有在设备上保存用户代码的能力，它只是一个玩具。如果您想将代码保存到模块中，请获取一个具有更多闪存的新模块。

(编辑:我得到的文件系统错误似乎*而不是*与闪存大小有关。将`--flash_size=32m`选项添加到`esptool`命令中，在全新的 Wemos D1 Mini 上创建了一个工作文件系统，但是在之前使用的几个类似单元上失败了。这里的安装有一些小故障，但它可能会得到解决。对我关于文件系统的抱怨要有所保留。)

接下来，我研究了包含哪些 HTML 解析和 web 服务器模块。没有。值得称赞的是，MicroPython 团队的`socket`模块是桌面 Python 版本的一个很好的副本，您可以用几行代码得到一个非常简单的 web 服务器，但是这比我想要键入的代码多了几行。我现在使用 Python 的一半原因是为了像 [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) 、 [lxml](http://lxml.de/) 或[请求](https://pypi.python.org/pypi/requests)这样的事情。也没有内置 MQTT 客户端，这些天我所有的 ESP8266 设备都需要使用 MQTT。

手头没有这些工具，面对手工完成所有低级的 HTML 工作，我流了一滴眼泪。ESP8266 MicroPython 到此结束了吗？

### 情感过山车

然后我找到了 [micropython-lib](https://github.com/micropython/micropython-lib) 。这就是人们在 MicroPython 库上工作的地方，如果不是特别受限制的 ESP8266 端口，一般来说就是将这些功能带到 MicroPython 平台上。所以使用手头的库来做 HTML 繁重的工作应该不会太难。MQTT 支持正在上[工作，最近刚刚合并到主 micropython-lib 库中。](https://github.com/micropython/micropython/issues/2055)

有了一个比我的闪存更多的 ESP，你可以很容易地在你的程序中添加一些这样的模块，你将几乎进入嵌入式天堂。鉴于所有模块都是用 Python(一种有限的方言)编写的，它们很容易阅读、维护和扩展。我对社区将采取的措施抱有很高的期望。

还有*和*许多内置的酷模块:例如，SPI、I2C、OneWire、NeoPixel、定时器、PWM 和伺服库。利用内置的功能，您可以非常轻松地做很多事情。

## 结论和代码

~~面对一个闪存空间太小、无法做任何超级花哨事情的 ESP8266 模块，~~我决定用我现有的东西尝试最后一招。NeoPixel / WS2812B 驱动程序支持是内置的，它有插座支持，这意味着:联网的彩色闪光灯。如果你以前从未建立过 TCP 套接字连接，你可能会惊讶于它的简单程度。

首先，一些服务器端代码:

```

import socket
def server_init():
    s = socket.socket()
    s.bind( ('', 31337) )
    s.listen(1)
    c, a = s.accept()
    print &quot;Client connected&quot;
    return c

c = server_init()
c.send(&quot;\x10\x2A\x0F&quot;)

```

`server_init()`创建一个套接字，将其绑定到给定端口的任何 IP 地址，监听一个连接，然后在`s.accept()`状态等待客户端连接，此时它返回一个客户端对象，该对象可以向另一端发送或接收任意数据。发送的数据使用 Python 的十六进制字节的标准字符串编码，前缀为`\x`。如果您想以十进制形式输入相同的数字，也可以使用`chr(16) + chr(42) + chr(15)`。

在 ESP8266 上，因为都是用 Python 写的，所以代码都差不多。事实上，相同的基本代码可以在两台运行 vanilla Python 的计算机之间运行，就像运行 MicroPython 的 ESP8266 一样。

```

import socket
import neopixel
import machine

def connect():
    s = socket.socket()
    s.connect( ('192.168.178.25', 31337) )
    return(s)

def remoteRGB(s):
    n = neopixel.NeoPixel(machine.Pin(2), 1)
    n[0] = s.recv(3)
    n.write()

s = connect()
while True:
    remoteRGB(s)

```

连接到套接字连接比创建服务器简单。客户端要做的就是连接。然后，`remoteRGB()`函数监听三个字节，并相应地设置 LED 的颜色。只要任何一方都没有关闭连接，通过 WiFi 的任何三个字节都将被数字解释并馈送到 WS2812。如果你有现成的零件，试试看。

### 包含(部分)电池

总之，ESP8266 上的 MicroPython 是一个大杂烩。能够实时键入代码并观看 led 灯亮起真是太棒了。当您在做一些更复杂的事情时，比如通过 SPI 与外设对话，交互调试的便利性会让人上瘾。有了一个大型社区的支持，并且考虑到在 Python 中开发和移植模块是多么简单，我可以预见这个项目会迅速扩大，而且不仅仅是在 ESP8266 上。

但是按照 ESP8266 的标准，MicroPython 是一个内存猪。因为我使用了 el-cheapo 模块，我甚至没有足够的闪存来测试文件系统和充分利用可用的库。即使有更大的一部分，很明显，ESP8266 MicroPython 的开发人员正在推动可能性的极限，他们肯定会在未来遇到更多的内存(RAM 和 flash)限制。

在大型计算机上使用 Python 的乐趣之一是“包含电池”的理念，即任何时候都可以将您想要的所有模块放在手边(或容易安装)，而这在 ESP8266 上是行不通的。在用户代码的空间和库及模块的空间之间总会有一个折衷。

当然，在更大的芯片上，这些权衡会不那么痛苦，但由于 WiFi，ESP8266 是不可能忽视的。就个人而言，如果 MQTT 支持在主线二进制发行版中，我会立即从 NodeMCU/Lua 切换到 MicroPython 进行 ESP8266 开发。就目前情况而言，我将继续关注这个项目，并购买一些带更多闪存的 ESP8266。