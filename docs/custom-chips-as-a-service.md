# 定制芯片即服务

> 原文：<https://hackaday.com/2018/04/24/custom-chips-as-a-service/>

很久以前，制作定制电路板很难。要么你不得不去 Radio Shack 买些唱片，要么你花了一大笔钱和一个板房谈话。现在，多氯联苯是如此便宜，我正在考虑用它们来贴我的浴室。如今，定制芯片的成本高得吓人。理论上你可以在家里制造晶体管，但是任何更多的东西都需要石英管加热器和氢氟酸。定制 ASICs 对于家庭黑客来说是遥不可及的，除非你从一些加密庞氏骗局中捞钱。

现在情况可能正在改变。成本正在下降，软件工具链正在实现，在芯片上，开源 32 位微控制器的制造商现在正在致力于所谓的“硅的 OSH 公园”。他们称之为 Itsy-Chipsy ，它有望以低至 100 美元的价格带给你自己的芯片。

这个商业计划的灵感来自于像 MOSIS 这样的服务，它允许大学班级在多项目晶片上设计他们自己的芯片。这将多个芯片聚集到一个晶片上，将原型的成本从数万美元降低到大约 5000 美元，或者一个芯片大约 1000 美元。

Itsy-Chipsy 将这种批处理向前推进了一步。这是一个在一个芯片上结合多个项目的平台。这个一千美元的芯片现在是 16 个不同的项目，与调节器、电流源、时钟和过程监控器联系在一起。Itsy-Chipsy 使用 2 毫米乘 2 毫米的芯片尺寸，使用 180 纳米 CMOS 工艺为芯片设计者提供 350 微米的硅。这对于一个 QFN 或 DIP 40 中的基本 32 位 RISC-V 微处理器来说，只需 100 美元就足够了。

这个项目是 Hackaday 奖的竞争者——该奖将于 11 月结束，届时我们会惊讶地看到结果。不过，Onchip 团队正在与代工厂洽谈，看起来业界对这种模式很感兴趣。我们猜测，最好的情况是在 2019 年的某个时候为一个类似奥什公园的芯片厂进行众筹。无论何时到来，这都是我们热切期待的。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)