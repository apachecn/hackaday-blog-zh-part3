# Hackaday 奖参赛作品:舌头视觉

> 原文：<https://hackaday.com/2016/10/03/hackaday-prize-entry-tongue-vision/>

视障人士知道一些我们其他人经常忽略的事情:我们实际上不是用眼睛看，而是用大脑看。为了他的 Hackaday 奖参赛作品，[Ray Lynch]正在建造一个舌头视觉系统，它将帮助盲人看穿人类大脑的一个辅助端口:味蕾。

[![tongue-vision-thumb](img/32487543769e2bd55915e5f8a6977fa8.png)](https://hackaday.com/wp-content/uploads/2016/10/tongue-vision-thumb1.jpg)

A display for the tongue (tongue image by [Mahdiabbasinv](https://en.wikipedia.org/wiki/Tongue#/media/File:%D8%B2%D8%A8%D8%A7%D9%86_tongue.jpg)).

舌头视觉的概念已经被证明了。Paul Bach-y-Rita 发明的舌视觉系统 Brainport 已经可以用于患者。然而，缺少的是一种低成本的开源硬件替代方案，使负担不起 10，000 美元产品的患者可以使用该技术。[雷]着手开始这个项目。他的第一个原型设计看起来已经很有希望，一旦他能够证明他的概念可行，所有的源代码都将作为开源发布。

基本上，该系统由一个数码相机组成，该相机将图像数据发送到一个棒棒糖状的电极矩阵，该电极矩阵刺激患者舌头上的一个区域。在训练阶段，患者学会将刺激模式解释为原始相机图像。对于电极矩阵，[Ray]设计了一个双面 PCB，上面有 16×16 个刺激味蕾的像素网格。每个像素都有一个暴露的通孔作为阳极，通孔周围有一个暴露的环形焊盘作为阴极。16 列阳极由两个 MC14555P 高端多路复用器驱动，而 16 行阴极环由 74LS156D 集电极开路多路复用器驱动。可以把它想象成一个没有 LED 的 LED 矩阵。图像可以通过一个带摄像头的树莓皮手机传送，也可以通过患者的智能手机传送。

[![tongue-vision-row-column-intersection](img/acd1ca93225f334a928932f37117644d.png)](https://hackaday.com/wp-content/uploads/2016/10/tongue-vision-row-column-intersection.jpg)

如果只有几个关于舌头实际电阻率和敏感度的假设被证明是正确的，一旦第一批原型 PCB 到达，该组件确实可以在舌头上产生预期的感觉。不管怎样，[雷的] PCB 布局——这也是他第一次接触 EAGLE——真的是赏心悦目。我们的舌头期待着看到原型的行动！

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)