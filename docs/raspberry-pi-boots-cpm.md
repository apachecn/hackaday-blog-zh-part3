# 覆盆子 Pi 靴子 CP/M

> 原文：<https://hackaday.com/2016/10/12/raspberry-pi-boots-cpm/>

逆向计算是一项有趣且有教育意义的追求，当然，有各种各样的模拟器可以让你使用和编程大量的旧计算机。然而，避免启动一个现代的操作系统，然后在其上模拟一个旧的系统，这是有吸引力的。一部分只是美学，当然真正的逆向计算发生在复古的硬件上。然而，作为一个实际的问题，逆向计算机会崩溃，并且通过仿真，您会假设花费在主机操作系统(以及在后台运行的其他程序)上的 CPU 周期将会从目标逆向计算机上取走。

如果你想尝试在树莓 Pi 上用 CP/M 引导一个“裸机”Z80 仿真器，可以试试 [EMUZ80 RPI](http://www.projekte.daleske.de/prog/11_EMUZ80_RPI/prog_EMUZ80_RPI_en.htm) 。文件驻留在 SD 卡上，Pi 直接引导它，避开任何 Linux 操作系统(如 Raspian)。它适用于 Raspberry Pi Model B、A+和 Raspberry Pi 2 Model B。与早期 Pi 模型上的标准 Linux 发行版的大量引导时间不同，您可以在短短五秒内引导到 CP/M。就像以前一样。

这项开发的秘密是一个被称为 [Ultibo](https://ultibo.org/) 的开源系统，这是一个基于 Open Pascal 的框架，允许你为 Raspberry Pi 创建裸机应用程序。选择免费的 Pascal 会让一些人高兴，让另一些人烦恼，这取决于你的偏好。Ultibo 仍在积极开发中，但最常见的功能已经存在；您可以写入帧缓冲区，读取 USB 键盘，并写入串行端口。这就是你制作自己的模拟器或编写自己的*末日*克隆版所需要的全部。你可以在下面看到一个关于 Ultibo 的视频(一系列中的第一个)。

 [https://www.youtube.com/embed/TCfpb8M0WeQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TCfpb8M0WeQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们过去也报道过其他的裸机项目。如果你宁愿去老派，你可以尝试复制[朗姆酒 80](https://hackaday.com/2015/04/15/the-rum-80-a-home-brew-z80-computer-built-from-scratch/)