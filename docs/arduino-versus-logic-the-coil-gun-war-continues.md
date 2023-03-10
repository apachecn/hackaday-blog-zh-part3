# Arduino 对逻辑:线圈枪战争继续

> 原文：<https://hackaday.com/2016/08/25/arduino-versus-logic-the-coil-gun-war-continues/>

看来一触即发的线圈控枪大战又开了一枪。这一次，【Great Scott】带着[一个使用单个 CMOS 芯片和几个晶体管的简化和改进的控制电路](https://fedetft.wordpress.com/2016/08/23/on-greatscotts-arduino-vs-common-ics-comparison/)来到了分立的木棚。它会在哪里结束？不会有人为孩子们着想吗？

最新的齐射是对[GreatScott]试图用分立逻辑控制 DIY 线圈枪的回应，这反过来也是对他采取简单方式并在[原始版本](http://hackaday.com/2016/08/19/coil-gun-for-newbies-learning-electromagnetic-propulsion/)中使用 Arduino 的评论的回应。[Great Scott]的第二次构建旨在证明最初的设计选择是正确的，并且似乎很好地解释了使用微控制器的构建是多么容易和更好。结案了，对吧？

没有。嵌入式设计师[fede.tft]甚至不确定设计是否接近优化，所以他开始工作——在他的假期里！他将元件数量减少到一个 CMOS 芯片(四施密特触发器 NAND)、几个开关晶体管、驱动线圈的 MOSFETs 和几个无源器件。Nand 设置为触发器，由射弹传感器触发和复位，射弹传感器实现为硬连线 AND 门。总元件数量实际上比原始 Arduino 构建中的支持元件要少，而且[fede.tft]甚至提供了一种替代方案的想法，取消了开关晶体管。

尽管[fede.tft]承认[GreatScott]击败了他，因为他实际上建造了两条电路，但还是要向他致敬，因为他向我们展示了只用几个元件就可以完成的事情。我们希望看到有人实现这种设计，并看看它可以变得多么简单。