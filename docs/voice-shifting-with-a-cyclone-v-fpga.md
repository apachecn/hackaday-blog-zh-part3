# 利用 Cyclone V FPGA 进行语音转换

> 原文：<https://hackaday.com/2017/06/18/voice-shifting-with-a-cyclone-v-fpga/>

康奈尔大学的学生[Sean Carroll]、[Gulnar Mirza]和[James Talmage]设计了一个[实时音高移位器](http://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2017/jmt329_swc63_gzm3/jmt329_swc63_gzm3/PitchShifter/index.html)，在他们的 DE1-SoC 上运行，并由其 ARM 内核控制。

该团队的目标是独立地对左右输出进行音高移位，使用原始声音以及音高移位的声音和延时音高移位来产生和弦。所有这一切都是通过一个简单的 GUI 在 VGA 显示器上控制的，允许用户通过分层不同的选项来创建许多不同的效果。

在引擎盖下，他们利用双循环缓冲器来进行音高移位，读取样本，然后使用简单的定点运算来修改它，然后让信号通过巴特沃兹滤波器来清除伪像。

该项目是作为[Bruce Land]的 ECE5760 级的一部分建造的。如果你正在寻找更多的好处，你会在 Hackaday 上找到大量优秀的项目，包括去年的 [LED 矩阵音频可视化器](http://hackaday.com/2016/06/13/fpga-powers-blazingly-fast-led-matrix-audio-visualizer/)和[在 Cyclone V](http://hackaday.com/2017/05/18/synthesizing-strings-on-a-cyclone-v/) 上合成字符串，等等。

 [https://www.youtube.com/embed/VeT4ikeRbic?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VeT4ikeRbic?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

