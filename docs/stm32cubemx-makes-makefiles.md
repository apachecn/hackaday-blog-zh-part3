# STM32CubeMX 制作 Makefiles

> 原文：<https://hackaday.com/2017/07/15/stm32cubemx-makes-makefiles/>

当硬件制造商制作 GUI 代码生成工具时，生成的文件通常看起来像一辆翻倒在高速公路上的罐装意大利面卡车——到处都是隐喻性的煮过头的面条和红酱。有时候我们认为他们故意这样做是为了把你绑在他们的 IDE 里。st 的图形 STM32CubeMX 的最新版本并非如此，它会引导您完成一个愉快的 pin 分配过程，然后转储出一个干净的 Makefile。

是的，没错。这是一个制造商软件套件，它输出的东西实际上可以用于任何编辑器、GUI、编译器或您希望的环境，甚至是命令行。在这个版本之前，你必须通过一个[粗糙但功能强大的脚本](https://github.com/baoshi/CubeMX2Makefile)才能从 CubeMX 中获得 Makefile。现在有了对真正黑客的官方支持。谢谢你，圣！

如果你自己编译，你需要更新`BINPATH`变量来指向你的编译器。(我们自己使用优秀的 [GNU ARM 嵌入式工具链](https://launchpad.net/gcc-arm-embedded/+download)，它非常容易安装在几乎任何 Linux 上。)如果你想在 Eclipse IDE 上使用 STM32CubeMX，【kali prasad yadav】给我们发来了 [PDF 指令](https://hackaday.com/wp-content/uploads/2017/07/tutorial.pdf)——不难。

如果你怀疑一个免费的、开放的、不受限制的工具链的可用性对一个芯片厂商来说有多重要，我们会提到 AVR 和 Arduino 平台，它们是从对 GCC 的支持中分离出来的。当然，Atmel 仍然在推他们的一体化奇迹，Atmel Studio，它比 Arduino IDE 好得多。但是 Studio 是关闭的，Arduino 是开放的。我们很想看看 Studio 用户与 Arduino 用户的对比。

祝贺 ST 在开放工具链的正确方向上迈出了一大步。