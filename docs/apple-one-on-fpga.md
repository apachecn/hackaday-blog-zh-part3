# 苹果一号，在 FPGA 上

> 原文：<https://hackaday.com/2018/03/29/apple-one-on-fpga/>

如今，苹果以 iPhones、iPads 和致力于图形用户界面而闻名。但事情并不是这样开始的。最初的苹果是围绕 6502 构建的单板计算机。1976 年，你可以花 666.66 美元买到一台，但你需要自己提供电视、电源和键盘。[Alangarf]没有 Apple 1，但他有一个来自[Andrew Holme]的用于 FPGAs 的 6502 CPU 内核，他将其充实为具有 VGA 输出和 PS/2 键盘端口的 Apple I 克隆。该项目使用 iCE40 板或 Terasic DE0 板。你可以把它移植到其他类似的 FPGAs 上。

这比试图找到一个原件要实际得多，因为苹果买回了许多旧主板并销毁了它们。根据 [Apple-1 注册表](https://www.apple1registry.com/)显示，目前仅存 71 块主板，其中 4 块可能已经丢失，8 块可能是重复的。我们听说其中只有六个还在工作。

该项目还允许您使用串行终端，您可以运行 Woz Mon 或 integer BASIC。有 8K 的系统内存，以及用于系统软件的仿真 4K 和 512 字节 rom。

最初的苹果在 1976 年很酷，但以今天的标准来看已经没有多少了。CPU 运行速度为 1 MHz，标准内存为 4K，而电视显示仅为字符。很难相信，这台简单的电脑推出了个人电脑行业的主要玩家。

旧苹果没有那么强大，所以体验它的另一个途径是通过它与现代 CPU 的简单模拟。我们已经看到 [ESP8266 完成了这个任务](https://hackaday.com/2017/12/30/espple-a-wireless-apple-1-on-an-esp8266/)。如果你更喜欢新的苹果]，你可以[在 DE2 FPGA 板](https://hackaday.com/2017/10/10/apple-ii-fpga/)上模拟一个。