# Orka 控制着(Pi)世界

> 原文：<https://hackaday.com/2016/10/07/orka-controls-the-pi-world/>

如果您部署了许多 Raspberry Pi 计算机，您可能会发现登录每台计算机来执行不同的任务很不方便。 [Orka](https://haikarthikssk.github.io/Orka-Server/) ，是由【Karthik K】开发的一个开源项目，是一个运行在桌面 PC (Windows、Linux 或者 Mac)上的服务器，可以控制多个 Orka 客户端(可以运行在 Pi，或者桌面 PC 上)。顺便说一下，我们知道[Karthik K]正在寻找 Mac 测试人员。

从服务器上，您可以执行命令和创建任务。您还可以在客户端电脑达到阈值时收到通知(例如，温度过高或 CPU 或 RAM 使用率过高)。您可以在客户端打开一个 shell 并执行其他操作。

在 GitHub 上，你可以同时找到[服务器](https://github.com/haikarthikssk/Orka-Server)和[客户端](https://github.com/haikarthikssk/Orka-Client)的 Javascript 源代码。该项目是全新的，所以如果它有一些粗糙的边缘，我们不会感到惊讶，但由于它是 HTML 和 Javascript，并且是开源的，您可能可以修复或增强您喜欢的任何东西，并将其反馈给该项目。

我们已经看到了很多树莓 Pi 集群，我们也谈到了 T2 在互联网上公开一个 Pi。如果你有很多 Pi 板，Orka 可能是一个有用的工具。