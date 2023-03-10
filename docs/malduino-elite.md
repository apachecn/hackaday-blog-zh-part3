# 马尔杜伊诺精英——第一印象

> 原文：<https://hackaday.com/2017/05/31/malduino-elite/>

不久前，我写了一篇关于 Malduino 的文章，这是一款基于 Arduino 的开源 BadUSB 设备。我发现这个项目很有趣，所以我注册了一个精英版，果然，友好的邮递员上周五把它放在了我的邮箱里，这意味着我整个周末都可以玩它。对于那些错过这篇文章的人来说，Malduino 是一个 USB 设备，它能够模拟键盘和输入击键，以及其他功能。在合适的外壳中，它看起来就像一个 u 盘。就像你在电影中看到的那样，一个人插上一个设备，它就自动入侵电脑。它有两个版本，Lite 和 Elite，都基于 ATmega32U4。

Lite 版本非常小，除了 USB 连接器之外，它只包含一个开关，允许用户在运行和编程模式之间进行选择，以及一个 LED，指示脚本何时完成运行。

![](img/0b029fa6b93219f9fa86d67ead8fb1c6.png)

Original Malduino Elite sketch and Lite prototype

精英版更大，配有一个微型 SD 卡读卡器和四个 DIP 开关，允许用户选择从卡上运行哪个脚本。它还有一个 LED 指示灯，用于指示脚本何时结束运行。这允许用户只刻录一次固件，然后对存储在 Micro-SD 卡中的击键注入脚本进行编程，相比之下，每次用户想要运行不同的脚本时，都需要刷新精简版。

这是两个 Malduinos，因为它们是直接从 Arduino IDE 编程的，所以我刚才提到的每个功能都可以重新编程、重新调整用途或一起删除。你可以买一个，选择像“普通”Arduino 一样使用它，尽管没有太多的引脚可供使用。这种自由是我最喜欢的事情之一，实际上驱使我参加了众筹活动。请继续阅读全文。

## 硬件

![](img/b8021c1b52576d9610f828044965a64f.png)

Malduino Elite vs USB flash drive

因此，精英董事会如期而至，我发现自己有时间去看看它。尽管比 Lite 版本长，但它仍然很小，尺寸大约为 4.6 厘米 x 1.1 厘米(约 1.8 英寸 x 0.43 英寸)，你可以很容易地适应旧的 USB 外壳，尽管你必须为 DIP 开关和 Micro-SD 卡切割一些孔。在众筹活动中，最初的草图是 3 个 DIP 开关版本，但最终的 Elite 有 4 个，我觉得很好。我把它插在一台旧电脑上，在考虑了它可以安装哪种固件以及它可以对我的笔记本电脑做什么之后，果然一个红色的 LED 出现了。就这样。没别的了。

在摆弄了开关并进行一些 RTFM 之后，我意识到它附带的固件可能是某种针对 dips 的 Q.C .测试，这使得 Malduino 输出数字 1 到 4(实际上模拟按键 1 到 4)，这取决于哪些开关是打开的。到目前为止还不错，它的工作，我见过比这更糟糕的 PCB 板。板有六个引脚的孔，我没有跟踪到微控制器，我不知道他们是什么。

## 设置

