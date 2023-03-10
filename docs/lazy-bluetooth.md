# 懒惰的蓝牙:与 BLE 一起构建，不要重新发明它

> 原文：<https://hackaday.com/2016/03/30/lazy-bluetooth/>

很有可能你身边至少有一个蓝牙设备。耳机、鼠标、键盘和扬声器变得越来越普遍。蓝牙形成一个短程无线网络，也可以执行文件传输和创建虚拟串行端口。

如果你曾经不得不停止听音乐来给蓝牙耳机充电，你知道蓝牙不会在电池上运行很久。2006 年，诺基亚推出了 Wibree，后来成为蓝牙低能耗(或 BLE)。如今，它被广泛应用于各种领域，值得您花时间对这项技术有一个基本的了解。

[![Fitbit_Charge_HR](img/4b7d9d56340fd971c3af38022aa1c838.png)](https://hackaday.com/wp-content/uploads/2016/03/fitbit_charge_hr.jpg) 现代蓝牙设备可以实现“经典”蓝牙、BLE 或两者兼而有之。正如你所料，BLE 非常省电，使用简单的纽扣电池可以运行几个月或几年。它还应该体积小，价格便宜。如果你有一个健身带(像左边的 FitBit)或智能手表，它可能依赖于 BLE。范围通常在 30 米以内。

## 客户端、服务器和节能

[![GATT](img/177ccec4a0e251983fdbd3404a750c62.png)](https://hackaday.com/wp-content/uploads/2016/03/gatt.png) 为了保存电力，BLE 的设备不怎么传输。蓝牙设备使用描述它们提供什么数据和服务的配置文件。所有 BLE 设备都使用从通用属性配置文件(GATT)派生的配置文件。关贸总协定使用 UUID(那些长的十六进制数字)来识别服务和特征。官方服务的 ID 为 16 位，而定制服务的 ID 为 128 位。服务器是拥有健身带、嵌入式恒温器或信标(发送 ID 和少量其他数据的 BLE 设备)等数据的设备。大多数设备将提供多种服务(见右图)。

作为节能计划的一部分，服务器拥有数据，并且大部分时间都处于休眠状态。例如，BLE 温度传感器将充当服务器。客户端是想要读取数据的手机、平板电脑或台式电脑。这看起来有些倒退，但这只是选择你的参考框架的问题。

服务器定期使用非常短的消息来广告它们所拥有的服务。作为广告的一部分，服务器可以包含少量数据，也可以告诉其他人它不接受连接(或者，通常两者都会接受)。当服务器通过广告发送其所有数据，并且不接受连接时，它被称为信标。

## 标准服务

蓝牙标准中定义了许多标准服务。例如，许多设备将提供电池服务，因此客户端可以询问设备的电源状态。然而，它将是一个只提供其电池电量的无聊设备。

其他服务面向 BLE 的目标市场。例如，有提供血压、跑步速度或体重(如体重)的服务。还有一些专门的服务，比如“找到我”,它会让服务器发出蜂鸣声或者指示它在哪里。

如果你熟悉传统的蓝牙，这些名字不会让你困惑。但是，如果您没有使用过较旧的系统，记住以下内容可能会有所帮助:

*   一个配置文件包含一个或多个服务。
*   服务器具有一个或多个特征。
*   虽然特征通常是单个值，但是也有值可以是相关数据的数组(例如，来自位置传感器的 X、Y 和 Z 坐标)的情况
*   描述符描述特征

甚至有一种邻近服务可以估计客户端和服务器之间的距离。它通过测量服务器接收到的信号强度来工作。客户端根据特定距离处的预期信号强度对自己进行评级，而服务器报告实际信号强度。这两个量的比值与距离有关。

## 抽象

[![ble1](img/6d2e72381a5893b76ff5b1aa3e89944a.png)](https://hackaday.com/wp-content/uploads/2016/03/ble1.png)

[Hackaday edition Tiny BLE board](http://store.hackaday.com/products/tiny-ble) will be used to demonstrate Bluetooth Low Energy in the next article of this series.

你可以在蓝牙规范中找到很多关于 BLE 内部的细节。然而，在实践中，您可能不会编写自己的 BLE 堆栈。相反，您将使用提供 API 的芯片组或开发板(就像右边出现的小 BLE)。

抽象对于 BLE 特别有用，因为每一微秒的传输时间都在消耗电池。您希望制造商已经对堆栈进行了微调，以充分利用他们的硬件。当然，也许你可以通过努力做得更好，但这很可能是一项艰苦的工作。下一次，我将介绍其中一个开发板和它提供的 API，以简化 BLE 开发。

同时，你可以通过下面的[吉米·雷·帕瑟]视频了解更多关于 BLE 的信息。[吉米·雷]有一种无与伦比的演讲风格。

 [https://www.youtube.com/embed/Wo2WmJFgf8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wo2WmJFgf8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



#### 照片致谢:

FitBit–By Wuefab[CC By-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0)