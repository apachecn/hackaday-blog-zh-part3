# FPGA 计算机涵盖了 A 到 Z

> 原文：<https://hackaday.com/2017/01/13/fpga-computer-covers-a-to-z/>

[F4HDK]称他的新电脑为 [A2Z](https://hackaday.io/project/18206-a2z-computer) ，因为他从头开始构建一切(字面意思，从 A 到 Z)。嗯，严格来说，他确实是从一个 FPGA 开始的，但是你得有一些基础。核心 CPU 是一个 16 位 RISC 处理器，具有 24 位地址总线和 128 字高速缓存。该计算机拥有 2 兆内存、一个引导 ROM、一个 VGA 端口和键盘，以及一些其他有用的 I/o。CPU 开发使用 Verilog。

就软件而言，计算机有一个简单的操作系统、一个文件系统和一些基本程序，如文本编辑器和图像浏览器。开发软件包括一个汇编器和一个编译器，用于驻留在 PC 上的类似 BASIC 的语言。你也可以运行一个仿真器，在没有硬件的情况下实验 A2Z。你可以在下面的视频中看到一个在 A2Z 上运行的“汽车游戏”。还可以看到一些其他应用的视频。

游戏展示了 VGA 双缓冲。许多 FPGA 开发人员开发“克隆”CPU，以便他们可以利用开发工具和软件。A2Z 是一种独特的设计，我们很少看到定制的 CPU 拥有如此广泛的工具和应用程序。

我们之前已经讨论过[围绕定制 CPU 开发自己的基础设施](http://hackaday.com/2015/07/31/build-your-own-cpu-thats-the-easy-part/)的困难。我们还介绍了[我们的一些 CPU](http://hackaday.com/2016/03/16/crawl-walk-run-planning-your-first-cpu-design/)(别忘了[第二部分](http://hackaday.com/2016/03/25/crawl-walk-run-a-starter-cpu/))。

 [https://www.youtube.com/embed/-RE_gQDusow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-RE_gQDusow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/9ERjwqe0yUk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9ERjwqe0yUk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/3EUfW6J1Efc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3EUfW6J1Efc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

