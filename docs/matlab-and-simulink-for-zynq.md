# Zynq 的 MATLAB 和 Simulink

> 原文：<https://hackaday.com/2017/05/05/matlab-and-simulink-for-zynq/>

尽管我们看到 MATLAB 在工业和学术界有很多应用，但它在黑客社区中并不流行。那大概是成本的原因吧。如果你想知道为什么公司会为基础产品支付超过 2000 美元，你可能会喜欢网上研讨会的[视频，该视频介绍了如何使用 MATLAB 和 Simulink(一种配套产品)对 Zynq Zedboard 上的 CPU 和 FPGA 进行编程。因为价格不感兴趣？如果你不把它用于商业目的，它并没有你想象的那么糟糕。](https://www.youtube.com/watch?v=iSAtwQt9dYM)

MathWorks 是一家喜欢通过向学生虚拟赠送产品来进行营销的公司，希望他们在行业中找到工作时会采用相同的工具。他们的旗舰产品 MATLAB 在大公司的实验室和办公室里根深蒂固。我们经常认为，如果 FORTRAN 是在过去 20 年而不是 60 年前开发的，那么 MATLAB 就会是这样。诚然，MATLAB 的基本许可证超过 2000 美元。然而，如果你不是出于商业目的使用它，并且你不能获得学生许可证，你可以花大约 150 美元获得 MATLAB 的个人许可证。额外的模块也同样降低了价格。如果你是学生，价格会降到 100 美元左右，尽管许多学校都有许可证，学生可以免费使用。

如果你看了诺姆·莱文的视频，你会发现你的钱花得值。如果你想直接配置 FPGA，这不适合你。但如果你只是想通过推送 DSP 或其他可以受益于硬件辅助的算法来加速一个程序，MATLAB 让它变得非常容易。

当然，这个工作流程是针对大型企业团队的。在一个团队中进行协作是有要求和工具的。即使对一个黑客项目来说，这些也不是坏事。基本原理是使用 Simulink 建立一个模型，从很高的层面来观察系统。

GUI 允许您指出模型的哪些部分实际位于 FPGA 中，向导会带您完成构建将配置 FPGA 的 HDL。示例项目是典型的闪烁 LED，但它仍然说明了该工具如何帮助您将功能推送到 FPGA。

当然，MATLAB 对很多事情都有好处。我们已经看到它解码来自 RTL 电子狗的无线电信号。我们也看到它处理数据来[帮助脊髓损伤患者](https://hackaday.com/2017/01/10/recording-functioning-muscles-to-rehab-spinal-cord-injury-patients/)。值 2000 美元吗？看情况。如果你的时间有价值，你的项目会赚钱，生产率的提高(一旦你知道你在做什么)可能会很快淹没成本。几百美元的个人版就更少了，但话说回来，它没有回报，因为你不能用它来赚钱。

如果你只是需要数字运算，又不想花几百块钱，那么有不少不错的开源替代品，包括 [GNU Octave](https://www.gnu.org/software/octave/) 、 [Scilab](http://www.scilab.org/) (以及 [Scicos](http://www.scicos.org) )、 [SageMath](http://www.sagemath.org/) 和 [FreeMat](http://freemat.sourceforge.net/) 。就语法和基本功能而言，这些都非常类似于 MATLAB。许多甚至可以在云中运行，所以你不需要安装任何东西。但是他们可能会缺少你在 MATLAB 中可以找到的高级工具箱和特性。然而，其中一些确实有一些基于 FPGA 的开发途径。特别是 Scicos 和 Scilab 可以使用 [Scicos-HDL](http://scicoshdl.sourceforge.net/) 。

 [https://www.youtube.com/embed/iSAtwQt9dYM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iSAtwQt9dYM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

