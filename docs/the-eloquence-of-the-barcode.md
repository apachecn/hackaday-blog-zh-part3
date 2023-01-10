# 条形码的魅力

> 原文：<https://hackaday.com/2015/11/02/the-eloquence-of-the-barcode/>

哔。每当你在零售店购买产品时，你都会听到这句话。收银员把你买的东西放在嵌入他们收银台的扫描仪上滑动，或者用手持扫描仪拍摄。标签上熟悉的一系列条和空格被数字化，解码成数字，然后用作对特定商店出售的每种产品的数据库的查询。这种事情经常发生，以至于我们认为这是理所当然的。现代条形码已经存在 41 年了。1974 年 6 月 26 日，在俄亥俄州特洛伊市的 Marsh 超市，第一个用条形码购买的产品是 10 包果汁口香糖。那天扫描的代码是 UPC-A，和今天你能买到的几乎所有零售产品上使用的条形码一样。

条形码的历史并不像人们想象的那样简单。不止一个小组被认为发明了这项技术。如何在机器上对数据进行编码，存储在物理介质上，然后在以后的某个时间读取它？穿孔卡片和纸带已经这样做了几个世纪了。问题是存储这些数据时不能在载体上打孔。总的来说，这个问题非常普遍，几个不同的行业都在努力解决这个问题。

在 20 世纪 30 年代，约翰·克莫德、道格拉斯·杨和哈里·斯帕克创造了一种四条码。他们是西屋电气公司的工程师，毫不奇怪，他们的应用是自动处理电力账单。[然而，这些专利被概括为“卡片分类机”](http://www.google.com/patents/US1985035)。

1948 年，伯纳德·西尔弗和约瑟夫·伍德兰开始研究一种用于超市读取线性和圆形印刷代码的系统。他们从 16 毫米和 35 毫米电影中使用的光学音轨中获得灵感。事实上，他们的阅读器采用了通常用于电影放映机的 RC935 光电倍增管。Silver 和 Woodland 通常被认为是条形码的发明者，但他们在自己的工作中参考了西屋公司的专利。包括 IBM 在内的几家公司对这项专利感兴趣，但认为在它成为实用系统之前，关键技术仍需开发。Philco 购买了专利，最终卖给了 RCA。

或许最臭名昭著的条形码宝座来自杰罗姆·h·勒梅尔森。莱梅尔森一生中获得了 600 多项专利，其中包括一些机器视觉专利。其中许多被认为是[号潜艇专利](https://en.wikipedia.org/wiki/Submarine_patent)。他的大部分财富都是通过实施和许可这些专利获得的，价值高达 13 亿美元。这给他打上了早期专利流氓的烙印。在具有里程碑意义的 2004 年针对康耐视公司和 Symbol Technologies 的诉讼中，Lemelson 的条形码专利被宣布为不可执行。这个案例在今天的专利欺诈诉讼中经常被引用。

我们所知的现代条形码始于 20 世纪 60 年代末。当地市场演变成了超市。带有机械收银机的结账系统是明显的瓶颈。但是如何加快速度呢？杂货贸易协会创建了统一杂货产品代码委员会(现在的 GS1)来解决这个问题。GS1 向 RCA、IBM、Singer、梁永能、Litton 和 Pitney Bowes 等公司寻求解决方案并收到提案。RCA 利用 Silver 和 Woodland 的专利创建了靶心代码。IBM 可能没有专利，但他们有更好的东西。当时，约瑟夫·伍德兰已经在 IBM 工作了几年。他被招募到一个包括乔治·劳雷尔在内的团队。Laurer 仍然活跃在这个行业，[维护着一个关于条形码信息的网页](http://www.laurerupc.com/)。这个团队努力设计一个健壮的代码。最终，IBM 代码变成了我们都知道的通用产品代码(UPC)。

自 1974 年以来，刚果爱国者联盟的符号相对保持不变。已经有一些扩展来编码额外的数据，但是核心作为一个持久的标准存在了下来。一旦代码投入使用，修订将需要从印刷业到销售点行业的大规模改变。

### 构建条形码

UPC-A 是一种纯数字符号系统。也是固定宽度。每个 UPC-A 符号编码 12 个数字，然而一个数字被用作校验字符，只剩下 11 个可用的数字。代码的框架从一个安静区开始，这个安静区实际上是一个安静的区域，与空间的颜色相同。在安静区内有一个保护栏，这是一个定义代码开始(或结束)的独特模式。UPC-A 在代码的开头和结尾有静区和防护栏。一个独特的中心防护栏定义了符号的中间。代码的其余部分由 12 个字符组成。

![upc-expand](img/f0a539d75ef6db4fb8a2dd50c2a8bbd0.png)

想象一下 UPC-A 是如何编码数据的，想想莫尔斯电码。如果一个人画出摩尔斯电码讯息的所有点和破折号，他们就会有一个基本的条码。实际上，莫尔斯字符集工作得不是很好，因为它使用可变长度的字符。T 是一个破折号，而 Y 是三个破折号和一个点。确定一个字符的结束位置和另一个字符的开始位置需要在每个字符之间添加空格。这在无线电通信中是可行的，但在印刷页面上就变得低效了。

### 字符–全在宽度上

单个 UPC 字符也是固定宽度的。长度的基本单位称为模块，表示符号系统中使用的最小条或空间。UPC-A 使用的标称模块尺寸为 0.33 mm。每个 UPC 字符由两个竖线和两个空格组成，总长度为 7 个模块。对于 UPC-A 左侧的数字 0，字符是 3，2，1，1——表示一个 3 个模块宽的空格，后跟一个 2 个模块宽的横条，然后是另一个两个模块宽的空格和横条。

中间防护栏右侧的字符与左侧的字符颜色相反。这意味着左侧的每个字符都以空格开头，而右侧的每个字符都以竖线开头。为什么两个颠倒的字符集如此复杂？方向！这些年来，杂货店收银台的条形码扫描仪没有什么变化。它安装在一个槽里，物品从上面通过。条形码可以在任何方向，所以扫描仪必须能够解码符号从左到右，从右到左，或几乎任何角度。

需要记住的重要一点是，读取条形码是关于相对宽度的。使用手持式扫描仪，条形码可以位于扫描仪的任何合理距离。较远的条形码看起来会比较近的条形码小。读者只需将看到的最小元素(模块)与其他元素的宽度进行比较。一旦这些相对宽度符合静区和防护栏的规则，阅读器就决定它已经找到了一个可能的代码，并开始寻找字符。

UPC-A 可能是第一个常用的条形码，但它并没有独立存在很长时间。欧洲修改了规范，增加了一个数字。由此产生的代码被称为 EAN-13。EAN 代码都包括一个三位数的国家代码。一个奇怪的副作用是创造了一个虚构的国家[“图书王国”](https://en.wikipedia.org/wiki/Bookland)，它被用于书籍和其他出版物。

今天，有几十种不同的条形码符号。常用的线性符号体系包括 Code 39、Code 128、GS1 DataBar、Interleaved 2 OF 5、MSI Plessy。当一行代码不够用时，可以使用 2D 符号，包括 PDF-417、Aztec 代码、Maxicode、Datamatrix 和 QR 代码。我们理所当然地认为扫描代码并跳转到网页是多么容易——但这一切都是从简单的 UPC 开始的。

来自[维基百科](https://en.wikipedia.org/wiki/Universal_Product_Code)的条形码图像。