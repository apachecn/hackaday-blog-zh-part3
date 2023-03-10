# 如何用 Delrin 和激光切割机制作任何东西——高级技巧

> 原文：<https://hackaday.com/2016/08/04/how-to-build-anything-with-delrin-and-a-laser-cutter-part-iii/>

每个人都希望他们的原型看起来很精致，而不是事后看起来像 3D 版的。Delrin 和激光切割机的结合使这变得容易，特别是如果你学会一些诀窍，将使你的组件在功能和美学上流行。

上次，我们深入探讨了用 Delrin 和典型的 40 瓦激光切割机制造零件的[，并且我们讨论了材料](http://hackaday.com/2015/09/03/how-to-build-anything-using-delrin-and-a-laser-cutter/)的一些[限制。最近，【Gerrit】让我们](http://hackaday.com/2015/09/22/drawbacks-of-lased-delrin-and-how-to-slip-around-them/)[近距离观察了材料本身](http://hackaday.com/2016/03/03/materials-to-know-acetal-and-delrin/)。距离我们的第一篇文章已经过去一年了，但是技巧列表还远未完成。

如果你在这个领域刚刚起步，让我给你介绍两种激光切割原型的经典技术:[拼图](http://store.curiousinventor.com/medimg/tips/custom_laser_cut_boxes/checker_assembling_big.jpg)和 [T 形螺母开槽](http://blog.ponoko.com/wp-content/uploads/2010/06/t-slot.jpg)。虽然这些技术是可靠的，但我希望，无畏的读者，它们会让你渴望更干净、更精致的东西。如果是这样，请继续阅读！

## 铆接

![rivet_lamp](img/06a140d32333581428b2d2a65e7cc659.png)

the [Delrin Rivet Lamp](http://www.doublejumpelectric.com/projects/collapsing_delrin_desklamp/2015-08-15-collapsing_delrin_desklamp/)

铆钉为我们提供了一个与螺钉相似的特征:它们非常适合将两块板固定在一起。铆钉的另一个好处是，它们的轴为需要相对旋转的零件提供了更光滑的表面。在数量上，铆钉在价格上与螺钉相当，并且它们提供了不同的美学吸引力，可能是因为我们在业余爱好者项目中不常看到它们。铆钉有各种各样的形状和尺寸，但我更喜欢标准的半管状，因为它们的顶部和底部只从安装的材料中稍微伸出来。使用半管状铆钉，暴露的底部呈蘑菇状形成一个独特的按钮功能，我们在服装和消费品中见过这种功能。作为一个提醒，指定铆钉长度需要对零件的尺寸有一点先见之明。对于信封背面的计算，铆钉在被压碎前应伸出零件约 55%的铆钉直径[[PDF](http://www.rivet.com/stats/tubular/semitub-design.pdf)]。

智者的一句话:铆钉是永久的！与螺钉不同，铆钉(不包括花哨的拆卸设备)是一次性操作。使用铆钉时，我们必须清楚地记住组装零件时的操作顺序。真人真事:在将两个零件以错误的顺序拼在一起后，我已经报废了许多零件。

## 埋头孔

[![](img/f86093aaebb569a28e26899554d4b5a7.png)](https://hackaday.com/wp-content/uploads/2016/07/28400380580_56518a3613_m.jpg)[![](img/d61d2605eeca9f2fcaaef3e8fae45c43.png)](https://hackaday.com/wp-content/uploads/2016/07/28606449781_58c43de473_m.jpg)

埋头钻给我们带来了两个直接的好处。首先，它使我们能够将螺钉放入与板齐平的设计中。其次，它极大地改善了零件的外观和感觉。我们的螺丝钉再也不会从我们的身体里伸出来，这是一种务实的需要。

从实用的角度来看，平头螺钉让我们将零件之间的间隙挤压在一起，为我们节省了空间，而那些突出的螺钉头却急切地想从我们身上拿走这些空间。在右边的例子中，这个机器人车轮与车身的紧密间隙要求使用[平头螺钉](http://www.mcmaster.com/#socket-cap-screws/=13j345j)解决方案。在美学方面，埋头孔在激光切割原型中并不常见。他们让我们的观众更努力地思考《他们是如何做到的》中的*如何*而不是操之过急，大喊“激光切割机！”在我们的项目上。

那么如何创造这样一个空洞呢？幸运的是，Delrin 喜欢黄油之类的标准金属工具。对于上面显示的触须机构椎骨，我创建了一个微型[埋头孔笼](http://www.panamericantool.com/micro-stop-countersinks-cage.html)的特征。这些工具是专门为航空业设计的，用于在工厂车间高效地将飞机铆接在一起。提示:通过适当设置钻床的急停螺母，你可以用传统的[锪孔刀具](http://www.mcmaster.com/#countersinks/=13j3jt3)达到同样的效果。

## 热定型嵌件

![heat_staking_delrin](img/ba598606be87a33a188fef8513b469ef.png)

applying heat-set inserts in Delrin at 4x speed

你需要一个既能承受重载又能反复拧紧和拧松的螺纹特征吗？那么[热定形插片](http://www.mcmaster.com/#heat-inserts/=13j22l0)可能适合你！像许多其他自重的热塑性塑料一样，Delrin 是这些黄铜块的主要候选材料。

热定形镶件确实如其名:取任何一种热塑性塑料，按预定尺寸切一个孔，然后将一个热金属镶件插入孔中。让结果冷却——噗——一个有弹性的螺纹特征现在永久地嵌入到你的零件中！供应商出售特定的插入工具，但我们发现我们的烙铁(温度高达 250°C)和一双稳定的手也能很好地工作。

## 用 3 项新技术武装自己

有时候，发现新的技巧是打开我们对周围世界的视野。随便看看。几乎我们周围的每一种消费品都是大量制造的，这要求大规模生产的技术。为了制造这些产品，设计师需要可重复、可靠、结果可预测的技术。铆钉、埋头钻和加热嵌件并不是什么新东西。他们是从这个世界借来的。通过对细节的仔细关注，也许你会发现更多适用于激光切割 Delrin 的技术。请在评论中告诉我们！在那之前，继续推出那些原型！