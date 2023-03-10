# 偏置晶体管:共基放大器

> 原文：<https://hackaday.com/2018/05/11/biasing-that-transistor-the-common-base-amplifier/>

我们[之前提到过](https://hackaday.com/2018/04/06/wont-somebody-please-think-of-the-transistors/)有一代人足够幸运，在 Arduino 或 Raspberry Pi 环境中长大，精通微控制器和基于计算机的电子产品，但不幸错过了基本的电子产品，如如何偏置晶体管，为了弥补这一差距，我们看了看晶体管偏置的[基础知识](https://hackaday.com/2018/05/04/biasing-that-transistor-part-1-the-common-emitter-amplifier/)。

我们在上一篇文章中使用的所有电路都将晶体管的发射极接地，从基极获得输入，从集电极获得输出。这种配置称为*共发射极*放大器，可能是最常见的，但这远不是使用晶体管的唯一方式。一旦按照我们描述的方法设置了偏置电压，使晶体管处于线性区域，还有其他几种方法可以将该器件用作放大器。本文的主题是这些配置中的一种，之所以这样描述是因为它将晶体管的基极而不是发射极接地，作为一个*共基极*放大器。

[![The common base amplifier circuit](img/602d2e40a6fc25788afbd5db54769371.png)](https://hackaday.com/wp-content/uploads/2018/05/common-base.png)

The common base amplifier circuit

花点时间考虑一下最基本的共基放大器。晶体管的基极保持恒定的偏置电位，发射极构成放大器的输入，集电极构成输出。DC 偏置配置与我们之前描述的共发射极放大器完全相同，因为基极比发射极高得多，晶体管在其线性区导通，并且有一个发射极电阻来限制通过该器件的电流。发射极电路中有一个小负载，输入端跨接在该负载上，输出来自集电极，与共发射极电路一样。

当通过改变放大器输入来改变发射极的电压时，它反过来改变基极和发射极之间的电压。随着基极和发射极之间的电压变化，基极电流也会变化，这反过来会由于晶体管的增益而导致集电极电流发生更大的变化。这导致集电极电阻上相应较大的电压变化，作为发射极上较小信号的放大版本在输出端可用。

这种工作模式有两个结果，使共基极放大器的特性与其共发射极放大器有很大不同。它是一个电压放大器，而不是电流放大器，它是非反相的，并且在其输入端具有极低的阻抗。

当我们研究共发射极电路时，我们了解了晶体管的基本工作原理，流经其集电极的电流是流经其基极的电流的倍数，该倍数称为其*增益*。因此，在改变基极电流时，我们会在集电极电流中产生相应的更大变化，由此我们可以在集电极电阻上获得放大的电压，但我们总是要求我们的输入是电流源而不是电压源。与共基电路相比，基极电流来自偏置网络，而不是输入，因此输入更像电压源，而不是电流源，因此共基电路是一个电压放大器。

我们上次看到的共发射极放大器是一种反相放大器，因为基极电流增加会导致更多集电极电流流过，从而拉低集电极电压。因此，输入端的电压上升会导致输出端相应的电压下降，正弦波等周期性波形通过时会发生反转。另一方面，共基极放大器对发射极(其输入端)上增加的电压作出反应，消耗较少的电流，输出端上剩余的电压增加。

最后，共基极放大器的输入阻抗远低于其共发射极等效阻抗。晶体管放大器的集电极电路可以是非常低的电阻，也可以是具有零电阻 DC 路径的电抗电路。相比之下，共发射极放大器的基极电路及其电阻网络的阻抗要高得多。大多数情况下，共发射极放大器输入的高阻抗相对于共基极配置的低阻抗而言是一个巨大优势，因为它不会给提供其输入的电路带来负载，但在需要与低阻抗源进行阻抗匹配的情况下，共基极放大器的低阻抗会成为一个优势。因此，在匹配低阻抗馈线的小信号 RF 放大器中，以及动圈式麦克风等低阻抗音频源的放大器中，您会发现常用的基极放大器。由于这个原因，[模拟电视调谐器](https://hackaday.com/2016/07/11/not-quite-101-uses-for-an-analog-uhf-tv-tuner/)中的天线前置放大器通常采用共基设计。

除非使用 RF，否则您可能永远也不会构建共基放大器，但当您需要低阻抗输入的电压放大器时，它仍然是一种有用的配置，是您电路库中的一件便利武器。在使用场效应晶体管(FET)检查等效电路之前，我们将继续讨论晶体管放大器的最终配置，即共集电极放大器或射极跟随器。