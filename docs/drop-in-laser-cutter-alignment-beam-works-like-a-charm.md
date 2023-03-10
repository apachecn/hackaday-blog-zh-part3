# 嵌入式激光切割机对准光束的效果非常好

> 原文：<https://hackaday.com/2016/11/29/drop-in-laser-cutter-alignment-beam-works-like-a-charm/>

每个激光切割机爱好者最终都会提出这样一个问题:我究竟如何对准一束不可见的光束，它非常乐意击中我的眼球，更不用说烧掉它路径上的所有东西了？我们讨厌承认这一点，但激光切割机光束对准不是一件容易的事情。然而，为了更好地帮助这项工作，一些人倾向于将红色二极管激光器混合到光束路径中。另一些则是将二极管激光器直接临时固定在光路中，一旦对准就将其移除。

一个离经叛道的人把二极管激光混合带到了一个新的高度！[Travis Reese]增加了一个伺服驱动的二极管激光器，当盖子弹出时，它会动态地落入激光管的路径中，然后当盖子再次关闭时，它会舒适地倾斜出激光路径。
 【特拉维斯】的光束对准装置由 Arduino 提供动力，并由经典的业余爱好伺服系统驱动。固件更新会稍微上下移动激光器的设定点进行调整，每步大约移动十分之一度。虽然[Travis]没有为对准暴露所有的自由度，但这个夹具对于获得与光束的真实路径精确匹配的路径来说绰绰有余。

好奇？[Travis'] [如果你想开发自己的变体，CAD 模型是可以随意购买的](https://myhub.autodesk360.com/ue2968626/g/shares/SHabee1QT1a327cf2b7a9e4a271fe94cc735)。

激光校准是棘手的，但我们已经看到了一些其他的解决方案。对于一个更经典的跟踪实际光束路径的机制，看看[【斯蒂芬的】方法](http://hackaday.com/2016/03/10/aligning-invisible-lasers-on-the-cheap/)。

 [https://www.youtube.com/embed/pDiI9qctFAo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pDiI9qctFAo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

