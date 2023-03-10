# 获奖后:SatNOGS 制造卫星

> 原文：<https://hackaday.com/2016/05/19/after-the-prize-satnogs-and-building-satellites/>

当 Hackaday 宣布 2014 年 Hackaday 奖的获奖者时，一群来自希腊的黑客因他们的 [SatNOGS 项目](https://hackaday.io/project/1340-satnogs-global-network-of-ground-stations)获得了 196，418 美元的大奖，该项目是一个面向业余 Cubesats 的全球卫星地面站网络。

该设计展示了一个可负担得起的地面站，它可以低成本建造，并连接到公共网络，以利用卫星的好处，即使是业余卫星。这个项目的社会影响是深远的。除了 SatNOGS 网络本身，这一倡议还是构建其他互联设备网络的模板，使共享(和开放)数据惠及所有人。为了推进这项事业，SatNOGS 团队成立了 [Libre 太空基金会](https://librespacefoundation.org/)，这是一个非营利性基金会，其使命是促进、推进和发展自由和开放源代码的太空技术和知识。

现在，该基金会与帕特雷大学合作，准备发射[UPSat——一颗 2U 开源希腊立方体卫星格式卫星](https://upsat.gr/),作为 [QB50 国际热层研究任务](https://www.qb50.eu/index.php/project-description-obj)的一部分。该设计旨在最大限度地 DIY，从头开始设计大多数子系统。虽然第一个原型很昂贵，但他们希望记录开源硬件和软件将有助于启动空间工程和技术的生态系统。截至目前，卫星已经完全建成，正在进行测试和集成。在 7 月中旬，它将被运送到[纳米轨道](http://nanoracks.com/)由 SpaceX 龙太空舱运载，然后从国际空间站发射。

像这样一个典型的立方体卫星由几个子系统组成。其中最主要的是将所有部件固定在一起的[结构](https://upsat.gr/?page_id=34)单元。电力子系统(EPS)模块生产、储存、分配和控制 Cubesat 的电力。科学单元(SU)是主要的有效载荷，由一个多针 Langmuir 探针仪器组成，该仪器通过测量放置在卫星前面的四个针探针分别收集的电流来工作。

第二个有效载荷是图像采集组件(IAC ),它使用运行 OpenWRT 定制版本的 DART4460 Linux 嵌入式板、Ximea MU9PM-MH USB 相机和连接到相机的 50 毫米镜头来制作地面图像，根据卫星的高度提供每像素 11 米至 18 米的分辨率。姿态确定和控制子系统(ADCS)在任务期间稳定卫星并将其定向在期望的方向。

星载计算机子系统(OBC)是卫星的大脑。它促进所有核心飞行功能，并执行所有主要决策和所有子系统的监控。它的核心是一个 STM32F4 微控制器，运行定制版本的 FreeRTOS。使用 ECSS-E-70 定义的 ECSS-CCSDS 遥测和遥控包标准实现地面通信。星载通信子系统(COMM)基于 CC1120 射频收发器芯片，该器件已在以前的任务中成功使用。

所有广泛的项目文档都可以在他们的 [GitHub 库](https://github.com/librespacefoundation?query=upsat)上获得，他们网站上的博客帖子记录了他们旅程中的主要里程碑，所以一定要全部查看。然后继续关注 7 月某个时候 UPsat 的发布和部署。与此同时，看看这篇宣布 2014 年[黑客日奖](http://hackaday.com/2014/11/13/satnogs-wins-the-2014-hackaday-prize/)获奖者的帖子。愿原力与你同在，厄普萨特。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)