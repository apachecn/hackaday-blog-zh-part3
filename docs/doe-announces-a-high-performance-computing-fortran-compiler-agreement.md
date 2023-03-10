# DOE 宣布高性能计算 Fortran 编译器协议

> 原文：<https://hackaday.com/2015/11/21/doe-announces-a-high-performance-computing-fortran-compiler-agreement/>

美国能源部国家核安全局(NNSA)及其三个国家实验室本周宣布，他们已经就高性能计算(HPC)的开源 Fortran 前端达成[协议。协议是和 IBM？微软？谷歌？不，协议是与英伟达，一家为游戏玩家制造显卡的公司。](https://www.llnl.gov/news/nnsa-national-labs-team-nvidia-develop-open-source-fortran-compiler-technology)

图形卡的核心是图形处理器单元(GPU)，它是一个极其强大的计算引擎。它实际上比计算机 CPU 有更大的马力，尽管没有很多人声称的那么大。几年前，NVIDIA 开始为他们的 GPU 提供编译器工具集。显而易见的目标是推动销售。NVIDIA 将使用他们现有的 Fortran 编译器作为起点，并将其与现有的 LLVM 编译器基础设施集成。那个 Fortran，一直在突突前进。

您可以在您的 Raspberry Pi 上尝试 GPU 编程。没错。即使它有一个，一个博通。只要[沿着树莓派游乐场的方向](https://rpiplayground.wordpress.com/2014/05/03/hacking-the-gpu-for-fun-and-profit-pt-1/)走就行了。汇编语言会弄脏你的手，所以这不适合胆小的人。GPU 面临的一大挑战是与它们交换数据，这些数据会进入 DMA 处理。你也可以看看【皮特·沃顿】关于使用 Pi 的 GPU 的[的工作。](http://petewarden.com/2014/08/07/how-to-optimize-raspberry-pi-code-using-its-gpu/)

还在疑惑 CPU vs GPU 的性能？这是亚当·沙维奇在看…

 [https://www.youtube.com/embed/-P28LKWTzrI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-P28LKWTzrI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

