# 看着眼睛，为怜悯而哭泣

> 原文：<https://hackaday.com/2018/03/21/look-upon-eyepot-and-weep-for-mercy/>

希望你不是在期待一个不受噩梦困扰的夜晚。保罗-路易·阿革诺尽他的职责来确保洛夫克拉夫特式的机械化恐怖在你的潜意识中消失，他最近释放了一种恐怖，这种恐怖是对一个毫无防备的世界的关注。这个[独眼的四条腿机器人茶壶](https://chapelierfou.org/blog/eyepot-a-creepy-teapot.html)从游戏*中的一个敌人那里获得灵感【爱丽丝:疯狂归来*，它的存在似乎除了让人毛骨悚然之外没有其他原因。

即使你没有做噩梦，也能从这个项目中学到很多东西。从 OpenSCAD 设计的 3D 打印组件到 Raspberry Pi Zero 和 Arduino Pro Mini 组合控制腿部的八个伺服系统，Paul-Louis Ageneau 在记录构建方面做了出色的工作。如果你想在家里一起玩，所有的信息和代码都在这里，尽管你可以跳过整个茶壶和眼球的事情。

第二篇文章解释了如何为 Arduino 和 Pi 编写代码，读起来很有启发性。Pi 上的 Python 脚本分解了运动学，并通过串行链路将适当的伺服角度传递给 Arduino。结合用于控制的 web 界面和来自茶壶的 Raspberry Pi 相机模块的流，你就拥有了世界上最恐怖的远程呈现机器人的气质。我们很想看到这个人在董事会桌上跺脚。

看起来我们最近和令人毛骨悚然的机器人朋友在一起。看到 Eyepot 和 JARVIS 之间的合作对我们来说可能太多了。虽然我们有一个很好的想法[我们会如何控制他们](http://hackaday.com/2018/03/17/control-a-swarm-of-rc-vehicles-with-esp8266/)。