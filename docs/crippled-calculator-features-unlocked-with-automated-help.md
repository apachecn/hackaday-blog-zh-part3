# 受损的计算器功能在自动帮助下解锁

> 原文：<https://hackaday.com/2017/01/13/crippled-calculator-features-unlocked-with-automated-help/>

[Aguilera Dario]喜欢他的卡西欧 fx-82ES 计算器。然而，它缺少一些功能，包括复数。卡西欧 fx-991ES 的功能更多，但当然价格也更高。谷歌显示，如果你按下正确的按钮，你可以把 fx-82ES 变成 fx-991ES。

因为这显然是一个缓冲区溢出漏洞，黑客涉及到许多关键，一旦你循环电源，你不得不再次这样做。[Aguilera]意识到这将是自动化的一个很好的候选，并添加了一个微控制器来推动他的按钮。你可以在下面看到一个试验板版本的视频。他还有一个 PCB 版本，应该可以更好地集成。

自动化硬件通过计算器 PCB 背面的测试垫插入按钮矩阵。[Aguilera]将带状电缆直接焊接到这些焊盘上，然后将它从计算器外壳背面切割的插槽中抽出，并在那里与 0.1”引脚插座端接。原型中使用了 Arduino Mini，下一个版本将在定制板上使用 ATmega328P。uC 使用古老的 4066 芯片与按钮连接接口，该芯片可以充当模拟开关。

PCB 版本的电路板布局显示在项目页面上。目前还不知道这是打算永久添加到计算器中，还是只是为了利用而插入并储存起来，以供下次循环供电时使用。无论哪种方式，了解这种利用都是很好的，而且自动化它也是一个很酷的挑战！

如果你不想破解一个现成的计算器，拿一些谢妮电子管[做你自己的](http://hackaday.com/2016/05/09/hackaday-prize-entry-a-programmable-calculator-with-nixie-tubes/)。或者，如果你缺少管子，试试[这个](http://hackaday.com/2015/08/18/hackaday-prize-entry-the-70s-called-they-want-this-calculator/)。

 [https://www.youtube.com/embed/c7waHOuBSYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/c7waHOuBSYY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

