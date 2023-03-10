# Das 修复

> 原文：<https://hackaday.com/2017/03/09/das-fix/>

曾经有一段时间，你的键盘和鼠标等桌面外围设备都是昂贵的物品，你需要保存和照顾。但是，几十年来个人电脑的商品化和越来越便宜的制造已经使它们每一个都达到了几乎被抛弃的水平，它们是如此便宜，以至于当一个坏了，你可以不假思索地伸手去拿另一个。

这并不是说更昂贵的专业键盘已经没有市场了。你会发现发烧友们仍然执着于他们珍爱的老式 IBM 型和 Fs 型，或者在一系列竞争的高端主板上打字。你可能会说，如今廉价的键盘质量相当高，但对一些人来说，只有优质开关的感觉才会起作用。

[Mac2612]是这类外围设备的一个特别好的例子，一个 Das 键盘 4C，上面有商标 missing key 贴花。虽然有一个小问题，它在生命中的某个时候会发生溢出，并且会发出随机的按键，这使它变得无用。他对故障的马拉松式调查和修复是一个有趣的阅读，并让我们了解为什么这些键盘需要额外的钱。

![](img/de993f15f4bc7fec082f0e87ea801c35.png)

“To my dismay, I quickly realized that this was probably an unnecessary endeavor…”

起初，似乎电路板上的腐蚀可能是问题所在，所以他用异丙醇清洗了一下。一切都无济于事，因此开始了一系列进一步的拆卸和清理，最终导致所有关键开关的脱焊。这个冗长的任务向我们详细展示了高端电路板的构造，但遗憾的是，它并没有揭示故障，而且幻像按键不断出现。

沿着电路板的轨迹追溯到微控制器，他最终发现湿气已经腐蚀了 10K 表面贴装电阻器的末端，使其在欧姆表中具有电阻。由于这是一个键盘行的下拉，他找到了问题的根源。我们花了很长时间查找一个带有机械故障的 SMD 部件的电路板，我们感受到了他的痛苦。

更换 SMD 部件和重新组装给他一个相当可爱的键盘，尽管工作量很大。

这是我们为您带来的第一个 Das 键盘拆卸，但不是第一个键盘黑客。例如，有人[重新制造 F 型](http://hackaday.com/2016/03/07/reviving-the-best-keyboard-ever/)，或者[最简约的键盘](http://hackaday.com/2016/07/20/binary-keyboard-is-the-purest-form-of-input-device/)。

[感谢 Graham Heath，通过 [/r/MechanicalKeyboards](https://www.reddit.com/r/MechanicalKeyboards/comments/5xz1fd/modificationrepair_i_got_a_free_das_ultimate_4c/)