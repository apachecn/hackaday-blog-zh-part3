# 推出自己的 Arduino PWM

> 原文：<https://hackaday.com/2017/11/12/roll-your-own-arduino-pwm/>

大多数项目都建立在抽象的基础上。毕竟，我们中很少有人能创造出自己的电线、自己的晶体管或自己的集成电路。几个月前，[Julian Ilett]在使用 Arduino 库进行 PWM 时发现了一个问题。最近，他重新审视了这个问题，并使用[他自己的 PWM 代码](https://www.youtube.com/watch?v=IMm0-gGkRi0)来解决这个问题。可以看下面的视频。

当然，无论是 Arduino 库还是[Julian 的]代码实际上都没有产生 PWM。Atmel CPU 的硬件正在做这项工作。Arduino 库为您提供了一个名为 analogWrite 的包装器——如果您不使用 Atmel CPU，而在 Atmel CPU 中相同的抽象将完成相同的工作，这将非常方便。当[Julian]打破抽象来反转 PWM 输出时，问题就出现了。

该视频很好地阐述了这个问题。将 PWM 硬件设置为零仍会导致出现一个节拍的输出。也就是说，实际计数是您提供的计数加 1。在 256 分中，255 分被视为 256 分，这在高端市场非常好。但在低端，零违反直觉地给你 1/256。Arduino 库作者选择检测这种边缘情况，并在这种情况下强制输出引脚变为低电平。然而，当反转时，该引脚在应该变高的时候仍然变低。你可以在下面看到负责任的源代码。

```
pinMode(pin, OUTPUT);
if (val == 0)
  {
  digitalWrite(pin, LOW);
  }
else if (val == 255)
  {
  digitalWrite(pin, HIGH);
  }
else
{ ...
```

奇怪的是，在正常情况下，255 的大小写看起来是多余的，但是如果你把输出反过来，它也是多余的。平心而论，Arduino 库没有为您提供反转输出的方法，所以您已经打破了抽象，这就是为什么这在技术上不是库中的错误。

[朱利安的]代码很简单。TCCR1A 和 TCCR1B 寄存器与 ICR1 一起进行初始设置。DDRB 寄存器将引脚设置为输出。之后，写入 OCR1A 和 OCR1B 设置 PWM 值。视频非常详细地解释了这一切。

我们已经至少看过一次 FPGA 上的 [PWM，这篇文章给出了任何应用中 PWM 的一些背景知识。我们还有](https://hackaday.com/2015/12/16/taking-the-pulse-width-modulation-of-an-fpga/)[2011 年关于 PWM 的视频](https://hackaday.com/2011/10/27/video-pwm-on-the-atmega328p/)。

 [https://www.youtube.com/embed/IMm0-gGkRi0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IMm0-gGkRi0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

