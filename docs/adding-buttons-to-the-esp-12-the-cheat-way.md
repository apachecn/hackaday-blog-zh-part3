# 向 ESP-12 添加按钮——作弊方式

> 原文：<https://hackaday.com/2017/03/23/adding-buttons-to-the-esp-12-the-cheat-way/>

[sorki]有一个 ESP-12F，想玩 nodeMCU，但发现他们缺少复位和闪光按钮。我们都有过这种经历——在试验板上摆弄一个项目，试图通过用电线短路引脚或弯曲元件腿来节省焊接按钮所需的时间。当微控制器不可避免地出错时，这要么不起作用，要么以阻塞微控制器而告终。[[Buger]找到了一个更整洁的解决方案，用最少的努力给 ESP-12F 添加按钮。](http://buger.dread.cz/esp12-f-reset-and-flash-button-hack.html)

这是 deadbug 精神在按钮上的体现。一根导线的一侧被焊接到需要被拉下的引脚上。组件腿边角料是这方面的理想选择。电线的另一端向上弯曲，漂浮在 ESP-12 的金属屏蔽上，该屏蔽接地。当你想要引脚变低时，将导线压入屏蔽层，使其接地。假设上拉电阻一切正常，放开它，引脚再次返回高电平。

这是一种快速的破解方法，比试图将一段连接电线的两端固定在适当的位置上要稳健得多。这也比试图找到一个触摸开关更容易，你也不会把它挂在电路板上。

对于令人印象深刻的死栓结构，看看这个由分立元件制成的时钟。

【感谢理查德·马尔科的提示！]