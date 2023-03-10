# 在 Arduino 上学习功能反应式编程

> 原文：<https://hackaday.com/2016/05/25/learn-functional-reactive-programming-on-your-arduino/>

每个人都喜欢学习一门新的编程语言，对吗？嗯，即使你不喜欢它，你也应该这样做，因为从不同的角度思考问题对想象力很有帮助。

[Juniper](http://www.juniper-lang.org/tutorial.html) 是一种用于 Arduino 平台的[函数式反应式编程语言](https://en.wikipedia.org/wiki/Functional_reactive_programming)。这意味着您将使用匿名函数、映射/折叠操作、递归和信号来编写代码。这就像是把你应该编程的事件驱动风格往前推了一步；你写`a=b+3`，当`b`改变时，编译器会自动为你改变`a`。(那是[【无功】](https://en.wikipedia.org/wiki/Reactive_programming)部分。)

[![functional](img/c1e3d6af4bf8ae188438c30d263c6b8e.png)](https://hackaday.com/wp-content/uploads/2016/05/functional.png) 如果你习惯了 Arduino(和大多数 C/C++)编程的先做这个再做那个的风格，这将是一次思维拓展。但是我们*确实*注意到许多微控制器代码寻找环境中的变化，然后(或多或少异步地)作用于这些数据。在这个抽象层次上，类似 Juniper 的东西看起来很合适。

改变 Arduino 的编程范式是一个雄心勃勃的项目，特别是考虑到它是由两个本科生[Caleb Helbling]和[Louis Ades]作为一个高级设计项目开始的。它也是全新的，所以还没有太多的代码库。时间和你的参与会证明它是否有用。但有一件事是肯定的，一旦你用反应式语言编程，你就不可能再看到同样的延迟循环。

你给微控制器编程时用过的最奇怪的语言是什么？

( [XKCD](https://xkcd.com/1270/) 漫画的 alt-text 写着“函数式编程将抽象数学的灵活性和强大性与抽象数学的直观清晰性结合在一起”。)