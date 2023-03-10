# MIDI 到 CV/Gate 的简单方式

> 原文：<https://hackaday.com/2017/09/30/midi-to-cvgate-the-easy-way/>

假设你有一个模块化合成器。你可能是个很酷的人。但是你所有的酷酷的笔记本电脑 DJ 朋友一直在炫耀他们的 MIDI 控制的硬件，你开始嫉妒了。嗯，[小规模]有适合你的体型。

Teensy 3.6 是目前来自 PJRC 的顶级 Teensy，它是[小规模]的首选武器。凭借 USB-MIDI 和两个 12 位 DAC，在模拟和数字音乐世界之间创建接口变得非常简单。俯仰和速度的控制电压通过模拟引脚输出，而引脚 29 用于门信号。

这是对进入 Teensy 平台的开发量的一个证明，这样的项目可以在几乎没有非机载组件的情况下构建。与[little-scale]之前的工作[相比，该构建在简单性上又向前迈进了一步，使用一个 Teensy 2 和一个片外 DAC 来产生输出电压](https://hackaday.com/2017/01/09/midi-dac-for-vintage-synth-hacks/)。

在 Hackaday，我们一直热衷于为模拟硬件添加计算机控制。这个吉他拾音器绕线机的 CNC 模块就是一个很好的例子。