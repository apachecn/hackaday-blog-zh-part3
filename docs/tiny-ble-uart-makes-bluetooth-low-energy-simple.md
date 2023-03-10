# 微型 BLE UART 让蓝牙低能耗变得简单

> 原文：<https://hackaday.com/2016/04/06/tiny-ble-uart-makes-bluetooth-low-energy-simple/>

上次我谈到了蓝牙低能耗(BLE)处理数据的内部原理。我提到过，它的设置方式是为了省电，也是为了支持常见的 BLE 设备，如心率监测器。另一方面，我也提到过你通常不需要处理这个问题，因为你使用了一个抽象层。

这一次，我想向你展示我是如何使用[Hackaday 特别版小 BLE](http://store.hackaday.com/products/tiny-ble) (来自 Seeed 工作室)及其 mbed 库来做一个快速简单的 BLE 项目的。如果你没有看过《T2》的第一部，不要担心。这种抽象非常好，除非您想回头更详细地了解幕后发生的事情，否则您可能不需要这么做。

我想要一个简单的例子，所以你可以在它的基础上建立，而不必删除很多代码。出于这个原因，我决定让我的手机通过 BLE 控制三色 LED 的状态。为此，我将使用虚拟 UART 和一些现成的电话软件。整个事情不需要太多代码，但这是关键:抽象使得 BLE 相对简单。

## 硬件

[![](img/811b179ff0121d9685dfa3cc1f68948b.png)](https://hackaday.com/wp-content/uploads/2016/04/tinyble600.png) 这个小小的 BLE 板大约有一个长方形大邮票那么大(见右图)。然而，这只是故事的一半。棋盘是两块连在一起的棋盘，中间有一条划线。较大的子板实际上是编程、调试和监控第二子板(图像右侧的目标板)的接口。第二块板是带有 BLE 和其它外设的板。它没有 USB 端口，但对于一个独立的应用程序，你可以对设备进行编程，将目标板取下并单独使用。那块板子大约有我食指的一个关节那么大(当然，我是个大块头，但没那么大)。

编程板有一个 USB 端口(提供一个虚拟串行端口)，一个按钮，它还可以测量提供给目标的电流(这很重要，因为许多 BLE 项目都希望尽可能长时间地使用电池)。

目标板有一个 nRF51822，它是 CPU(一个 16 MHz 的 ARM Cortex-M0)和 BLE 接口。还有一个 3 色 LED 和按钮，以及一个 MPU6050，允许 CPU 使用 3D 加速度计和陀螺仪来确定位置和运动。该设备有一个板上处理器，它融合数据并卸载 CPU。30 美元左右还不错。

## 环境

小小的 BLE 板使用 mbed [在线环境](https://developer.mbed.org/)。登录后，点击平台，找到 TinyBLE 板，并使用提供的按钮将其添加到您的 IDE 中。就是这样。工具链已准备就绪。

关于在线 ide 有很多争论，也有可能使用其他离线工具。然而，对于入门来说，很难在两三分钟内设置好整个工具链。还有许多示例代码可以帮助您入门。如果您决定要这样做，可以稍后从联机 ide 导出到脱机 IDE。

如果你想回顾如何开始 mbed，我们过去已经就此做过[个帖子](http://hackaday.com/2015/08/11/getting-started-with-arm-using-mbed/)，包括下面的一个视频。

 [https://www.youtube.com/embed/cKbMyXl3yBA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cKbMyXl3yBA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 接收端

[![term](img/b259daf052b3e2d53b565da31734b9f7.png)](https://hackaday.com/wp-content/uploads/2016/03/term.png) 在嵌入式方面使用虚拟 UART 的想法听起来很棒，但你也需要在手机或其他设备上安装软件，对吗？幸运的是，UART 服务可以与 Nordic Semiconductors 的免费 nRF UART 应用程序配合使用，适用于 [iOS](https://itunes.apple.com/us/app/nrf-uart/id614594903?mt=8) 和 [Android](https://play.google.com/store/apps/details?id=com.nordicsemi.nrfUARTv2) 。

这个应用程序非常简单。但是，它允许您使用嵌入式设备进行发送和接收。在您的嵌入式代码工作之后，您总是可以自己更详细地了解主机软件。

## 简单的例子

我剥离了一个更大的示例程序来创建简单的演示程序(你可以在网上找到[整个项目)。这是代码的核心部分:](https://developer.mbed.org/users/wd5gnr/code/Tiny_BLE_Simple/)

```
 ble.setAdvertisingInterval(160); /* 100ms; in multiples of 0.625ms. */
 ble.gap().startAdvertising();
 char r[4];
 r[1]='\r';
 r[2]='\n';
 r[3]='\0';

 while (true) {
   ble.waitForEvent();
   int c; 
   r[0]=c=uartService._getc();
   if (c<=0) continue;
   if (c=='R' || c=='r') { red=0; green=1; blue=1; }
   else if (c=='G' || c=='g') { red=1; green=0; blue=1; }
   else if (c=='B' || c=='b') { red=1; green=1; blue=0; }
   else r[0]='?';
   uartService.writeString(r);
 }

```

如果您阅读了上一期文章，您可能会记得 BLE 服务器(在本例中是微型服务器)发送广告，客户端可以使用这些广告来发现服务器。在某些情况下，数据在广告中，而在其他情况下，它只是通知客户服务是可用的。这里，设置已经完成，开始时的两个调用只是将时间间隔设置为 100 毫秒，然后开始播放广告。

让我们回到广告设置，看看主循环。当 BLE 事件发生时，代码从虚拟 UART 中读取并查找 R、G 或 B，并按预期设置 LED。它也回显命令。小写字母是可以接受的，如果你输入了任何意想不到的东西，你会得到一个问号，而不是回显。简单吧？

实际的 BLE 设置如下所示:

```
ble.init();
ble.gap().onDisconnection(disconnectionCallback);
ble.gap().onConnection(connectionCallback);
/* setup advertising */
ble.accumulateAdvertisingPayload(GapAdvertisingData::BREDR_NOT_SUPPORTED);
ble.setAdvertisingType(GapAdvertisingParams::ADV_CONNECTABLE_UNDIRECTED);
ble.accumulateAdvertisingPayload(GapAdvertisingData::SHORTENED_LOCAL_NAME,
(const uint8_t *)"smurfs", sizeof("smurfs"));
ble.accumulateAdvertisingPayload(GapAdvertisingData::COMPLETE_LIST_128BIT_SERVICE_IDS,
(const uint8_t *)UARTServiceUUID_reversed, sizeof(UARTServiceUUID_reversed));
UARTService uartService(ble);
```

您可以看到客户端连接和断开连接都有回调。此外，广告上还有各种参数设置。BREDR_NOT_SUPPORTED 标志告诉客户端这是一个仅限 BLE 的设备。UART 服务有特定的连接类型和 id，所以您可以把它们当作样板文件。简称与原始示例 smurfs 相同。

代码还有更多的内容，但仅此而已。其中大部分涉及到设置 I/O 引脚和本地串行端口以进行调试。诚然，这是一个简单的例子，但这就是要点:几十行代码产生了一个 BLE“串口”，可以与手机上的应用程序进行对话。

## 下一步是什么？

如果你想玩 MPU6050 令人印象深刻的动作捕捉功能，当你在编辑器中启动一个新项目时，你可以选择的标准示例将让你开始(你也可以[在这里](https://developer.mbed.org/teams/Seeed/code/Seeed_Tiny_BLE_Get_Started/)找到代码)。这个例子也使用了 UART 服务，实际读取 MPU6050 的代码都在这里。

当然，你也可以构建不使用 UART 服务的东西。库文档可以帮助您从那里开始，但是我最初的观点仍然成立:了解 BLE 协议的细节是很好的，但是由于库的抽象，您不需要知道太多就可以工作。特别是使用 UART 服务，使得 BLE 只是串行端口的另一个传输层，这是一个我们都知道如何忍受的抽象概念。