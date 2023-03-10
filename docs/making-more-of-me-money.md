# 让我赚更多的钱

> 原文：<https://hackaday.com/2017/03/22/making-more-of-me-money/>

在过去的几年里，Hackaday 真的通过营销材料加强了我们的游戏。我们的 t 恤和礼品是首屈一指的，去年我们推出了“Benchoff Buck”(如上所述)，这是一种充满欢乐扳手欧元的法案，但尚未成为法定货币。至少在我们在沙漠里找到一个甜蜜的化合物之前。

[![](img/1207f04c2c7a769ed6ffbae50cc7563b.png) ](https://hackaday.com/wp-content/uploads/2017/03/benchoffnickel.jpg) [【安德鲁·索瓦】创造了板凳镍](http://andrewsowa.com/blog/2017/3/19/creating-the-benchoff-nickel)。这是你的真面目，印在 PCB 上，用 FR4、丝印、金色和奥什帕克的皇家紫色呈现。通过这样做，[安德鲁]为自己赢得了中尉军衔的战地任命，现在他可以预订沙滩车一整个周末。

基准镍是使用 KiCad 组件功能在 KiCad 中创建的。计划这需要一点工作；在 OSH Park PCB 上只有五种颜色，从白色到金色到米色到紫色(铜上的阻焊层)到黑色(不含铜的阻焊层)。幸运的是，我们现有的最好的一张我的照片在五种颜色中表现得非常好。

不过，KiCad 的 bitmap 2 组件只能帮你做到这一步。它主要用于将丝印标志放在板上，摆弄铜和掩膜层超出了它的功能。为了将我面部的不同图层导入到 KiCad PCB 的不同图层中，[Andrew]必须打开记事本进行一些手动编辑。很烦，但是是的，可以做到。

[![](img/79b66e7389dad67ac72d5df7fd43f540.png)](https://hackaday.com/wp-content/uploads/2017/03/benchoffnickles.jpg)

OSH Park’s fabs apparently use two different tones of FR4

《板凳镍》可以在 Github 上找到[，也可以在奥什公园](https://github.com/Junes-PhD/Benchoff-Nickel)上作为[的共享项目找到(三本 22.55 美元)。奥什公园制造过程中的一个小小的好奇心出现在[安德鲁]的第二个板凳镍币订单上。OSH Park 使用至少两个板房来生产多氯联苯，其中一个显然使用了较浅的 FR4。这导致了第二阶板凳镍币的较浅肤色。](https://oshpark.com/shared_projects/943h1NuJ)

这确实是一项巨大的工作。我从未见过这样的东西，这是我手中握过的最好的“艺术”PCB 之一。当[Andrew]在芝加哥的[hack aday un conference 上递给我一个这样的东西时，我真是大吃一惊。我将在本周的中西部说唱音乐节上再次与安德鲁交谈，我们将尝试找出一些方法来做一个小规模的板凳镍币。](https://hackaday.io/event/20141-hackaday-unconference-chicago)

编辑:奥什帕克揭示了为什么 FR4 会有不同的音调。总之，没有。肤色较浅的其实是 FR408，用在 4 层板上。

[![](img/098c18712140f2039c54e3f2d55f6b7e.png)](https://hackaday.com/wp-content/uploads/2017/03/oshpark.png)