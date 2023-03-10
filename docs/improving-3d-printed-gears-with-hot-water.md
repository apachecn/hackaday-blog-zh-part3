# 用热水改善 3D 打印齿轮

> 原文：<https://hackaday.com/2016/07/03/improving-3d-printed-gears-with-hot-water/>

能够打印出定制齿轮是 3D 打印真正能够大放异彩的一个领域，而[Karl Lew]一直在忙着用 PLA 打印小齿轮并将其安装到步进电机轴上，但也有权衡。小齿轮需要紧紧地抓住电机轴，通常用一个螺钉穿过齿轮拧到电机轴上。但是，当做大量工作时，电机及其轴可能会变得相当热，热电机轴上的拧紧螺钉会将热量传递到 PLA，PLA 随后会变形。

[卡尔·卢]设法以一种不寻常的方式改进了事情:[当齿轮连接到步进轴上时，使用热水浴对齿轮进行退火](https://github.com/firepick/FireGear/wiki/Anneal-PLA)。退火 PLA 具有增加材料结晶度的效果，根据[一篇详细介绍 PLA 退火过程的文章](http://www.4spepro.org/view.php?article=005392-2014-03-28)，增加了硬度、强度和热变形。退火过程还会使零件略微收缩，如果在连接到电机的情况下对齿轮*进行退火，这会导致齿轮和开槽步进轴之间产生非常紧密的接合。*

 [https://www.youtube.com/embed/2JXesKiAqbs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2JXesKiAqbs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Karl Lew]关于 PLA 退火的维基页面总结了他的测试的重要部分:

> 用一个松动的定位螺钉将小齿轮连接到步进轴上，并使用双层真空塑料袋(如 Ziploc)在 160°F/71°C 水温下退火 50 分钟。在这种情况下，我们利用了与退火相关的收缩。零件收缩通常是一件坏事，但在这里，我们使用它来获得良好的效果，以获得一个坚实而紧密的连接开槽步进轴。确保退火小齿轮使用高填充(80%或更高)。轴退火小齿轮需要很少或没有固定螺钉张力，以保持在开槽传动轴上的位置。

如果使用热水来改善齿轮方面的东西太低技术含量，总有[将电机本身转换成闭环步进伺服](https://hackaday.com/2016/06/01/mechaduino-closed-loop-stepper-servos-for-everyone/)来完成升级循环。