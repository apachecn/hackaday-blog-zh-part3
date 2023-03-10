# 口袋妖怪 Go-机器人版

> 原文：<https://hackaday.com/2016/07/26/pokemon-go-bot-edition/>

一条野蟒出现了，它想玩 Pokemon Go。当你不能的时候，Python 机器人正在接管游戏，它们很好。因为你迟早会碰到一个，所以这里有一个概述:

第一批可用的机器人之一和许多(肮脏)代码的来源，以及(一点也不肮脏)口袋妖怪训练者俱乐部客户秘密，是[【Mila 432 的】口袋妖怪 Go 机器人](https://github.com/Mila432/Pokemon_Go_API)。他最初的目标之一是更好地理解 API，结果比他希望的要好。

他不想冲动地破坏已经建立在部分已知的 API 上的众多有用的应用程序，所以决定让这个项目远离 Niantic 的雷达。他的机器人的最新(也是最强大的)版本还没有发布。当前版本在其有限的功能范围内运行良好:四处游荡和抢劫 Pokestops。

在其他地方，[Mila 432]的 API 代码被清理和重组，但剩下的大部分是 PTC 客户端的秘密和对 API 的理解。特别是[【tejado 的】API 代码库](https://github.com/tejado/pgoapi/tree/master)和[【AeonLucid 的】协议缓冲](https://github.com/AeonLucid)，激发了一些新的 bot 项目。其中[【鲁本·维勒肯的】API 和演示机器人](https://github.com/rubenvereecken/pokemongo-api)，可以处理更多的基本功能，比如抓口袋妖怪。它的 bot 例程四处游荡，掠夺和捕捉它能找到的一切(如果没有从演示代码中注释)。

最终，我们迄今为止遇到的最先进的 Python 机器人是[PokemonGoF] 的超级机器人[。这个机器人不仅实现了所有已知的 API 函数，而且战略性地使用它们。这个高度可配置的机器人可以被设置成只保留特定的口袋妖怪和特定的属性，其余的用来交换糖果。它还可以进化口袋妖怪，孵化鸡蛋，并具有一个](https://github.com/PokemonGoF/PokemonGo-Bot)[“人类行为”](https://github.com/PokemonGoF/PokemonGo-Bot/blob/master/pokemongo_bot/human_behaviour.py)——一个禁令预防技巧，为其行动增加了一定的随机性。它甚至在地图上显示它在做什么，正如你在标题动画中看到的。

不管是不是人类行为，它们都有一个共同点:经过一天的使用，它们让我们的测试账户充满了物品，口袋妖怪和 XP，尽管这些账户仍然完全可用。没有禁令，一切正常。这实际上是相当毁灭性的。尽管风险自担，或者更好:在评论中让我们知道人类玩家如何打败一大群机器人！

 [https://www.youtube.com/embed/rtGyUPhrGY0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rtGyUPhrGY0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

