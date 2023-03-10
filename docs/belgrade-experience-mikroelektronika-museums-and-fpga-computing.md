# 贝尔格莱德体验:MikroElektronika、博物馆和 FPGA 计算

> 原文：<https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/>

我最近有机会访问贝尔格莱德，并参加了 Hackaday |贝尔格莱德会议。每当我旅行时，我喜欢做一些额外的实地考察来探索这个地区。这次塞尔维亚之行包括参观电子制造业、一些优秀的博物馆和一家将 FPGAs 嵌入服务器和 PCIe 卡的初创公司。

### MikroElektronika

二战后，塞尔维亚是南斯拉夫的一部分，该地区是整个苏联集团的制造业中心。特别是大量的电子元件(电阻、电容等。)是在这里制造的。这些类型的组件可能不再在这里生产，但仍然有一个强大的电子制造中心，一个很好的例子是 MikroElektronika，一家在一些旧工厂的基础上建立的公司。这座建筑和这家企业一点也不古老，而且他们非常成功，他们正在计划建造第二座大型建筑，以提高他们的生产能力。Sophi Kravitz 和我受到了首席执行官 Nebojsa Mati 的问候，见本文顶部图片。

 [![So many mikroBUS click boards!](img/bc88a82d1c03ee4e7ebde67e52afa5ac.png "lots-of-mikroBUS-boards")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/lots-of-click-boards/) So many mikroBUS click boards! [![STM32 Development Board](img/d8fd76e981889bdd450395f3f7b358ad.png "stm32-development-board")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/stm32-development-board/) STM32 Development Board

MikroElektronika 因其 mikroBUS 点击板而闻名。这些是标准化的模块，承载着世界上所有的传感器、显示器、输入法和通信方案。想要操纵杆吗？是的。蓝牙 LE，ZigBee，WiFi，LoRa RF？所有大是。上面的图像显示了客户支持部门为最近的测试而布置的点击板，这远远不是所有可用的。