设置 Malduino 要求您安装了 Arduino IDE 并且是最新的。您需要打开电路板管理器并安装 [Sparkfun 电路板](https://raw.githubusercontent.com/sparkfun/Arduino_Boards/master/IDE_Board_Manager/package_sparkfun_index.json)，因为 Elite 被编程为以 3.3 V 和 8 MHz 运行的“Sparkfun Pro Micro”。然后你需要去 [Malduino 脚本转换器](https://malduino.com/converter/)网站，它有几个用途:

*   它允许在精简版和精英版之间转换脚本
*   它允许你选择你的键盘布局语言
*   它会自动生成 Arduino 项目供您导入到 IDE 中

对于精英版，只需创建一个简单甚至空的脚本来下载项目，因为在“正常”操作中，您只需刷新 Malduino 一次，然后使用 Micro-SD 卡来存储新的脚本。

关于闪存的一个注意事项，如果你使用的是基于 Debian 的发行版，你可能会像我一样遇到一些问题，并且不能刷新设备。像这篇[最有用帖子](https://forum.sparkfun.com/viewtopic.php?f=14&t=37680)上的用户一样，我的调制解调器管理器在每次重置后都试图与 Malduino 对话，而*把 AVRDUDE 搞得晕头转向。*解决方法是在“/etc/udev/rules . d/77-mm-USB-device-black list-local . rules”中添加 udev 规则，为【socrim】致敬:

```
ACTION!=&quot;add|change&quot;, GOTO=&quot;mm_usb_device_blacklist_local_end&quot;
SUBSYSTEM!=&quot;usb&quot;, GOTO=&quot;mm_usb_device_blacklist_local_end&quot;
ENV{DEVTYPE}!=&quot;usb_device&quot;, GOTO=&quot;mm_usb_device_blacklist_local_end&quot;

ATTRS{idVendor}==&quot;1b4f&quot; ATTRS{idProduct}==&quot;9204&quot;, ENV{ID_MM_DEVICE_IGNORE}=&quot;1&quot;
ATTRS{idVendor}==&quot;1b4f&quot; ATTRS{idProduct}==&quot;9203&quot;, ENV{ID_MM_DEVICE_IGNORE}=&quot;1&quot;

LABEL=&quot;mm_usb_device_blacklist_local_end&quot;
```

## 软件

因为我运行的是 Linux，所以运行命令的快捷方式是 ALT-F2 组合键。所以我将它编写成一个文件，并保存到`1111.txt`。Elite 在微型 SD 卡中搜索对应于当前 dip 开关状态的文件。假设 dip 开关 2 和 4 打开。在这种情况下，软件试图找到名为`0101.txt`的文件并解析其内容(如 dip 开关顺序 1，2，3，4，而不是数字 2 和 4 的二进制表示)。完成后，红色 LED 开始快速闪烁。我的简单脚本是:

```
DELAY 2000
ALT F2
DELAY 1000
STRING xterm
DELAY 1000
ENTER
DELAY 1000
STRING id
DELAY 1000
ENTER
```

但是它不起作用。几乎所有的命令都工作正常，但是 ALT-F2 组合键不能正常工作。很接近，但没有雪茄。没有 ALT-F2，没有运行命令窗口。我已经偷懒浏览了一点源代码，因为我真的没有太多的时间，但我需要解决这个问题。令人不快的代码是这样的:

```
else if(equals(s,e,&quot;F1&quot;,3)) Keyboard.press(KEY_F1);&lt;/pre&gt;

else if(equals(s,e,&quot;F2&quot;,3)) Keyboard.press(KEY_F2);
...
else if(equals(s,e,&quot;F10&quot;,3)) Keyboard.press(KEY_F10);
else if(equals(s,e,&quot;F11&quot;,3)) Keyboard.press(KEY_F11);
```

一个自定义的*等于*函数接收功能键字符串的大小为 3，比如“F2”。对“F10”、“F11”和“F12”来说还可以，但对其余的键来说就不行了。将 3 改为 2 成功了，但是我的葡萄牙语键盘布局开始干扰其他测试脚本。所以我修改了代码，加入了 PT 和 UK 布局，在编译时在`#define`中修改它们。

如果能像普通的 USB 卷一样从电脑上访问 SD 卡，那就太酷了。我不知道这到底有多可行，但目前的固件不支持。我仍然希望能够将 SD 卡上任意文件的内容输出到屏幕上，所以我添加了另一个名为`ECHOFILEHEX`的脚本函数，它将 SD 卡中文件的内容作为转义字符输出。例如，如果文件`a.txt`包含“AAA”，脚本命令`ECHOFILEHEX a.txt`将输出“\x41\x41\x41”。这对于将二进制文件回显到`printf`或`echo -e`中很有用，至少在 Linux 主机中是这样。

与此同时，我在阅读原始代码时遇到了一些麻烦。你知道，我们都有不同的编程风格。不要误解我，我写过一些混乱的代码。我有时会浏览旧项目，寻找我编写的一些库或类，并想知道“到底是谁写了这么一堆冒着热气的代码？”我，是我。无论如何，我开始在这里和那里做了一点改变，最后几乎改变了整个代码。这就是开源的好处和坏处。如果你好奇，你可以在这里看看。

## 结论

总而言之，尽管有些颠簸，我对马尔杜伊诺还是很满意的。这正是我所期待的:一个针对 BadUSB 攻击的开放平台，它还处于起步阶段。很棒的是，我们都可以修补它，修改它，让它变得更好，或者只是让它适合我们的需要。我希望一个真正的社区可以开始，这样我们就可以看到它的全部潜力出现。我的清单包括模拟其他 USB 设备，更好的 SD 卡管理，以及通过未使用的引脚扩展设备。你想补充什么？

这是一条很长的路要走，很多事情都可能出错，所以祝这个项目好运！