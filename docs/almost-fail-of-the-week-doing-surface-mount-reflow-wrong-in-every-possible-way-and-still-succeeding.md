# 本周几乎失败:尽一切可能做错表面贴装回流焊，但仍然成功

> 原文：<https://hackaday.com/2016/08/12/almost-fail-of-the-week-doing-surface-mount-reflow-wrong-in-every-possible-way-and-still-succeeding/>

有时候最好的学习方法是从别人的成功中学习。有时候失败是最好的老师。在这种情况下,[我们从[Tim Trzepacz]尝试使用回流炉将一块电路板焊接到另一块电路板的连续失败中吸取教训。他们不知何故互相抵消了，他最终有了一个工作委员会。用过回流焊炉的，会有翻白眼的。](https://hackaday.io/project/11367-megsy-a-homebrew-teensy-3/log/41123-first-build-of-megsy-pcb)

[Tim]的第一个错误是使用常规焊料而不是锡膏。我们可以看到他是如何合乎逻辑地到达那里的；如果你手工焊接一个 SMD，你要先把焊料熔化到焊盘上，这样更容易。然而，结果是，由于焊盘上的焊料滴，他的两块电路板不会平放在一起。

他没有被吓住，把木板一层一层地放在一起，把烤箱加热到 650 度。不完全是。该死的烤箱没有转到 11 点，所以他认为 500 也可以。完全错过了提示，他让他的板在接近 1000 华氏度的烤箱中烘烤，直到他注意到一些烟雾，他直觉地知道，绝对不应该发生。

电路板变黑了，阻焊膜从基板上冒出来了，人们过来看表演，他认为成功还是有可能的。他用活页夹把加热的木板夹在一起，直到它们冷却。有人给他上了一堂[回流](http://hackaday.com/2016/06/26/i-can-reflow-merit-badge/)的课，想必是听得耳朵都红了。

羞愧和失败，他回家了。然而，他心中有一个疑问。当然，这看起来很糟糕，但是这种板真的能工作吗？经过快速测试，答案是肯定的。它加载了一些代码，一段时间后，他愉快地开始了黑客攻击。去想想。