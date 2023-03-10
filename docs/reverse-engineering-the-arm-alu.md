# ARM ALU 的逆向工程

> 原文：<https://hackaday.com/2015/12/21/reverse-engineering-the-arm-alu/>

[Dave]想了解更多关于 ARM 架构的知识，所以他从 ARMV1 芯片的图片开始。如果你有观察 CPU 芯片的经验，你可以很好地猜测芯片的哪些部分有特定的功能。然而，[戴夫]走得更远。他对整个 ALU 进行了逆向工程——大约有 2200 个晶体管。

[![arm600](img/65f075c0601b0dc48dcfb47cccdec87e.png)](https://hackaday.com/wp-content/uploads/2015/12/arm600.png) 从图像中，他算出了晶体管的结构以及它们如何映射到栅极。因为 ARM 是 32 位处理器，所以 ALU 有 32 个独立的片，每个片有大约 70 个晶体管(见下文)。在支持零和进位传播方面，某些片之间存在细微差异。PLA 产生控制信号，该控制信号通过 ALU 路由数据以执行期望的操作。

[戴夫]的灵感来自于[visual 6502 项目](http://hackaday.com/2010/09/19/hackaday-links-september-19-2010/)以及[肯·希尔里夫的][T2 的]8085 逆向工程，这两个项目我们过去都报道过。如果 FET 晶体管逻辑不合你意，你可以试试[《我的世界》](http://hackaday.com/2012/05/20/building-a-6502-in-minecraft/)。

[![alu](img/fb360ac55783b2a0553dfdba35d33886.png)](https://hackaday.com/wp-content/uploads/2015/12/alu.png)