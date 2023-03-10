# 一个可以踩踏的键盘

> 原文：<https://hackaday.com/2018/01/19/a-keyboard-to-stomp-on/>

宏是有用的东西。它们允许一次按键就能执行一系列命令。有各种各样的硬件和软件解决方案来创建和使用宏来改进您的工作流，现在[Evan]已经将开源的 ManyKey、[和一个构建教程带入了竞争中。](https://www.manykey.org/tutorial.html)

本教程是对 ManyKey 的一个很好的介绍，因为[Evan]介绍了一个用脚操作的宏键盘的构造。基于 Arduino Leonardo 并使用吉他效果中常用的现成脚踏开关，它是可访问的，同时还暗示了系统的灵活性。宏通过 Python 应用程序编程输入键盘，Python 应用程序通过串行通信，配置保存在 Arduino 的板载 EEPROM 中。在 GitHub 上自然可以获得 ManyKey 源代码。

[Evan]告诉我们，当他的手在转盘上忙碌时，他用他的设置用脚运行 DJ 软件。也就是说，这可以用于各种各样的其他应用。效率就是一切，我们喜欢看到旨在通过新想法和定制构建来改善工作流程的键盘项目—[这种快捷键就是一个很好的例子。](https://hackaday.com/2017/06/19/diy-shortcut-keyboard/)