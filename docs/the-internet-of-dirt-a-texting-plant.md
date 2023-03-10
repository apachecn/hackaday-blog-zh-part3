# 肮脏的互联网，短信工厂

> 原文：<https://hackaday.com/2017/01/08/the-internet-of-dirt-a-texting-plant/>

我们都会在某个时候忘记给植物浇水。如果我们幸运的话，那么当我们匆忙浇水时，我们回到的虚弱的植物会神奇地复活，如果不是这样，我们就会有一个空花盆的耻辱来提醒我们的愚蠢。

没关系，你可能会想，我们可以用技术来解决这个问题，用微控制器来实现自动化！[【Bonnie】已经做到了这一点](http://www.instructables.com/id/Internet-of-Dirt-a-Texting-Plant/)，电容式土壤传感器为基于 ESP8266 的 Adafruit Feather HUZZAH 供电，该传感器进而通过 Adafruit IO 在线服务记录土壤湿度数据。IFTTT 小程序监控数据，并在湿度下降到需要浇水的程度时触发通知。

Instructables 的文章为整个过程提供了全面的分步指南，包括代码，因此这是一个几乎任何人都可以尝试的项目，也是对使用硬件在线服务的基本介绍。然而，我们不禁要问，如果让系统来浇水，而不是仅仅刺激一下它那多肉的园艺创造者，是否会更好。也许这是留给其他人建立一个添加作为增强。

这些年来，相当多的植物浇水自动化项目已经出现在这些页面上，从[这个使用汽车零件的项目](http://hackaday.com/2015/02/20/automated-plant-watering-system-uses-car-parts/)到一个带有令人印象深刻的[简单阀门的系统，该阀门是通过压缩一根软管](http://hackaday.com/2014/09/27/automated-watering-system-uses-neat-diy-water-valve/)制成的。不过，最终的浇水设备必须是[这款全自动温室机器人](http://hackaday.com/2013/09/12/fully-automated-watering-robot-takes-a-big-leap-forward-toward-greenhouse-automation/)。