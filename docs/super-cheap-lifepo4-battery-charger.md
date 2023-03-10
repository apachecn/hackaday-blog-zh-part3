# TL431 的颂歌和 LiFePO4 电池充电器

> 原文：<https://hackaday.com/2016/01/08/super-cheap-lifepo4-battery-charger/>

呆子拉尔夫喜欢廉价和肮脏的黑客，因此我们为他鼓掌。他最近的努力是用手头上不到 0.5 美元的零件做了一个 LiFePO4 电池充电器。(虽然我们认为他真的是为了制作的乐趣而制作的。)

该电路以一个 [TL431 可编程分流调节器](http://www.ti.com/product/tl431)为中心，这是一个令人敬畏但被低估的芯片。如果你不知道 TL431(又名 LM431)，你应该自己去获取数据手册，并在下一个电子产品订单中挑选一些。事实上，这是一款非常棒的芯片，我们忍不住要向您介绍一下。

## TL431

 [![tl431_symbol](img/bd48ccfa2fde81451122a3b7c45c44a0.png "tl431_symbol")](https://hackaday.com/2016/01/08/super-cheap-lifepo4-battery-charger/tl431_symbol/)  [![tl431_block_diagram](img/6abfa1e975a53e8d8d7dd31efe422ff6.png "tl431_block_diagram")](https://hackaday.com/2016/01/08/super-cheap-lifepo4-battery-charger/tl431_block_diagram/) 

尽管 TL431 的电气符号具有误导性，但请将其视为电压激活型开关晶体管。当参考引脚上的电压低于 2.5V 时，晶体管不导通。当基准引脚上的电压高于 2.5V 时，晶体管充当闭合开关，向地吸收约 100 mA 的电流。

如果将基准引脚连接到阴极，TL431 *的表现就像一个击穿电压为 2.5 V 的齐纳二极管，但这是在低估它。TL431 是一款成熟的 IC，内置精密电压基准、比较器和有源晶体管。在基准引脚和阴极上施加不同电压的能力非常有趣。*

[![led_version.sch](img/444204e214f79a77bb6d0fb19c54e415.png)](https://hackaday.com/wp-content/uploads/2016/01/led_version-sch1.png) 在最简单的电路中，你可以用 TL431 驱动一个 LED。将一个 LED 和一个限流电阻连接到 TL431 的阴极，并将阳极接地。然后，当基准上的电压高于 2.5V 时，LED 将明亮地亮起。2.5V 你不感兴趣？您可以添加一个分压器，将阈值提高到您想要的 2.5 V 以上的任何值。这里显示的是一个 LED，只有当输入为 5V 或更高时才会亮起。你可以在任何需要电压激活开关的地方使用这个想法，例如作为电池的低压监控器。

## 电池充电器和反馈

TL431 作为一个开关很好，但它依赖于[反馈](https://en.wikipedia.org/wiki/Negative_feedback)。要用这里显示的 LED 电路制作一个电压调节器，你需要做的就是在 LED 的位置上增加一个晶体管；让 TL431 在电压低于目标电压时打开晶体管，在电压高于目标电压时关闭晶体管。事实上，几乎所有 TL431s 都是基于这种廉价且令人愉悦的电压调节器应用——在开关电源中提供电压调节。事实上，你的电脑电源里可能已经有几个了。

[![431_shunt.sch](img/3d7538225779099fef8e941dff1b2d76.png)](https://hackaday.com/wp-content/uploads/2016/01/431_shunt-sch2.png) 那么让我们回到讷瑞夫和他的电池充电器上来。拉尔夫的简单电池充电器本质上就是这个简单的稳压电路。他选择电压设置电阻`R1`和`R2`，当输出为 3.6 V 时，在 TL431 上为其提供 2.5 V 的电压，这是 LiFePO4 电池基本完成充电的电压。

要查看 TL431 的运行情况，首先假设它不导电(关闭)。电流从电源通过`RB1`流入晶体管，开启晶体管。`Vout`处的电压增加，电池充电，分压器中间的电压成比例增加。当达到 2.5 V 阈值时，TL431 开启并汲取电流，剥夺晶体管的基极电流，同时点亮 LED。

因为磷酸铁锂电池[喜欢以恒定电流](http://www.powerstream.com/LLLF.htm)充电，几乎达到其范围的极限，Ralph 选择了晶体管的基极电阻`RB1`来限制输送到电池的最大电流。他测试了半充电电池的输出电流，以验证他是在正确的范围内。

现在，我们并不完全相信这是一个恒流充电器电路。毕竟，基本电路是一个电压调节器。依靠晶体管的[电流增益](https://en.wikipedia.org/wiki/Bipolar_junction_transistor#Transistor_parameters:_alpha_.28.CE.B1.29_and_beta_.28.CE.B2.29)在整个温度范围内或不同晶体管之间保持恒定有点粗略——例如[电子技术](http://www.artofelectronics.com/)明确警告你电流增益值的可变性。但是与其他锂电池相比，LiFePO4 电池看起来非常坚固，电压曲线仅在 10%充电时的 3.4 V 到 90%充电时的 3.6V 之间变化。足够稳定。

它还缺少一些我们喜欢在其他 LiPO 充电器中拥有的东西，如电池温度感应和充电完成后断开连接。但同样，磷酸铁锂电池足够坚固，可以过度充电，如果他不把电池放在充电器里很长时间，他可能会逃脱。毕竟是个黑客。

## 荣誉和评论

[![TL431 in its natural environment: a cheap switching power supply](img/37e8bf23f20d9e66c7e16828838b8757.png)](https://hackaday.com/wp-content/uploads/2016/01/dscf8153.jpg)

TL431 in its natural habitat: next to an optoisolator in a cheap switching power supply

首先，我们要感谢拉尔夫提醒我们极简主义电子产品的一个非常有用的部分。TL431 的数据手册中有很多很酷的应用，在几分钟的硅片中集成了基准电压源和比较器驱动晶体管的功能。如果您的项目中需要电压触发开关，现在您知道去哪里找了。

Ken Shirriff 写了一篇非常好的 TL431 解剖图，其中包括芯片图像。对于 TL431 的真正深奥的使用，这里有一个水晶收音机设计，[滥用 TL431 作为音频放大器](http://www.techlib.com/electronics/crystal.html#AudioAmp)。

你觉得拉尔夫的充电器设计怎么样？你对 TL431 有什么特别喜欢的小技巧吗？你认为哪块硅片是未经加工的未知宝石？请在评论中告诉我们，并[发送一个提示](http://hackaday.com/submit-a-tip/)来获取您希望在未来看到的部件。