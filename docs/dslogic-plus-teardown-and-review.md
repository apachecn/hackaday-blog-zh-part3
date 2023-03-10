# DSLogic Plus 拆卸和检查

> 原文：<https://hackaday.com/2017/08/24/dslogic-plus-teardown-and-review/>

DSLogic 开源逻辑分析仪已经发布了第二版(plus 版本),[OpenTechLab]对新型号进行了[全面评估](https://www.youtube.com/watch?v=xZ5wKYnCNcs&t=2s),与原始型号不同，新型号包括一种不同的探针连接方法，并为每个输入引脚提供了单独的接地。

该设备非常简单，内置一个 FPGA、一个 RAM 和一个 USB 微控制器。还有一个配置 EEPROM 和一个开关电源。该设备内部存储高达 256 兆位，每秒可以在 16 个通道中的 4 个通道上采样 4 亿个样本。[OpenTechLab]甚至将电路板放在显微镜下，绘制出输入电路。

与许多 USB 逻辑分析仪不同，探头和专用接地的新排列允许探头使用非常短的跨线连接到一根薄同轴电缆。这改进了逻辑分析仪，但[OpenTechLab]指出，如果没有端接电阻，探针会修改信号，他甚至展示了这种效果的模拟，以及普通飞线探针和 DSLogic 提供的探针的实际比较。

[OpenTechLab]是 Sigrok 的积极贡献者，他讨论了最初的 DSLogic 软件如何成为 Pulseview 的未授权分支，并删除了所有 Sigrok 许可和品牌。一些视频涉及 DSView 软件的争议性地位，该软件最初的名称是 PulseView。

我们回顾了 2015 年[的原始版本](http://hackaday.com/2015/05/26/review-dslogic-logic-analyzer/)。逻辑分析仪比以前更简单，这既是因为你很少能接触到太多的内部连接，也是因为[廉价 FPGA 硬件](http://hackaday.com/2016/12/13/compiling-a-22-analyzer/)的可用性。

 [https://www.youtube.com/embed/xZ5wKYnCNcs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2&wmode=transparent](https://www.youtube.com/embed/xZ5wKYnCNcs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2&wmode=transparent)

