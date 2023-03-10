# 引发革命的导电纸

> 原文：<https://hackaday.com/2015/09/28/the-conductive-paper-that-sparked-a-revolution/>

传奇电气工程师和线性 IC 先驱 [Bob Widlar](http://hackaday.com/2014/04/08/heroes-of-hardware-revolution-bob-widlar/) 就像你一样。我的意思是，他会利用一切可以利用的东西来模拟电路，创造原型，并使之工作。他使用的最简单也是最酷的工具之一是[，一种叫做 Teledeltos](http://electronicdesign.com/analog/whats-all-teledeltos-stuff-anyway) 的导电纸。这个奇妙的东西让他能够定义和测试他在一些高性能电路设计中使用的异形镇流电阻的各种配置。但它不是为你和鲍勃这样的人创造的。Teledeltos 纸是由通信巨头西联公司创造并注册的，目的是为了极大地提高电报的便利性。

电报的发展开创了全球通信的时代。突然之间，人们可以把信息发送到世界的另一端，只需要邮寄时间的一小部分。电报彻底改变了人类的交流方式。这是那个时代的电子邮件和推特。电报的效率使得驿马快信在 19 世纪 60 年代就已经过时了。很长一段时间里，人们发一封电报比打一个长途电话要便宜得多。

### 传真的优点

“teledeltos”翻译自古希腊语，基本意思是在远处书写平板电脑。西联公司在 20 世纪 30 年代开始开发 Teledeltos 纸，目的是通过传真发送电报，这种方法将大大减少将信息输入系统并从另一端发出的时间。只要发送者和接收者都有传真机，手写电报就可以传送，而不必由办事员打字或翻译成代码。Teledeltos 纸也用于各种图表记录器，如地震仪和地图绘图仪。将手写信息、照片或敌方领土地图输入一台传输精确副本的机器的能力是真正的游戏规则改变者。

因为它的成分，Teledeltos 纸可以在没有电解质的情况下容易地被标记。它标记得非常好，照片和其他图形信息可以传输，在接收端不需要任何处理。干燥的记录纸对光和极端温度也不太敏感。更重要的是，正确储存的干纸不会滋生真菌。Teledeltos 的纸张可以无限期闲置，而不会变得毫无用处。这种纸唯一真正的缺点是要达到预期的阻力需要一些费力的过程。传真机最终转向了数字传输和热敏打印技术。

![](img/277feb675b69c20cf6ad6b1bd4669612.png)

Image credit: [MIT](http://massis.lcs.mit.edu/archives/technical/western-union-tech-review/03-1/p008.htm)

### 引发一场革命

Teledeltos 纸的一面有浅灰色的电敏感涂层，另一面是炭黑。当用铁笔在纸的涂层面上通电时，涂层立即被烧掉，露出炭黑。Teledeltos 纸可以用 AC 或 DC 标记。极性也不重要，但是西联公司实验室里的男孩们在 DC 身上使用正极手写笔比负极手写笔时运气更好。

Teledeltos 纸有两种类型——“L”代表低电阻,“H”代表高电阻。一卷 Teledeltos 纸的电阻率取决于放入其中的导电纤维的质量。纸张的电气特性也受到纤维打浆过程和超级压光机导电纤维分布的影响，超级压光机是造纸和其他过程中使用的硬辊系统，用于压制和平整纸张和其他材料以增加密度。

### Teledeltos 前来救援

![The Western Union Telecar printed telegrams on the go and delivered them to homes and businesses.](img/a6b57996a2fd0afa270652df5ba1dd4d.png)

The Western Union Telecar printed telegrams on the go and delivered them to homes and businesses. Image credit: [Modern Mechanix](http://blog.modernmechanix.com/mags/MechanixIllustrated/1-1952/telecar.jpg)

西联汇款渴望将其触角延伸到私营企业和公共场所，这样那些不经常使用电报的顾客就不必为了分享一点好消息或表示哀悼而去电报局了。该公司的传真部门推出了几种类型的机器来满足不同的业务需求。

一些信息继续由专人递送，但不在总部打印。西部联合公司创造了一种远程汽车服务，打印由中央局传送到汽车上的电报，并把它们送到人们的家中。信息被印在记录空白上，这些空白由位于汽车乘客区的传真记录器自动切割。电视车的无线电和扩音设备在后备箱里。

办公室使用的标准传真机相当大，就像早期的微波炉。一种叫做 [DeskFax](http://www.cs.ubc.ca/~hilpert/e/deskfax/) 的较小版本只有面包盒大小，因为方便，这些设备占据了许多商人和秘书的办公桌。

![A Western Union DeskFax unit. Image from [B. Hilpert]http://www.cs.ubc.ca/~hilpert/e/deskfax/](img/4005ea8cf4ab17efae073939474f6485.png)

西联传真台。图片来自[ [B. Hilpert](http://www.cs.ubc.ca/~hilpert/e/deskfax/) ]

电传和传真都是使用转鼓机制扫描和记录电报。一条信息既可以打字也可以手写在空白电报上。然后，发送者将电报包在一个鼓上，并设置机器发送。这台机器会对信息进行光学扫描，然后传送到中央办公室。

在将信息发送给接收者之前，电报局的工作人员必须将收到的信息取出，包裹在发报机的滚筒上。一旦连接到接收方的线路上，远端单元就会发出蜂鸣声以引起注意。然后，接收顾客会将一张空白纸放在他们的传真滚筒上，并设置他们的机器接收。

### 黑客和教育 Teledeltos

![Measuring potential differences. Image from https://physics.ucsd.edu/students/courses/summer2010/physicslabs/SS2101BLLab03.pdf](img/cd62527552ee767c0fcdd62eff8396ad.png)

Measuring potential differences.
Image from [UCSD](https://physics.ucsd.edu/students/courses/summer2010/physicslabs/SS2101BLLab03.pdf)

除了传真机和测厚仪之外，像 Teledeltos 这样的导电纸还有许多用途。首先，它非常适合一次性制作标准和可变电阻。导电涂料可用作电线的连接点。该论文也非常适合使用生产中预期电流的一部分来模拟通过电路的电流。真空管设计师使用 Teledeltos 来模拟电势。Teledeltos 也可用于可视化电磁势和[执行场标绘](http://www-users.aston.ac.uk/~pearcecg/Teaching/PDF/TELDELT.PDF)。

我们确信至少有一些读者在学校或工作中使用 Teledeltos 或类似的东西。你知道你还能买到它吗？Teledeltos 纸张本身仍然可以从英国的两家公司获得，即装备更好的 T1 和 T2 的 Timstar T3。在美国，你可以从[帕斯科](http://www.pasco.com/prodGroups/conductive-paper-and-pen/index.cfm)买到 50 和 100 张一包的，有没有格子图案都可以。

[Teledeltos 纸质图片是来自[装备更好的](http://www.betterequipped.co.uk/teledeltos-conductive-paper-prd1516-pack-of-10-sheetsp-1262)的产品照片]