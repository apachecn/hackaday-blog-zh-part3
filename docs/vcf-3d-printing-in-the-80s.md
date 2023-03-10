# VCF:80 年代的 3D 打印

> 原文：<https://hackaday.com/2017/04/02/vcf-3d-printing-in-the-80s/>

东老式电脑节正在进行，我被 20 世纪 70 年代和 80 年代的科技高峰所包围。奇怪的是，Hackaday 经常涉及*80 年代的另一项*技术，尽管你不会这样认为。3D 打印发明于 20 世纪 80 年代末，由于专利只有 20 年左右，这意味着 3D 打印在 2000 年代开始流行

20 世纪 70 年代，第一台个人电脑出现在车库里。21 世纪初，第一台 3D 打印机出现在车间和黑客空间。这些相似之处提出了一个有趣的问题——有可能建造一台由当代计算机控制的 20 世纪 80 年代的 3D 打印机吗？这是本周末在老式电脑节上哥伦布创意铸造厂的 Ethan Dicks 谈论的焦点。

 [![MBElectronics](img/371ec3414ea6fee704b96d3ad8bc0238.png "MBElectronics")](https://hackaday.com/2017/04/02/vcf-3d-printing-in-the-80s/mbelectronics/)  [![The serial number](img/a618c4e6e0a77f79bd8bdb09788b5cc2.png "Serial")](https://hackaday.com/2017/04/02/vcf-3d-printing-in-the-80s/serial-3/) The serial number [![Revar's LCD mod](img/c410ecd2c1ee2e96cbed5ee6fa317289.png "Revars")](https://hackaday.com/2017/04/02/vcf-3d-printing-in-the-80s/revars/) Revar’s LCD mod [![Ethan's test bench of electronics](img/3a1ae19fbfe9eb285154bdd21d7ac3af.png "TestBench")](https://hackaday.com/2017/04/02/vcf-3d-printing-in-the-80s/testbench/) Ethan’s test bench of electronics

第一，硬件。[Ethan]的测试平台包括一个 Commodore PET 型号 8032，运行 1MHz 6502，配备 32k 内存，并通过总共有 8 个数字输出的“用户端口”与外界连接。

这次演讲的打印机样本是一个 MakerBot 纸杯蛋糕。不，纸杯蛋糕不在工作状态。毕竟，一个工作中的 MakerBot 纸杯蛋糕[是一个有新闻价值的事件。然而，对于简单的 3D 打印机来说，这实际上是一个不错的选择。这台打印机只有三个步进电机，每个驱动器只需要一个步进和方向信号。纸杯蛋糕真的不需要终点挡板，挤压机只是一个 DC 马达，加热床是一种奢侈品。总的来说，你需要大约八个控制信号来运行这台打印机的电机，一个或两个控制信号来打开和关闭加热器，以及一个模拟输入。再加上](http://hackaday.com/2017/03/27/mrrf-17-a-working-makerbot-cupcake/) [Revars LCD mod](https://web-beta.archive.org/web/20100729170629/http://wiki.makerbot.com/revarlcd-assembly) (从 MakerBot 删除，但是 Wayback 机器抓到了)，你就可以带着宠物轻松控制打印机了。

虽然可以用 6502 控制打印机的电机，但这并不容易。为纸杯蛋糕开发的电子板——Sanguinololu(T1)使用 16MHz 的 ATMega644。PET 中的 6502 运行在 1MHz，但它变得更糟:ATMega 上的许多指令只需要一个时钟，而 6502 每条指令需要几个时钟。6502 根本不具备像 3 美元的微控制器那样快速遍历代码的能力。

还有如何在老式电脑上存储 3D 可打印文件的问题。今天，简单的 STL 文件达到兆字节并不罕见。一个复杂的模型不可能存在老式硬盘里。

[伊森]有一些解决这些问题的方法。他不能真正绕过 PET 的处理速度，但他确实有一个 STL 立方体大小的解决方案。在切片过程中，立方体的 3D 可打印文件被分割成多个层。底层是实心的，中间层有周边和填充图案，顶层也是实心的。不是处理一个几兆字节重的文件，[Ethan]只是简单地取几个底层、一个中间层和顶层，并通过一个 for 循环运行它们。

[Ethan]能和宠物一起研磨 MakerBot 发动机吗？可惜没有。理论是存在的，即使分割一个模型远远超出了这个黑客的范围。尽管如此，至少有可能在 80 年代的电脑周围建造一台 3D 打印机。你只需要看看原始专利就能找到证据。