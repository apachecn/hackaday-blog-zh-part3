# 问 Hackaday:磁齿轮有什么用？

> 原文：<https://hackaday.com/2016/08/15/ask-hackaday-what-are-magnetic-gears-good-for/>

令人惊讶的是，磁性齿轮并不为人所知，只在少数特殊应用中使用。然而，它们的受欢迎程度正在上升，它们是传递机械能、转换旋转扭矩和转速的最巧妙的解决方案之一。迟早，你会在某个地方偶然发现它们，所以让我们来看看它们是什么，它们有什么用处。

## 什么是磁力齿轮？

[![](img/779ecaa1fc39d7e1a77f4609ef7032db.png)](https://hackaday.com/wp-content/uploads/2016/08/gears_animation1.gif)

Conventional gears ([image source](https://en.wikipedia.org/wiki/Gear#/media/File:Gears_animation.gif))

传统齿轮使用机械互锁齿的配合面，而磁性齿轮使用交变磁场来传递扭矩。长期以来，磁力齿轮在工程中只起次要作用。它们相对较高的价格，直接反映了它们对钕等稀土的依赖，复杂的组件，以及它们在高扭矩下打滑的趋势，并没有将它们推到聚光灯下。磁性齿轮可实现的扭矩密度确实比它们的机械对应物低得多，尽管从好的方面来看，如果超过它们的指定扭矩，它们也不会遭受不可修复的损坏。目前，增加磁性齿轮中的扭矩是许多研究项目的主题，并且磁性齿轮正在找到进入更多应用的方法。

[![3D printed, magnetic cogwheels by GM Ferrari CC-BY](img/c933e01011b588249ed571ef5d398bb5.png)](https://hackaday.com/wp-content/uploads/2016/08/magnetic_cogwheel1.gif)

3D printed, magnetic cogwheels [by GM Ferrari](http://www.thingiverse.com/thing:1169108) CC-BY

因为磁性齿轮不是机械互锁的，任何转子之间都没有物理接触，所以它们不会受到机械磨损。大多数常规齿轮类型，如嵌齿轮甚至蜗轮，都可以复制为磁性齿轮，只需用永磁体的交替磁极替换切割齿即可。右侧的 3D 打印磁性“齿轮”组件就是一个很好的例子。

然而，在工业应用中，磁性齿轮一词通常意味着性能更好的同轴类型，您可以在下面的动画中看到。它在结构上非常类似于一个应变波齿轮(即[谐波传动齿轮](https://en.wikipedia.org/wiki/Harmonic_drive)，也如下所示),并允许高传动比以及相对较高的扭矩。这种类型的齿轮依赖于磁场的灵活性，而不是一个灵活的花键。点击下面不同齿轮的动画，查看它们如何工作的细节:

 [![Harmonic Drive gear with outer circular spline (blue), flex spline (red) and wave generator (yellow) by LaurensvanLieshout CC-BY-SA 3.0](img/d133d1a582eb7165de1ac2dd564965ee.png "harmonic-drive")](https://hackaday.com/2016/08/15/ask-hackaday-what-are-magnetic-gears-good-for/harmonic-drive/) Harmonic Drive gear with outer circular spline (blue), flex spline (red) and wave generator (yellow) by [LaurensvanLieshout](https://en.wikipedia.org/wiki/Harmonic_drive#/media/File:Harmonic_drive_animation.gif) CC-BY-SA 3.0 [![Concentric, magnetic gear with magnetic rings (north: red / blue: south) and steel pieces in the modulator ring tray (green)](img/fae7a311c9322abe32075bd739aa4a9a.png "magnetic_gear_26_o")](https://hackaday.com/2016/08/15/ask-hackaday-what-are-magnetic-gears-good-for/magnetic_gear_26_o/) Concentric, magnetic gear with magnetic rings (north: red / blue: south) and steel pieces in the modulator ring tray (green) [![Magnetic field simulation of a magnetic gear, based on this video by hoangcokhi123](img/712a96955edc976244cc42acdbc7fec5.png "magnetic_gear_field_o")](https://hackaday.com/2016/08/15/ask-hackaday-what-are-magnetic-gears-good-for/magnetic_gear_field_o/) Magnetic field simulation of a magnetic gear, based on [this video by hoangcokhi123](https://www.youtube.com/watch?v=aUjr_uD-fLA)

当同心磁性齿轮的内部快速旋转磁环旋转时，它迫使由嵌入非磁性托盘中的铁磁钢片组成的调制器环与外环的交变磁场相啮合。内环和外环都由强永磁体组装而成，内环和外环中的极对数以及铁片的数量决定了传动比。由于所有环之间的空气间隙很小，所以没有摩擦力。这种齿轮的实际实施可以变化，并且调节器环可以充当定子，或者可以直接附接到输出轴，然后外部磁体环充当定子。

[![UNC-gear](img/c1a040f93bad8234605c88d7007294a5.png)](https://hackaday.com/wp-content/uploads/2016/08/unc-gear.jpg)

Magnetic gearbox, research prototype of the UNC Coastal Studies Institute ([video source](https://www.youtube.com/watch?v=Sgr6IiRc8wc))

同轴磁性齿轮可以非常高效，几乎免维护，具有非常低的扭矩波动，并且可以在这些因素成为问题的情况下找到应用。低速时，它们的效率在 99.9 %的范围内。磁性齿轮的高齿轮比使它们对增加非常缓慢的输入力感兴趣，例如[海洋波浪能](http://coastalstudiesinstitute.org/research/coastal-engineering/renewable-ocean-energy-project-overview/improving-renewable-energy-device-efficiency-maintenance-and-power-output/)，这是一种由 UNC 海岸研究所开发的应用。同样的好处也让他们对风力涡轮机感兴趣。

磁性齿轮的另一个应用是船舶推进，它们用于将发动机的较高输入转速降低到螺旋桨轴所需的低转速和高扭矩。今年早些时候，罗尔斯·罗伊斯、ATB 劳伦斯·斯科特和磁力齿轮箱制造商 Magnomatics 宣布了他们为船只开发[磁力齿轮推进系统](http://www.drivesncontrols.com/news/fullstory.php/aid/5036/_A31.7m_project_will_use_magnetic_gears_for_marine_propulsion.html)的计划。磁性齿轮密封输入和输出力的能力在实验室和医疗环境中也很有用。

[![CMR printed magnetic gears](img/d2d20ebd8434540fc268193be9f2d9d4.png)](https://hackaday.com/wp-content/uploads/2016/08/cmr-printed-magnetic-gears.png)

Printed, magnetic gears by CMR, as demonstrated in [this video](https://www.youtube.com/watch?v=drD416THU7Y)

当然，磁力齿轮也有缺点。如前所述，最大扭矩可能不足以满足某些应用，而且价格昂贵，通常比普通齿轮重。此外，在非常高的转速下，由于调制器中的迟滞和涡流增加导致损耗增加，它们失去了效率优势。然而，正在进行的研究正在慢慢消除这些限制。CMR 的[可编程磁体允许强大、精细的磁结构，这可能允许未来更小、更高效、扭矩密度更高的磁齿轮。此外，对齿轮的要求也在变化。虽然在工业应用中扭矩越大越好，但交互式机器人应用需要屈服并确保人类用户安全的机制。](https://www.youtube.com/watch?v=drD416THU7Y)

磁性齿轮也可以在不需要重型齿轮切割机械的情况下制造，这使得它们对于 DIY 项目特别有意思。一个像样的同心磁性齿轮可以由一堆永磁体、容易获得的硬件和 3D 打印零件组装而成。我们的读者是怎么想的，你会在一个项目中使用磁力齿轮吗？你在我这里错过的应用中遇到过磁性齿轮吗？让我们知道并在评论中分享你的想法吧！

感谢 Hackaday.io 会员[magnets]，他在看到下面的视频后请求了这篇帖子:

 [https://www.youtube.com/embed/PyBTE5cjGDY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PyBTE5cjGDY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Ralph Bijker]创建了标题图形中使用的[齿轮渲染图](https://www.flickr.com/photos/17258892@N05/2588347668/)！