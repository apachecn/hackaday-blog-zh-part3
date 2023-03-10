# 本周失败:NASA 版

> 原文：<https://hackaday.com/2017/01/11/fail-of-the-week-nasa-edition/>

我们经常使用“这不是火箭科学”这句话是有原因的。因为真正的火箭科学很难。它既危险又复杂，很多事情都可能出错，而且确实出错了，往往会带来灾难性的后果。必须记录和传播从过去的失败中吸取的教训，以防止未来的灾难。这说起来容易做起来难。有大量的机构和实验室在长时间内从事多个项目。这就是为什么 NASA 建立了 [NASA 经验教训](https://www.nasa.gov/offices/oce/functions/lessons/index.html)——一个由 NASA 内部以及其他组织的贡献者记录的问题的中央在线数据库。

该系统由一个指导委员会管理，该委员会由来自 NASA 所有中心的成员组成。公众访问仅限于原始驾驶事件、经验教训和建议的总结。但是即使这些信息对普通人来说也是非常有用的。例如，这堂关于美国宇航局选择 DC-DC 转换器应用指南的课包含了一些有用的智慧。或者是关于组装时[电容残放](https://llis.nasa.gov/lesson/297)导致 IC 损坏的问题。如果你需要给你的硬件添加保形涂层，检查[玻璃外壳组件是如何由于过量使用涂层/粘合材料收缩而破裂的](https://llis.nasa.gov/lesson/460)。最后，我们在处理极化元件时都经历过的一件事是[钽电容的反极性问题](https://llis.nasa.gov/lesson/981)。这里有一个关于极化电容器的更具体的技术说明(pdf): [防止极化电容器的错误安装](https://www.nasa.gov/sites/default/files/atoms/files/nesc_tb_15-01_preventing_incorrect_installation_of_polarized_capacitors.pdf)。

不幸的是，所有这些过去的知识有时仍然不足以预防问题。一个恰当的例子是最近在国际空间站发现的一个问题——一个完全可以避免的电源错误。科学有效载荷通过称为[快递物流载体](https://en.wikipedia.org/wiki/ExPRESS_Logistics_Carrier)的支架连接到国际空间站。这些提供机械锚定、电力和数据链接。在运载工具内部，为有效载荷提供 28V 电压的电源被发现反过来安装了几个电容器。这迫使有效载荷使用 120V 电源，要求它们具有额外的 120V 到 28V 转换器改型。这意味着修改现有硬件，并在添加额外转换器时考虑额外的重量、体积、热量、成本和其他问题。如果你想深入了解细节，可以看看这篇关于[美国宇航局电源故障](https://www.wired.com/2016/12/nasa-made-really-dumb-mistake-iss-power-supply/)的文章。

感谢[Jarek]给我们这个提示。