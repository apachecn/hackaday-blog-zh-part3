# 构建一个，获得两个:在一块板上开发 CPLD 和 STM32

> 原文：<https://hackaday.com/2017/11/14/build-one-get-two-cpld-and-stm32-development-on-a-single-board/>

可编程逻辑器件已经在业余爱好者的世界中占据了一席之地，越来越多的项目展示了 CPLD 或其更大的兄弟 FPGA。这个位置是理所应当的——创建自己的定制数字电路不仅增加了灵活性，还开启了一个全新的机会世界。然而，这种新的境界可能会令人不知所措，同时又令人害怕。要轻松做到这一点，一个很好的方法是将可编程逻辑与您已经了解并熟悉的通用 MCU 系统相结合。[Just4Fun]用 [CPLD Fun Board](https://hackaday.io/project/27062-arduino-cpld-cpld-fun-board) 做到了这一点，这是一种将 Arduino 兼容 STM32F103 Cortex-M3 控制器连接到 Altera MAX II CPLD 的开发板。

PCB 本身有一些连接到 CPLD 的标准开发板设备:led、按钮、七段显示器和额外的 GPIO。CPLD 的其余引脚直接连接到 STM32 及其 SPI、I2C 和 UART 引脚。假设您想要创建自己的 SPI 器件。借助 CPLD Fun Board，您可以利用 STM32 上所有预先存在的库，并完全专注于可编程逻辑部分。更好的是，从 MCU 到 CPLD 的每个连接都有自己的引脚接头连接，以便连接您最喜欢的测量设备进行调试。如果您想知道，是的，您可以通过将 MCU 或 CPLD 引脚设置为 Hi-Z 来将外部硬件连接到这些连接器。

所有这些的缺点是需要专有的设计软件和专用于 CPLD 的程序员，可悲的是，这是可编程逻辑器件的日常现实。[Just4Fun]做得很好，编写了一个详细的分步指南，介绍如何设置环境和开始使用电路板，但如果你想了解更多，还有其他关于开始使用 CPLDs 的指南，如[。](https://hackaday.com/2014/04/06/cpld-tutorial-learn-programmable-logic-the-easy-way/)