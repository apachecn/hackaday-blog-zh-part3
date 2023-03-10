# 编译一个 22 美元的逻辑分析仪

> 原文：<https://hackaday.com/2016/12/13/compiling-a-22-analyzer/>

在我参加今年的 Hackaday 超级大会的路上，我在 EE Times 上看到了一篇文章，内容是有人拿走了 22 美元的格子冰棍，并把它变成了一个逻辑分析仪，配有一个 Python 应用程序来显示波形。鉴于棒上真的没有一吨 RAM，基本上没有不包含在 FPGA 本身中的，这对我来说非常酷。

[Jenny List]也写了关于 Black Mesa Labs 的[Kevin Hubbard]开发的这个应用程序的文章，并且[Al Williams]在[发表了一组关于使用同样的 22 美元评估板的文章](http://hackaday.com/2015/08/19/learning-verilog-on-a-25-fpga-part-i/)，使用开源工具进行 Verilog 设计。即使你最终没有把 stick 作为一个逻辑分析器来使用，也很容易找到许多其他项目，你可以在那里重新编译，为它发明一个新的用途。

 [https://www.youtube.com/embed/I30fCF4bWes?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I30fCF4bWes?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 关于棍子

Lattice iCEstick 是一个小型 FPGA 评估 PCB，只有一点点支持电路；基本上只有 FPGA、一个时钟、一些 SPI 闪存和一个 USB 接口。还有一些连接器和引脚垫以及一个红外收发器，以获取组件上和组件外的信号。

[![ice](img/fe35a599bcef2a02e21456cfe21e0d8b.png)](https://hackaday.com/wp-content/uploads/2016/11/ice.png)

FPGA 本身是一个 iCE40HX1K，其中有 160 个逻辑模块和高达 8 kb 的 RAM，对我来说这听起来像是一个中小型设备，但是由于 FPGA 架构不同，我真的不能确定，除非我加载一些我过去使用的旧设计进行比较。

## 关于水坑

我一直在看[原来的 SUMP.org](https://www.sump.org/projects/analyzer/)[分析仪](https://www.sump.org/projects/analyzer/)，以便在我无聊时放入我制作的一个小定制 FPGA 板。我认为逻辑分析仪应用程序是一个 RAM 泵(循环缓冲控制器),一边是 UART，另一边是许多 I/O 线。一般来说，在任何特定时钟频率下需要捕获的时间量直接转化为所需的 RAM 量。如果将 FPGA 用于严肃的工作，保护 FPGA 免受恶劣环境以及目标系统中工作电压的影响也很重要。

## SUMP2

[Kevin]将他的设计称为 SUMP2，这是有充分理由的，因为它与最初的污水坑架构有些不同。SUMP2 利用一种称为[游程编码](https://en.wikipedia.org/wiki/Run-length_encoding) (RLE)的简单无损压缩方案，它不是连续发送大量的 0 或 1，而是发送一个位值以及在下一次转换到不同的位状态之前重复该值多少次。SUMP2 设计压缩数据不仅是为了将数据发送到控制计算机，也是为了将其存储在 iCE40 有限的 RAM 中。这也意味着，决定存储多少数据的不一定是时间量(或采样时钟数)，而是记录的转换次数。

## RLE

从框图中可以看出，该架构还支持非 RLE 编码的数据采样，如左下角名为“dwords”的信号所示。

[![rle](img/c287cbf8d714171e485a0794566819be.png)](https://hackaday.com/wp-content/uploads/2016/11/rle.png)

在 [Lattice 网站](http://www.latticesemi.com/programmer)上有一个程序员可以免费给冰棍编程，比特文件可以从 [Black Mesa Labs 网站](https://blackmesalabs.wordpress.com/)上下载。

为了获得更多的实践经验，我建议下载整个项目，然后从 Lattice 下载免费的 FPGA 设计软件 [iCEcube2，尽管它们确实要求用户提交其计算机的 MAC 地址，以获得运行软件的许可证密钥。](http://www.latticesemi.com/en/Products/DesignSoftwareAndIP/FPGAandLDS/iCEcube2.aspx)

在视频中，我一步一步地加载项目和所有的步骤，直到编译 RTL 代码和编程的 FPGA。这是我的说法，我不会重复所有的步骤。

另一部分是 Python GUI，它由两个模块组成，一个是名为 bd_server.py 的服务器模块，它驻留在 TCP 端口上并与 USB 接口，另一个是作为 pygame 应用程序运行的核心 sump.py 模块。在运行应用程序之前，需要加载几个模块(这些都包含在安装说明中)，即 pyserial 和 pygame。我使用了以下命令(我不是 Python 的人，你可能有更有见地或更高效的 l 方式):

```
“python -m pip install -U pip setuptools”
“python -m pip install -U pip pyserial”
“python -m pip install -U pip wheel”
“python -m pip install -U pip Pygame”
```

但是等等，没那么简单，说明(和视频)引导用户在 Lattice 设备驱动的 USB B 端口上设置 VCP。如果你成功了，你将获得虚拟 COM 端口的价值。

## 图形用户界面

接下来要做的就是从 Windows CMD 提示符“start bd_server.py”运行 bd_server app。第一次可能会失败，但会留下一个配置文件“bd_server.ini ”,在该文件中可以编辑 COM 端口和的设置。将“AUTO”改为正确的 COM 端口似乎是一个常见的要求。第二次运行该应用程序时，会出现一条“5 乘 5”的消息，表明它运行正常。

运行 SUMP 应用程序本身“start sump.py”弹出一个窗口，分析器以其所有绿色管状的荣耀出现(我把我的改成了紫色，如下所示…或者叫紫色？) [![waveform](img/618e0e060e51ffc9324f477c86712021.png)](https://hackaday.com/wp-content/uploads/2016/11/waveform.jpg)

从这里开始，你可以自由地开始分析和修改，如果你有兴趣的话。对我来说，我在 sump.py 中找到了一行，并取消了对它的注释，这样菜单就提供了一种直接的方法来使事情变得更大，这样我的老眼睛就可以实际看到我正在看的东西(原来“home”和“end”总是可以扩大行高，但我只从阅读代码中知道这一点。

需要注意的是，这里使用的 FPGA 只能承受 3.3V 电压，[Kevin]在 Osh park 有一个公共域 PCB，用于转换为 5V 电压。

## 菲尼

如果你非常需要一个逻辑分析仪，使用一个严肃的分析仪，但是如果你想花最少的钱和/或喜欢开源的东西，看看这个。