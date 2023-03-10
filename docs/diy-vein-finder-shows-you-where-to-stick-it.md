# DIY 静脉探测器告诉你在哪里贴它

> 原文：<https://hackaday.com/2016/05/19/diy-vein-finder-shows-you-where-to-stick-it/>

每个献血、接受静脉注射或验血的人都知道在针头扎进去之前的那一点点焦虑。这将是一个单一的操作，还是抽血医生会在试图找到静脉的同时进行石油钻探？我们中的一些人很容易找到血管。其他人最终走出去，看起来像是在和一根针搏斗。

亚历克斯的妻子的女朋友是一名护士，她过去一直找不到静脉。[Alex]是一名汽车工程师，他更熟悉油管而不是静脉和动脉。虽然他自己不能帮助她，【亚历克斯】[设计了这个 3D 打印的静脉探测器](http://www.instructables.com/id/3d-Printed-Medical-Vein-Finder/)来帮助他~~的妻子~~的女朋友外出工作。他开始研究市场上的设备。像 [Veinlite](https://www.veinlite.com/) 这样的产品使用发光二极管照亮皮肤。本质上，这些产品是一串发光二极管和一个电池。它们获得了专利，通过了 FDA 认证，价格在 188 到 549 美元之间。[亚历克斯]和他的 T10 妻子 T11 女朋友付不起那种费用，所以他自己造了。

发光二极管是这个设备的关键。静脉中缺氧的血液吸收光线，使静脉在皮肤上呈现为暗纹。[Alex]发现在 620 纳米和 680 纳米之间需要 ~~15~~ 11 个 led。发光二极管也需要有适当的亮度。低于 4000 mcd 就不够亮了。超过 6000 的 mcd 会让用户眼花缭乱。几个限流电阻，一个开关，电子设计就完成了。

这个案子经过了几次修改才弄清楚。Veinlite 使用 C 形，允许静脉注射针头穿过插槽并插入 lite 字段。[Alex]能够在他自己的静脉探测器中克隆这个设计。

如果 led 对你来说还不够高科技，[还有其他设备](https://www.youtube.com/watch?v=no_kjDorJeo)使用相机和投影仪在病人皮肤上创建血管的增强图像。如果你想深入浅出，看看 2015 年 Hackaday 奖的[这款 DIY CT 扫描仪](http://hackaday.com/2015/05/29/hackaday-prize-entry-a-better-diy-ct-scanner/)。

 [https://www.youtube.com/embed/QaK9M3PqqzY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QaK9M3PqqzY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

