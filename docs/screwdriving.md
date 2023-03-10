# 螺丝驱动

> 原文：<https://hackaday.com/2017/10/09/screwdriving/>

螺丝刀！这就像 wardriving，但不是发现 WiFi 网络，而是发现一种特殊类型的蓝牙低能耗(BLE)设备:成人玩具。是的，一切都将被连接起来，甚至振动器。欢迎来到 21 世纪。

安全研究员[Alex Lomas]最近发现，许多 BLE 成人玩具完全容易受到恶意攻击。事实上，从设计上来说，它们基本上对任何人都是敞开的。

> “成人玩具有助于成为物联网研究的伟大试验台:它们是 BLE，它们相对便宜，易于使用，并且有用于全方位测试的配套应用。”

是的…很棒的测试平台…嗯，总之，[Alex Lomas]发现没有 PIN 也没有密码保护，或者在分析的每个蓝牙成人玩具上 PIN 是静态的和通用的(0000 / 1234)。制造商不想经历这些麻烦，大概是因为性玩具缺乏显示屏，无法实现经典的蓝牙配对，以及随机 PIN 码等。虽然这可能是一个有效的观点，但几乎所有的电子设备都有一个用于输入的“开/关”按钮和一些允许某种形式输出的 LED(或者在这些情况下甚至是振动)。这是可以做到的，振动器并不是物联网世界中唯一的简约设备。

尽管 BLE 的安全性被设计削弱了，但是在有缺陷的协议上增加安全性是可能的。普通的网络浏览器一直都在这么做。通信不一定是明文，你可以看到“振动:10”在数据包中四处乱飞。例如，加密可以在应用程序和设备之间的 BLE 链接之上实现。可以理解的是，某些设备的安全性并不是绝对重要的。话虽如此，安全栏不一定要降到零——工作*或*游玩都不安全。

[via [Arstechnica](https://arstechnica.com/information-technology/2017/10/screwdriving-many-bluetooth-sex-toys-leave-users-vulnerable/)