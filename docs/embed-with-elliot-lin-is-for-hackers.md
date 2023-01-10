# 嵌入埃利奥特:林是黑客

> 原文：<https://hackaday.com/2017/05/26/embed-with-elliot-lin-is-for-hackers/>

如今，一辆汽车是数百个微控制器的滚动堆——只要问问任何一个灰胡子机械师，他就会开始他的“汽化器”咆哮。所有这些系统和子系统都需要在一个电气敌对的环境中相互交谈，毫不夸张地说，沟通错误，甚至延迟的沟通都会产生严重的后果。车内联网是一项严肃的业务。对于非汽车硬件黑客来说，汽车的大规模生产使得许多相关的收发器 IC 变得便宜。那么，为什么我们看不到更多利用这一巨大资源基础的黑客项目呢？

汽车网络的主干是控制器局域网(CAN)。Hackaday 自己的[Eric Evenchick]是一位杰出的汽车黑客，在一个多部分的系列文章中写下了你想知道的关于 CAN 总线的几乎所有东西，你肯定会想把它收藏起来以便以后阅读。发动机、刹车、门和所有仪表数据都经过(差动)CAN。速度快，可靠性高。实现起来也很复杂，有点贵。

在 20 世纪 90 年代末，许多制造商拥有自己专有的总线协议，与 CAN 一起用于汽车网络的非关键部分:例如，安装在门上的控制台如何与门锁驱动器和车窗电机通信。不值得用这样的非关键和本地通信来混淆主 CAN 总线，所以子网从主 CAN 中分离出来。这些不需要主网络的速度或可靠性保证，并且由于成本原因，它们必须易于实现。最小的微控制器应该足以上下滚动窗口，对吗？

