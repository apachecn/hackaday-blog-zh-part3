# 回流设备使 SMD 焊接成为公园里的铁锅

> 原文：<https://hackaday.com/2018/04/25/reflow-rig-makes-smd-soldering-a-wok-in-the-park/>

对于 DIY 回流设置，大多数人似乎依赖可靠的旧货店烤面包机作为平台来破解。但有一点要说的是，直接加热 PCB 而不是加热周围的空气，为此，人们可以在庭院销售中寻找热板进行转换。但是[电炒锅作为回流焊热板？](https://www.instructables.com/id/Reflow-Soldering-Hotplate/)当然，为什么不呢？

最终，[ThomasVDD]的回流工作与任何其他回流构建是一样的。它有一个易于控制的热源、温度传感器和一个微控制器，可以运行精确温度控制所需的[比例-积分-微分(PID)](https://hackaday.com/2016/05/18/flying-with-proportional-integral-derivative-control/) 控制算法。他使用的加热元件来自电炒锅，这只是一个幸运的意外。一个配有[切缝弯曲接头](https://hackaday.com/2012/09/04/playing-around-with-kerf-bending/)的激光切割 MDF 外壳容纳着加热元件、固态继电器和运行该节目的 Arduino Nano。MAX6675 热电偶放大器检测温度，并允许 Nano 通过不同焊料的不同曲线来循环温度。它很紧凑，简单，而且[ThomasVDD]现在有一个备用的炒锅可以放在灶台上使用。不喜欢什么？

当然，回流不仅仅意味着烤箱或电炉。为什么不给[回流焊大灯](https://hackaday.com/2017/12/12/car-lights-for-reflow-heat-source/)、[回流焊喷灯](https://hackaday.com/2016/09/01/blowtorch-smd-reflow/)，甚至[回流焊工作灯](https://hackaday.com/2017/07/13/a-bright-idea-for-reflow-soldering/)试一试？