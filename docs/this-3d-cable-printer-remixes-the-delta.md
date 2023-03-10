# 这台 3D 电缆打印机重新混合了三角洲

> 原文：<https://hackaday.com/2017/10/12/this-3d-cable-printer-remixes-the-delta/>

上次我们遇到[Daren Schwenke]时，他正在展示他的 6 色 delta 打印机，这种打印机可以在打印过程中无缝变色。现在，他正在研究一种打印机，这种打印机使用张紧的电缆来精确地移动工具头，同时保持足够的稳固性，使[达人]可以轻敲工具头而丝毫不动。

这比龙门式 3D 打印机简单得多，底盘形状像测地线多面体，由玻璃纤维桁架(那些车道标志)组成，由 3D 打印的凸耳固定，所有这些都由一个 Beaglebone Green 和四个步进器控制。建造的一个关键元素是中心钢杆，一个 4 英尺的重新利用的花园桩，用于稳定整个工具架。就建造直径而言，它可以从大约 200 毫米扩展到 600 毫米。[达人]的目标是使用 Machinekit 的[三脚架运动学](https://github.com/machinekit/machinekit/blob/master/src/emc/kinematics/tripodkins.c)进行控制，他也从 [RepRap 的飞行 SkyDelta](http://reprap.org/wiki/TriDPrinting.com_Flying_SkyDelta) 项目中学到了很多。

要获得更多 3D 打印的好处，一定要看看[达人]前面提到的 [6 色 delta](https://hackaday.com/2017/03/26/mrrf-17-true-color-3d-printing/) 。

 [https://www.youtube.com/embed/KQ19fT4BQQU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KQ19fT4BQQU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

