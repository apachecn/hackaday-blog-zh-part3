# 定制灯泡固件

> 原文：<https://hackaday.com/2017/10/01/custom-lightbulb-firmware/>

随着爱好者和公司争相开发最新、最棒的家庭自动化设备，物联网正在快速发展。一些人特别感兴趣的一个领域是照明——是的，即使是不起眼的灯泡现在也有了大脑，黑客攻击的时机已经成熟。

[补锅匠]从彻底拆卸 Sonoff B1 灯泡开始。这是一款受欢迎的设备，在易贝售价不到 20 美元。额定功率为 6 瓦，灯泡有一个散热器，似乎远远大于必要的。里面是通常的交流/DC 转换器，LED 驱动器和一个 ESP8285 运行显示。虽然这是一个与通常的 ESP8266 略有不同的器件，但通过选择正确的编程模式，它可以以相同的方式[进行编程。](http://wp.me/pk3lN-19BP)

这就是有趣的地方——【补锅匠】用一种叫做 [ESPurna 的定制固件刷新设备。](https://bitbucket.org/xoseperez/espurna/wiki/Home)该固件能够更好地控制灯泡的功能，从颜色选择到通过 MQTT 对灯泡说话。

[补锅匠]很好地完成了拆卸和重新编程灯泡所需的精确步骤，并触及了定制固件带来的额外灵活性。我们喜欢看到像这样的项目，它们能够更好地控制物联网设备，并使用户能够更好地将它们与其他系统集成。