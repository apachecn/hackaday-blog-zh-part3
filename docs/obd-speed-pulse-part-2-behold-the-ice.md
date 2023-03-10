# 建立 OBD 速度脉冲:看冰

> 原文：<https://hackaday.com/2017/05/09/obd-speed-pulse-part-2-behold-the-ice/>

说到这个，我是一个蹩脚的软件程序员。当一切都面向对象时，我没有注意，反正我的根总是汇编语言和实时操作系统(RTOS)。

因此，很自然地，我将达到一个真正的在线仿真器(冰)来完成我的小 OBDII 总线速度脉冲发生器部件。ICE 是用于调试嵌入式系统的硬件设备。它与主板上的微控制器通信，允许您通过暂停执行、检查或更改硬件寄存器中的值来查看发生了什么。如果你想在嵌入式开发方面表现出色，你需要擅长使用在线仿真。

我不仅可以几乎实时地看到我的错误，还可以制作一个视频。

### 从车辆中获取数据

我一直在研究一个小的插件板，它可以插到我的汽车上，直接访问控制器局域网(CAN 总线)上报告的速度。

稍微回顾一下，[我的上一个视频帖子](http://hackaday.com/2017/02/15/obd-and-asking-the-question-how-fast-am-i-going/)是关于我的一个愚蠢的愿望:做一个小组件，可以插入我卡车上的 OBDII 端口，并创建一系列代表车辆速度的脉冲，以便我的 GPS 更准确地工作。虽然有一根电线深埋在连接到车辆发动机控制模块的多束电线中，但出于多种原因，我决定创建自己的信号源。

我项目的核心是需要将 OBDII 端口和底层 CAN 协议转换为一个简单的速度变量，然后将该值转换为一个脉冲流，其中频率根据速度而变化。OBDII/CAN 协议由 STN1110 芯片处理并转换为 ASCII，我使用的是 ATmega328，就像在众多 Arduino'ish 板上找到的一样，用于 ASCII 到脉冲的转换。我使用硬件中断来控制信号输出，实现坚如磐石、无抖动的时序。

在下面的视频中演示使用在线仿真器的过程，休息后请和我一起了解更多细节。

 [https://www.youtube.com/embed/lYhiwI_akoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lYhiwI_akoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 硬件

自从上一个视频以来，我修改了电路板，并删除了对除 CAN 之外的各种协议的支持，CAN 是一系列协议中尚未过时的协议。通过移除一些部件，我能够将封装风格改为通孔封装，这对许多家庭爱好者来说更容易，所以你可以将锡膏放在冰箱里。

[![](img/0a10665d1514739643675aa4ae5110c5.png)](https://hackaday.com/2017/05/09/obd-speed-pulse-part-2-behold-the-ice/pcb-3d/)

Rev 2

[![](img/7eb68d786fe1943298b8f0fb265b122c.png)](https://hackaday.com/2017/05/09/obd-speed-pulse-part-2-behold-the-ice/600-600-12/)

Rev 1

## Arduino 上的“另一个连接器”

不像 Arduino，当你把它从盒子里拿出来时，它已经准备好与你的 USB 端口对话，ATmega 芯片到达时没有任何如何去下载代码的知识，换句话说，它没有引导加载程序。因此，我将在线串行编程(ICSP)引脚连接到电路板上的一个引脚接头，这样我就可以直接对器件进行编程。

在这个连接器上，你会发现复位线，这意味着有了这个标题，我可以使用一个真正的冰利用 debugWIRE 协议。由于使用 AVR 芯片的绝大多数设计都没有将 reset 引脚用于 GPIO，因此它是用于 ICE 的理想引脚。调试过程中的所有通信都将发生在 reset 引脚上。

 [![ICE-Rev2](img/39d7d28745d77140b0bb788d0a092c2e.png "ICE-Rev2")](https://hackaday.com/2017/05/09/obd-speed-pulse-part-2-behold-the-ice/ice-rev2/)  [![ICE Arduino 2](img/86b1aa6cf0b7fe0fea0644e65b844042.png "ICE Arduino 2")](https://hackaday.com/2017/05/09/obd-speed-pulse-part-2-behold-the-ice/ice-arduino-2/) 

## 进入冰中

当从头开始设计一台计算机时，总会有一个阶段什么都不能工作。简单地说，一个微处理器电路只有在设计的几乎每个部分都正常工作时才能工作；RAM、ROM 和底层总线都需要(大部分)工作，然后才能做简单的事情。作为一名硬件工程师，我总是会伸手拿一块冰来启动实现；只有在测试版发布后，冰才会开始在角落里积灰。

在 ATmega 的情况下，调试功能内置于微控制器本身。与早期相比，这是一种更简单的实现方式，当时我们必须有第二个独立的处理器在板外运行，并带有自己的本地 RAM/ROM。

视频中提到的一点是，标准 Arduino'ish 板需要从复位线路中移除滤波电容，以允许线路上的高速数据供其 debugWIRE 使用。

我在这里使用的冰是由 Atmel 制造的，并与 Atmel Studio 兼容，也有其他型号，如 AVR Dragon。

## 冰冷

ICE 允许我们下载和单步执行我们的代码，同时能够从键盘观察和重写 RAM 和 I/O 寄存器。我们能够一步一步地观察程序，或者从根本上看编译器生成的实际汇编代码。我们可以直接在 RAM 中观察变量和位置，或者观察 C 语言中的对应物。在只想看到结果而不想看到所有处理的情况下，也可以跳过一个子程序调用。

即使只是看一眼 ICE 的运行能力，也是值得的。我建议您[观看调试开始的视频](https://www.youtube.com/watch?v=lYhiwI_akoE&t=13m29s)。

## 最后的话

这个视频实际上是关于完成 OBDII 赛道的，所以我真的没有时间去回顾 ICE 能做的一切，也许下次我会专门写一篇关于 ICE 和开发环境的文章。