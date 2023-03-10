# 树莓派上的地狱操作系统

> 原文：<https://hackaday.com/2015/11/22/inferno-os-on-raspberry-pi/>

Unix 不是唯一来自贝尔实验室的操作系统。为了通过网络将硬件与用户界面分离，贝尔还开发了一个名为 Plan 9 的操作系统(以著名的糟糕电影 Ed Wood 命名)。虽然 Plan 9 仍在使用，但它从来没有像 Unix 那样获得过动力。1996 年，贝尔实验室(现在的美国电话电报公司)决定将其重点转移到 Inferno，这是一个旨在挑战 Java 作为跨平台虚拟机环境的操作系统。现在 LynxLine Labs 已经将 Inferno 移植到树莓 Pi 上。

他们不仅做了这项工作，还在 26 个实验室做了记录，如果你想跟进的话。或者，您可以直接进入[项目页面](https://bitbucket.org/infpi/inferno-rpi)并获得结果和更新(从提交日志判断，该项目正在积极开发中)。

但丁会感到自豪，因为现在维护地狱的公司被命名为维塔四星龙控股公司。虚拟机命名为 Dis，基础语言为 Limbo，通信协议命名为 Styx。顺便说一下，Styx 与最新的 Plan 9 文件系统协议相同。

鉴于其传统，9 号计划和 Inferno 有很多共同的想法并不奇怪。特别是所有的资源都是文件，甚至是网络资源。Styx 管理与本地和远程资源的所有通信。它与 Raspberry Pi 不太一样，但桑迪亚国家实验室甚至将 Inferno 移植到了安卓手机上(见下面的视频)。

如果你正在寻找更多关于使用 Pi 进行操作系统开发的教育，我们[找到了一门课程。如果你对](http://hackaday.com/2012/09/02/operating-systems-development-with-the-raspberry-pi/)[计划 9](http://hackaday.com/2012/12/01/plan-9-on-the-raspberry-pi/) 和《地狱》通过软件让所有资源看起来像文件印象深刻，别忘了你也可以用硬件做到这一点。

 [https://www.youtube.com/embed/dF_-jQc53jw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dF_-jQc53jw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