MikroBUS 是连接外设的标准，我们已经在许多主板上看到过，如 [Microchip Curiosity](http://hackaday.com/2015/07/22/review-microchip-curiosity-is-a-gorgeous-new-8-bit-dev-board/) 。当然，MikroElektronika 也制作自己的开发板，采用这种外形。上面是许多开发板中的一个——这是用于 STM32 开发的，但你可以说出它的名字，他们可能有——它在右上角包括一对 mikroBUS 插槽。这些主板让我想起了我小时候做的 300 合 1 电子项目。只要在标题上加上“嵌入式”，我们就生活在一个全新的时代。

 [![Getting solder paste machine ready](img/a790235d28064ed5156deffe8b905c32.png "working-paste-machine")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/working-paste-machine/) Getting solder paste machine ready [![Solder paste stencil](img/cc4d9fb57acb22af48a2dd544a82ec47.png "solder-squeegee-machine")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/solder-squeegee-machine/) Solder paste stencil [![Aleksandar Nikolić explains equipment to Sophi Kravitz and me](img/a9ca431177569e51e44c3d0b3ea61eae.png "aleksandar-explaining-assembly-lines")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/aleksandar-explaining-assembly-lines/) Aleksandar Nikolić explains equipment to Sophi Kravitz and me [![Selective soldering machine](img/b7ab9b11a61e2a50cce4b28392b86ed4.png "selective-soldering-machine")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/selective-soldering-machine/) Selective soldering machine [![Huge pick-and-place machine](img/99ff837fb6d9388543782b46cf4a4411.png "gnarly-pick-and-place")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/gnarly-pick-and-place/) Huge pick-and-place machine [![Reels!](img/7c31147f579fafc334d421e137fc4f62.png "reels-of-fun")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/reels-of-fun/) Reels!

一旦我们看了成品，就可以了解一切是如何制作的。他们有两组线来填充所有的电路板。目前，他们不生产自己的印刷电路板，但希望通过新建筑来改变这种状况。一旦他们从制造商那里拿到 PCB，其他的一切都在现场完成。

上图中，你可以看到一名技术人员正在准备锡膏机，将锡膏涂在电路板上。从那里进入一个巨大的令人印象深刻的取放机器。光是看到机器上的卷轴就很美了。他们有用于表面贴装元件的回流焊炉，在另一个房间(未画出)有波峰焊。对我来说，这里最酷的机器是选择性焊接机。它在电路板下面有一个向上翻转的管道，有溢出的熔化焊料从中流出。电路板在这根棒上移动，焊接通孔元件。这里有一个选择性焊接机的随机视频，让你对这里发生的事情有个概念。

### 博物馆

我很兴奋能和迈克·哈里森和克里斯·甘梅尔一起去科技博物馆。他们有一个巨大的计算机技术展览，我们直接进入模拟计算机。

 [![Pace patch board for programming](img/463b17683087af52b907c0b643d3067a.png "IMG_20160410_185555")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/img_20160410_185555/) Pace patch board for programming [![Pace analog computer](img/dfeddfeaee176383439ab32226e31853.png "IMG_20160410_185624")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/img_20160410_185624/) Pace analog computer [![Analog calculator uses stylus for set up](img/86f28a8f99d1fb46be4067739c2b079d.png "IMG_20160410_185922")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/img_20160410_185922/) Analog calculator uses stylus for set up

这台巨大的电脑令人印象深刻。当你用随身携带的价值 200 美元的智能手机给它拍照时，你会真正感受到我们来自哪里。编程的很大一部分是接线板，它可以追溯到电话接线员在线路之间打电话。也有一些其他模拟计算设备展出，我喜欢这个手持模拟计算器，它使用手写笔来设置计算。

 [![Galaksija computer designed by Voja Antonic](img/be617e88e5a1e1b9e99c046f9a844acd.png "IMG_20160410_190035")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/img_20160410_190035/) Galaksija computer designed by Voja Antonic [![IMG_20160410_190046](img/62c3595d8bb6ce8da4e302b5befd74b2.png "IMG_20160410_190046")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/img_20160410_190046/) 

我应该意识到这台电脑会展出，但看到 Galaksija 电脑是一种快乐的冲击。这是一台由 Voja Antoni 开发的自己组装的个人电脑。1983 年，当个人电脑在硅谷上市时，由于禁运，所用的芯片在南斯拉夫无法买到。Voja 找到了解决所有这些问题的方法，购买了大约 8000 个套件，这样人们第一次可以拥有自己的电脑。我们当然很了解 Voja Antoni，他一直在为 Hackaday 撰写[的精彩文章](https://hackaday.com/2015/08/03/hacking-the-digital-and-social-system/)，并设计了 [Hackaday | Belgrade 徽章](https://hackaday.io/project/9509-badge-for-hackaday-belgrade-conference)。他关于硬件的会议报告将很快发表。

### 马克斯勒

最后我们参观了 Maxeler 公司在贝尔格莱德的办事处。他们是一家高速计算公司，创建了一个基于 FPGA 的平台，可以用作某些类型算法的动力室。将软件循环卸载到高度并行的硬件上可以带来巨大的速度提升。

 [![PCIE fpga module](img/35b7adf1eba879f30c27ff6fe2d73823.png "pcie-fpga-card-back")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/pcie-fpga-card-back/) PCIE fpga module [![1U server contians up to 8 FPGA computing modules](img/64f179b2b225c4ba16341ddc72b4c0b5.png "server-blade-fpga")](https://hackaday.com/2016/04/26/belgrade-experience-mikroelektronika-museums-and-fpga-computing/server-blade-fpga/) 1U server contians up to 8 FPGA computing modules

硬件有两种形式。左边显示的是一张价值 5000 美元的 PCIe 卡，你可以把它装入台式电脑。该公司一直在向大学项目提供这些工具，以帮助研究，并在程序员学习技术时向他们提供平台。右边是一个 1U 刀片服务器，可以装载多达八个 FPGA 模块。

硬件本身只是难题的一小部分。剩下的就靠定制软件了，这样它就知道什么时候打电话给大铁。Maxeler 有一个类似 Java 的编程环境来帮助解决这个问题，他们的大部分业务是定制客户端代码来配合硬件。Maxeler 的一个主要用例是财务分析。

![serbian-dinar-tesla](img/c4ab409b80e8ba2438d0c31d35266ca4.png)

这远远不是我们在贝尔格莱德所做的一切，还有许多事情我们没有做到。这座城市、这里的人们和这里的历史令人惊叹。你会感到受欢迎，想要回来。

这次我没能去特斯拉博物馆，但希望能再有一次机会。著名的发明家和思想家尼古拉·特斯拉来自塞尔维亚。我给你们留下这张 100 塞尔维亚第纳尔钞票的图片，上面有他的头像(现在装饰在我办公室的公告栏上)。但是那个等式呢？