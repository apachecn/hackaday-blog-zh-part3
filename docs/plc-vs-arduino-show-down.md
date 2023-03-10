# PLC 与 Arduino 对决

> 原文：<https://hackaday.com/2017/07/17/plc-vs-arduino-show-down/>

Hackaday 的读者不需要介绍 Arduino。但在工业控制应用中，可编程逻辑控制器或 PLC 更为常见。这些是小型坚固设备，可以做简单的事情，如监控开关和控制执行器。由于经过加固，它们通常相当昂贵，尤其是与 Arduino 相比。[Doug Reneker]决定[在一个相对简单的工业风格应用中评估 Arduino 与 PLC](http://www.controldesign.com/articles/2017/arduino-vs-plc-for-industrial-control/) 。

该应用是由泵产生的流量的简单闭环控制。传感器测量 Arduino 的流量，Arduino 调节控制阀致动器以保持指定的设定点。软件使用比例和积分控制(PID 回路的 PI 部分)。

虽然 Arduino 有很好的 I/O 引脚选择，但它没有工业控制器中常见的 I/O 功能。例如，演示中使用的流量计产生的电流与 4 mA 至 20 mA 范围内的流量成比例。这是工业设备中非常常见的设置，因为电流环路能够处理长距离走线以及其他原因。[Doug]发现他必须创建一个转换器来将数据传输到 Arduino。他还需要一种方法来将 Arduino 的 PWM 输出转换为 4-20 mA 输出，这甚至更复杂。

当然，PLC 已经有了所有这些选项，以及一个适合该任务的用户界面。由此,[道格]得出结论，虽然基本硬件更便宜，但当你添加辅助组件时，它就已经是废物了。他还认为构建 Arduino 版本项目的工程时间淹没了使用 PLC 的所有成本。

总的来说，我们不反对。然而，这取决于你试图完成什么。锤子擅长钉钉子，但不擅长钉螺丝钉。你需要合适的工具来完成这项工作。如果你真的有 4-20 毫安齿轮，需要一个类似 PLC 的用户界面，那么，当然，PLC 可能是正确的选择。然而，如果您从 Arduino 开始，您可以选择更好的流量监控和执行器，提供更好的功率，使用更适合 Arduino 的用户界面，并获得更好的结果。

不要误解我们。PLC 有一席之地。Arduinos 也是。ARM 芯片、覆盆子 PIs 和 555 定时器也是如此。对于[道格的]项目，PLC 显然是正确的答案。这并不意味着它总是正确的答案。然而，我们确实认为看到两者之间的比较可能有助于 PLC 专家更好地理解 Arduino，反之亦然。

尽管大多数 PLC 都是专有的，我们在之前已经介绍过 [OpenPLC。也许最好的主意不是选择一个或另一个，而是](https://hackaday.com/2016/06/07/openplc-is-ready-for-hacking/)[两者并用，发挥他们的长处](https://hackaday.com/2015/12/18/reading-smart-cards-from-a-plc-with-a-little-arduino-help/)。