[![](img/a7eaee8f30c49945d9eb13e6135395fd.png)](https://hackaday.com/wp-content/uploads/2017/04/local-interconnect-network-lin-animated-tutorial-1rxo3lobx0imkv-shot0002_thumbnail.png) 在 21 世纪初，本地互连网络(LIN)规范对这些子网的一种方法进行了标准化，重点关注低实施成本、中速、可重新配置性以及集群中一个主微控制器和少量从微控制器之间通信的可预测行为。便宜、简单、可在小型微控制器上实现，并且正好适合中等规模的项目？黑客的梦想！你为什么不在你的多微项目中使用林？让我们开始吧，你可以看看这些是否对你有用。

## LIN 协议

阿林“集群”，也就是行话中对本地微型网络的称呼，由一个主微控制器和多个从微控制器组成。LIN 从标准 8N1 UART 串行开始，通常为 19，200 波特，并取消了一条线。接下来，它添加了一个协议，允许将这条单线用作总线，在多个从设备之间共享。如果您尝试为简单的 UART 串行通信开发自己的网络协议，您最终会得到类似 LIN 的结果。去拿一份规格说明书 (PDF)并一起阅读！

每个 LIN 事务基本上是相同的:主机发送一个包含受保护标识符(PID)的报头，它指定要执行的任务。任务可以是类似“报告温度传感器 2”或“设置伺服机构 3 的位置”。根据任务的不同，随后是 1 到 8 字节的数据，带有 2 字节的校验和。从机必须知道对哪些任务做出响应，以及如何做出响应。因此，如果发送了“设置伺服 3 位置”,伺服 3 从机需要监听下一个字节并做出相应的反应。所有不响应命令的从机可以忽略数据，直到下一个前同步码。

[![](img/718e9c8a09dc37df6aafa5f774d4aaa0.png)](https://hackaday.com/wp-content/uploads/2017/04/lin_frame.png) 在“报告温度传感器 2”的情况下，带温度传感器的从机收到命令后立即发送其数据。由于字节长度是预先知道的，并且只允许传感器 2 对该任务作出响应，所以主机知道正好监听(比如说)四个字节的响应，并且知道这需要多长时间。

这种主设备发送报头、从设备发送响应的轮询系统可以保证所有器件都不会同时访问总线，因此 LIN 只需一条 RX/TX 线路。前同步码包括一个 sync 字节(0x55 ),帮助从机锁定主时钟，因此从机可以运行在更便宜的 RC 时钟源上，并且可以自动选通。

因为消息的长度是预先知道的，所以主设备的轮询例程的时间可以写在时间表中。主设备以规定的时间间隔轮询网络，如果从设备没有在 1.4 倍于事务所需时间的时间内做出响应，则认为从设备在运行中丢失。无论哪种方式，主设备都在处理其时间表中的下一个项目，并且不会重试可能有缺陷的从设备，直到它再次出现。这保证了所有器件的已知更新速率，从而简化了主机编程。

[![](img/411b3b41a6bc3b8d68fce28a3aabca13.png)](https://hackaday.com/wp-content/uploads/2017/04/lin_frame_detail.png) 这些都是基础知识。主机发送 PID，随后是一系列数据字节。一切都是舒适的老式 UART，呼叫和响应，尽可能简单地适应，以创建一个小网络。

## 临时演员

[![](img/f7bf02d501e7d0bac92db92da9a052c7.png)](https://hackaday.com/wp-content/uploads/2017/04/local-interconnect-network-lin-animated-tutorial-1rxo3lobx0imkv-shot0002.jpg)

GUI LIN configuration app from [an instructive video](https://www.youtube.com/watch?v=1RXo3lOBX0I).

保持网络的简单性要求主设备和从设备都同意命令集和有效的响应长度。原则上，LIN 集群运行需要大量的信息。在 LIN 规范中，有一个标准格式可以用来表示所有这些内容。

还有一个标准的 API，主微控制器和从微控制器都可以使用它来处理阿林集群中的编码行为。结合起来，这就形成了指定和实现 LIN 总线的标准工作流程——对汽车制造商来说非常方便，对黑客来说也不是没有用。

还有一种为总线定义的睡眠状态和行为，以及相关的睡眠和唤醒信号。所有从机都应该响应睡眠信号，如果没有收到主机的消息，任何一个从机都应该在四秒钟的超时后自动进入睡眠状态。任何节点，无论是从节点还是主节点，都可以发送唤醒命令，之后主节点应该回到正常的轮询时间表。

[![](img/3c3ef50fa5e5c150d228198d3262aa95.png)](https://hackaday.com/wp-content/uploads/2017/04/lin-bus-diagnostics-ku1odyxooxwmp4-shot0001.jpg)LIN 2.0 版本包含了许多可选的帧类型，使网络更加灵活。特别是，“零星帧”使得从机的响应是可选的，如果它自上次更新以来没有获得任何新数据的话。“事件触发帧”类似于零星帧，除了它们可以被任何具有新数据的从节点额外响应。

这可能会在总线上引起冲突，在这种情况下，校验和不会累加，主机会像以前一样退回到特定于从机的帧。当数据更新不频繁时，这两种模式加快了总线速度，但增加了调度的不确定性和代码的条件复杂性。只有在需要的时候才使用它们。

主服务器也可以有多个时间表，并在它们之间切换。奴隶们不在乎——他们只是监听与他们相关的任务。举例来说，如果伺服位置数据没有改变，即使它使事情在概念上变得更简单，主机也没有理由每一个周期都发送伺服位置数据。你的电话。

甚至还有一个可选的传输层规范，它与 CAN 总线兼容，使本地 LIN 集群与更大的网络集成更加容易。简而言之，林是一个非常透彻的思考通过 UART 总线协议与体面的行业采用。您可以从 LIN 收发器硬件的各个供应商那里找到不错的教程。(这里有一个来自国家仪器的[精彩介绍。)](http://sine.ni.com/np/app/main/p/ap/icomm/lang/en/pg/1/sn/n17:icomm,n21:9536/fmid/2954/)

## 硬件—物理层

除了这些协议之外，还有各种各样的 LIN 收发器芯片，普通收发器的价格从 0.25 美元到 0.50 美元不等，集成稳压器的“系统基础”芯片的价格高达一两美元左右。这些特别巧妙，因为收发器可以处理睡眠/唤醒逻辑，并打开和关闭微控制器的电源。这使得集成工作电压为 3.3 V 的从节点变得非常简单。

[![](img/9e7acbbb13215bf4b274cb11b57eb827.png)](https://hackaday.com/wp-content/uploads/2017/04/mlx80030-lin-system-melexis.jpg)

[Little chip buys you a lot.](https://www.melexis.com/en/product/MLX80030/LIN-System-Basis-IC)

由于 LIN 总线是为汽车设计的，因此它通常被指定为 12 V，因为这是通过汽车线束的线路。LIN 收发器硬件需要能够适应更高的电压，因为汽车电气系统可能处于尖峰环境。它们还必须应对总线争用问题，因为收发器芯片可能试图拉低 LIN 线路，而其他人试图拉高它，因此还内置了过热保护。LIN 收发器是健壮的小动物。

与用小电阻上拉的 I2C 线路不同，汽车 LIN 总线用 1kω电阻上拉至 12 V。为了足够快地拉低这条线，LIN 收发器需要能够传导数十毫安的电流，因此它们内置了略显粗壮的(用于 IC)晶体管。高电压和相对较高的线路电流相结合意味着汽车专用 LIN 总线适用于 40 米，而不是 I2C 在不借助驱动器的情况下提供的几米。如果您需要的距离或噪音免疫，林是你的。

但是没有任何东西强迫你在 12 V 下运行总线，甚至是收发器硬件。我见过的微芯片收发器工作电压低至 5.5 V，而恩智浦和 Melexis 的芯片收发器工作电压为兼容 Arduino 的 5 V。

没有任何东西强迫你使用收发器硬件！您只需将一个 PNP 晶体管(或 P 沟道 MOSFET)连接到总线线路，用 UART TX 驱动它，用 RX 线路对总线进行采样。这有本地回声的缺点，但可以用软件处理。或者，只增加几个部件，就有了我们在之前见过的[这个解决方案。不过，我没有发现任何实现 LIN 收发器的黑客项目。可能是因为工业用的太便宜了。](http://hackaday.com/2014/01/13/software-half-duplex-uart-for-avrs/)

## 优势和劣势

没有一辆巴士是适合所有场合的，林也不例外。LIN 并不是特别快，它被设计成 19，200 波特左右的 UART。从微控制器的角度来看，更新很少发生。带超时的全长事务大约需要 10 毫秒。如果主设备轮询 16 个设备，最坏的情况下，更新速率约为 7 赫兹。当然，主机不需要每次都轮询每个设备，很多时候消息长度只有一半，但你不会得到超过 200 Hz 的频率。另一方面，更新率是恒定的，因为能够为易变的设备实现严格的超时，这对于可靠性和简单性来说是非常好的，并且不比 I2C 慢多少。

您将在野外看到 LIN 的两个主要版本，1.x 和 2.x。除了上面提到的可选帧类型之外，这两个版本还有不同的校验和公式，2.x 中的一个真的很奇怪，需要一个基于网络的计算器来确保您做得正确。他们从 256 或更大的值中减去 255，而不是加上 mod-256。这就像一个 8 位溢出，绕回 1 而不是 0。这对你们任何人有意义吗？

LIN 设备在汽车行业之外不像 I2C 或 SPI 那样普遍，所以你可能从来没有被迫处理协议。但是，如果你想用一根线(加上地)将少量基于微控制器的模块尽可能简单、廉价地联网，很难想象还有比这更简单的事情。编写 [I2C 奴隶代码](http://hackaday.com/2016/11/07/diy-i2c-devices-with-attiny85/)当然不是一件轻松的事。编写代码监听 UART 线路上的特定字节，然后做出反应，这再简单不过了。

想把你的普通 UART 变成总线吗？从林的书里拿一两页出来！你已经这样做了吗？给我们看看！