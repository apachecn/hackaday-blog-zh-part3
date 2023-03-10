# 黑魔法探针:最好的 ARM JTAG 调试器？

> 原文：<https://hackaday.com/2016/12/02/black-magic-probe-the-best-arm-jtag-debugger/>

我们并不总是 JTAG，但当我们这样做时，我们会使用一个黑魔法探针。这是一个完全开放的 ARM 芯片调试发电站。如果你对小型 ARM 芯片编程，而你没有 BMP，你需要一个 BMP。现在，这些小宝石的主要生产商之一正在运行一个 [Kickstarter](https://www.kickstarter.com/projects/esden/1bitsy-and-black-magic-probe-demystifying-arm-prog) ，在那里你可以得到一个制作精美的和/或一个 [1Bitsy](https://hackaday.io/page/2540-1bitsy-firmware-development-with-the-lights-on) 基于 STM32F415 的开发板。

BMP 为什么这么伟大？首先，它在一个器件中集成了 JTAG 和 UART 串行端口。你可以闪存目标，运行你的代码，使用串行端口进行`printf`调试，就像你知道你想要的那样，然后在你需要的时候依靠成熟的 JTAG 加 GDB，所有这些都在一个加密狗中。就是很方便。

但是 BMP 的杀手锏是它在探测器上运行一个 GDB 服务器*。它打开了一个虚拟串行端口，您可以通过主机上的 GDB 直接连接到该端口。没有必要为 [OpenOCD](http://openocd.org/) 配置争论不休，或者打开第二个窗口来运行【texane】神奇的 [st-util](https://github.com/texane/stlink) 。运行 GDB，你就可以调试了。正如上面的链接所展示的，有许多硬件/软件组合可以帮助您进行调试。但是通过将调试服务器和 JTAG 硬件结合起来，BMP 是迄今为止最聪明的。*

充分披露:我们使用我们自己构建的 BMP，也就是说我们[编译并刷新固件到我们手头的 4 美元 STLink 克隆编程器](http://embdev.net/articles/STM_Discovery_as_Black_Magic_Probe#Building_Firmware_for_ST_Link_V2_Clones_and_Flash_Using_Two_Cheap_Clones)中。打破所需的信号需要一点丑陋，精细的焊接，但我们喜欢这种事情。如果你不知道，对我们来说，早期的 Kickstarter(带电缆)看起来很划算。