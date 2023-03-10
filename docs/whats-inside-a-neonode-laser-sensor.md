# 新节点激光传感器里有什么？

> 原文：<https://hackaday.com/2018/03/06/whats-inside-a-neonode-laser-sensor/>

每隔一段时间，你会得到一个很酷的硬件，当然，你的第一反应是打开它，看看它是如何工作的，对吗？也许看看它是否能被哄骗做得比盒子上说的多一点点？上周三也是如此，当时我在嵌入式世界贸易博览会上，无意中发现了一个很酷的触摸显示屏，它显然漂浮在半空中。

这种展示本身是一种聚焦的“小辣椒的鬼魂”的幻觉，从 [Aska3D](https://aska3d.com/en/) 制造的一面昂贵的镜子上反射出来。我知道的不多——我没能把一个精美的玻璃盘子带回家——但它看起来相当不错。但这种显示是交互式的:你可以触摸浮动的 2D 投影，就好像它真的在那里一样，软件会做出反应。什么在半空中做触摸反应？我对传感器很着迷，所以我开始问问题，并带着一小盒原型 [Neonode zForce 空气传感器棒](http://www.neonode.com/products/)离开。

[![](img/60644069c31fea2e6eea1875e161b459.png)](https://hackaday.com/wp-content/uploads/2018/03/technology_v2.png)zForce 传感器本质上是一组红外激光器和光电二极管，一些透镜限制了它们的视野。红外线照射到你的手指上，然后反射回棒上的光电二极管。因为光电二极管的响应角度有限，所以它们可以用来三角测量手指在显示器上方的距离。在红外激光中快速扫描并注意哪些光电二极管接收到反射，可以在 2D 空间中定位几个指尖，这解释了浮动显示器的交互部分。有了这些传感器中的一个，你就可以[给任何东西](https://air.bar/)添加一个 2D 触摸面。就像隐形的[激光竖琴](https://en.wikipedia.org/wiki/Laser_harp)也能感知距离。

预期的目的是指尖检测，这是固件擅长的，但它也必须能够检测其范围内的任意(凹)物体的形状，这将是我的黑客。我在一个晚上就完成了 90%的工作，这要感谢每个硬件黑客工具箱里都应该有的负担得起的工具和免费软件。因此，请继续阅读对 nice 硬件的不幸破坏，浏览一些有用的命令行硬件黑客工具，以及从一些测试点获得的类似 SPI 的数据中免费创建动画。

## 打开箱子

回想起来，可能没有必要把这些东西拆开——制造商网站上的图表非常逼真。在里面，你会发现一个印刷电路板，每 8 毫米有一个红外激光器和光电二极管，一些定制的塑料透镜和几个芯片。不过，这里有一些漂亮的图片。

 [![Strip Broken Open](img/ceafb97dde773dba0290feffc8300e1a.png "DSCF0645")](https://hackaday.com/dscf0645/) Strip Broken Open [![Molded Lenses and Mirrors](img/89f0b8bbeae809f5b25d70a111da867e.png "DSCF0649")](https://hackaday.com/dscf0649/) Molded Lenses and Mirrors [![Chip B and Mirror Profile](img/008c6597d117a77f3602e6ebb15754e9.png "DSCF0639")](https://hackaday.com/dscf0639/) Chip B and Mirror Profile [![Chips Closeup](img/3c3026f5f2ed45e60af41d463653fa32.png "DSCF0646")](https://hackaday.com/dscf0646/) Chips Closeup [![Chip A](img/3c7a6995711ca2e9fec73a2979b2871a.png "DSCF0637")](https://hackaday.com/dscf0637/) Chip A [![Chip B](img/a64990d2773a3ab662dae9daa51e7ec3.png "DSCF0638")](https://hackaday.com/dscf0638/) Chip B

镜头很整洁，由一个 45 度的镜子组成，允许 PCB 上安装的二极管在杆的厚度范围内发射和接收。激光器和光电二极管共用透镜，降低了制造成本。前三个单元之后的大部分薄 PCB 是“空的”，仅用于容纳激光器和光电二极管芯片。这是一个不错的硬件。

板上芯片集成电路甚至没有覆盖环氧树脂——尽管这些电路板标有“原型”,谁知道生产单位是否如此。根据广告文案，这两个芯片中的一个是实时进行图像处理的定制 ASIC，另一个是[定制 STM32 ARM 微控制器](http://www.st.com/content/st_com/en/about/media-center/press-item.html/t3995.html)。在评论里推测哪个是哪个！

PCB 在金属框架下粘合到位，内部肯定没有用户可维修的部件。遗憾的是，当我移除 PCB 时，一些连接线松了。当我把这个传感器粘在一起时，定制 ASIC 附近的一个区域变热。为我无聊的好奇心牺牲了！叹气。

## 基础知识:USB 接口

我得到了传感器演示套件的原型版本，其中包括传感器的 USB 和 I2C 手指检测功能的分线板，所以当然，我必须测试它们。插上电源，输入`dmesg`显示“Neonode AirModule 30v”是一个 USB HID 设备，这意味着弄清楚它的 USB 功能将是一件轻而易举的事情，因为它发出的所有数据都在数据描述符中描述。

我用 [`usbhid-dump`](https://github.com/DIGImend/usbhid-dump) 读入描述符，用【Frank Zhao】优秀的[描述符解码器](http://eleccelerator.com/usbdescreqparser/)以纯文本方式获取全部内容。它看起来像是一个标准的数字化仪，支持六个手指，并具有供应商定义的配置端点。如果你想继续玩下去，这里有一个描述符转储。顺便说一下，如果你正在制作自己的 USB HID 设备，像这样的转储是很好的起点。查看您的鼠标有哪些功能。

[![](img/cbfeb7463023b7b3332d4042cf8bc447.png)](https://hackaday.com/wp-content/uploads/2018/03/2018-03-06-005236_1366x1792_scrot.png) 但是坦白地说，遍历一个描述符文件是一项艰苦的工作。`dmesg`说传感器是作为`/dev/usb/hiddev3`连接的，那么为什么不在我挥动手指的时候实时看看它在做什么呢？`sudo cat /dev/usb/hiddev3 | xxd`获取原始的二进制输出，并通过`[xxd](https://linux.die.net/man/1/xxd)`将其转换成“人类可读的”hexdump。(`xxd`的天才之处在于`-r`标志，它能把你编辑过的 hexdump 变回二进制，在命令行上实现 90 年代的破解。)仅仅通过观察数字的变化和移动手指，我就弄清楚了哪个字段代表手指数，哪个字段对应每个手指的 16 位 X 和 Y 坐标。根据描述符，它将未测量的手指报告为零。

当然，所有这些，以及 I2C 接口的完整规格都可以在 zForce 在线文档中找到。命令被包装成 [ASN.1 格式](https://support.neonode.com/docs/display/AIRTSUsersGuide/ASN.1+PDU+Description)，这是一种可疑的便利。不过，如果你想通过 USB 或 I2C 使用这些设备来检测手指，只需阅读一些文档并编写一个驱动程序。

## 逻辑分析仪与测试点

[![](img/09cd01e061601acc8095b159d7540b38.png)](https://hackaday.com/wp-content/uploads/2018/03/dscf0651.jpg) 为了让这些感应条更有趣，我开始在设备背面暴露的测试点周围打转。最靠近输出连接器的那组引脚大多是连接器本身的重复引脚，没什么意思。比较好玩的是一个星座([昴宿星？](https://en.wikipedia.org/wiki/Pleiades))的七个测试点，似乎只适用于长度超过 180 毫米的传感条

一个点有一个清晰的 21 MHz 时钟信号周期性运行，另外两条线路有看起来是 10.5 MHz 的数据，强烈暗示某种同步串行线路。该区域的另外两个引脚发射脉冲，可能与传感器扫描的开始和处理数据的开始有关，但直到我连接一些跳线和逻辑分析仪后，这一点才变得明显。

我非常喜欢开源的 [Sigrok](https://sigrok.org/) 软件来进行这种分析。GUI `pulseview`使得探索您还不理解的信号变得相当容易，而切换到命令行`sigrok-cli`来执行重复的任务使得一些相当复杂的扩展变得容易。我会告诉你我的意思。

![](img/3738c5bddd631dac6cba5faf03e1dbe3.png)

我从一个基于相同 Cypress FX2 芯片的 Saleae 逻辑克隆开始。这对于 5 美元左右来说是一笔不错的交易，体面的内存深度和良好的 Sigrok 支持弥补了 24 MHz 的低采样率。这让我对信号有了一个很好的了解，并证实了当没有手指时，设备会进入低功耗扫描模式，当引脚 5 变为低电平时触发会很好地隔离大部分数据。但为了真正提取三个同步串行引脚上的数据，我需要加快速度。

[Openbench 逻辑嗅探器](https://sigrok.org/wiki/Openbench_Logic_Sniffer) (OLS)将执行 100 MHz，这对于该应用来说足够了，但是它具有非常短的 24 k 样本存储器，它必须通过 115，200 波特串行线中继回 Sigrok。尽管如此，我可以*只是*挤在 50 兆赫的完整读取。在时钟和两条数据线上使用 Sigrok 的 SPI 解码器，我得到了看起来不错的数据。但是怎么解读呢？那是什么？

## 命令行、图形和实时手指挥动

从`pulseview`中获取一个数据很容易，但是弄清楚这些数据意味着什么需要建立一个微小的工具链。命令行和`sigrok-cli`进行救援:

```

sigrok-cli --driver=ols:conn=/dev/ttyACM3 --config samplerate=50m --samples 20k \
            --channels 0-5 --wait-trigger --triggers 5=0 -o capture.sr  

```

该命令读取指定串行端口上的 OLS，等待通道 5 变为低电平时触发，并以 Sigrok(zipped)数据格式输出数据。

```

sigrok-cli -i capture.sr -P spi:clk=0:miso=1:cpha=1 -B spi | tail -c +3 &gt; spi1.bin
sigrok-cli -i capture.sr -P spi:clk=0:miso=2:cpha=1 -B spi | tail -c +3 &gt; spi2.bin

```

这两个命令对采集的数据运行 SPI 解码器。没有必要在一个单独的步骤中这样做，除非您像我一样希望输出在两个单独的文件中。`-P`标志指定协议解码器，而`-B`告诉它只输出二进制的解码数据。`Tail`通过删除三个头字节来对齐数据。

现在是真正的技巧:绘制数据，交互地挥动手指，希望弄清楚发生了什么。你会惊讶于这种方法对未知信号的使用频率。

```

t=`date +%s`
convert -depth 8 -size 15x45+0 gray:spi1.bin -scale 200 out1_${t}.png
convert -depth 8 -size 15x45+0 gray:spi2.bin -scale 200 out2_${t}.png
convert  out1_${t}.png spacer.png out2_${t}.png +append image_${t}.png
convert  out1_${t}.png spacer.png out2_${t}.png +append foo.png

```

`[![](img/9bc872895247853bac879d26ce14d11a.png)](https://hackaday.com/wp-content/uploads/2018/03/image_1520295414.png)Convert`是 [Imagemagick](http://imagemagick.org/script/index.php) 图像编辑和创建工具集的一部分。您可以花几个小时来深入研究它的功能，但在这里，我只是从文件中提取字节，将它们解释为灰度像素，将它们组合成指定尺寸的图像，并将其放大，以便更容易看到。对来自传感器的每个数据流都是如此。

然后，这两个图像并排组合(`+append`)，中间有一个间隔图像，加上时间戳并保存。还写出了一个没有时间戳的版本，这样我就可以使用`eog`实时观察进度，因为它会在图像改变时自动重新加载图像。

将所有这些拼凑在一起会产生一个流，该流从逻辑分析器接收数据，将其解码为字节，然后将字节转换为图像。这足以让我看到我正在从(可能)Neonode 定制 ASIC 的输出中捕获近似位置数据。但是为什么就此打住呢？我以每秒 8 帧的速度将这些图像组合起来，把整个努力变成了一个视频:

```

ffmpeg -r 8 -pattern_type glob -i &quot;image_*.png&quot; \ 
  -c:v libx264 -vf fps=8 -pix_fmt yuv420p finger_hand_movie.mp4

```

 <https://hackaday.com/wp-content/uploads/2018/03/finger_hand_movie.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2018/03/finger_hand_movie.mp4](https://hackaday.com/wp-content/uploads/2018/03/finger_hand_movie.mp4)

这是我移动我的手指刚好在酒吧的表面上，然后超出范围，然后移动一只手，然后两只手都在框架里。数据较少的帧是它在没有检测到任何东西时所做的事情，它降低了扫描速率，显然进行了较少的数据处理。你也可以看到选择图像中 15 个像素的奇怪宽度的原因——这个条中有 30 个光电二极管，其中一边的 15 个数据显然与另一边的 15 个数据分开处理。无论如何，选择 15 的宽度会使图像环绕得恰到好处。

[![](img/08af4f941ba7ad76491dc1fe514940ca.png)](https://hackaday.com/wp-content/uploads/2018/03/dscf0654.jpg) 有一堆数据我还是不明白。头部的内容和扫描中途出现的斑点仍然是个谜。出于某种原因，数据底部的“高度”字段与顶部相反——上是上半部分的右边，下半部分的左边。

但是，即使我只是从转储 SPI 数据中得到并绘制出来，很明显我得到的是后处理的 X/Y 估计数据，它在描述简单对象的形状方面没有问题，至少像我手掌一样。这比我从默认的手指传感器输出中获得的数据集丰富得多，所以我可以说这次黑客攻击是成功的。也许我会在一个小机器人里放一对这样的东西，或者我会为我的笔记本电脑做一个(不)触摸板。

不管怎样，我希望你和我一起读这些东西的时候一样开心。如果您不是命令行忍者，我希望我向您展示了通过简单地将一系列工具组合在一起可以拥有的一些功能，如果您是，您最喜欢的 undersung 数据分析工具有哪些？