# 甲骨文诉谷歌可能冷却软件开发

> 原文：<https://hackaday.com/2018/03/30/oracle-v-google-could-chill-software-development/>

除非你完全不看新闻，否则你可能知道甲骨文和谷歌之间的长期不和本周有了新的法院判决。上诉法院发现谷歌的合理使用的借口是不可接受的，他们确实侵犯了甲骨文对 Java 的版权。甲骨文要求大约 90 亿美元的损害赔偿，尽管实际金额尚未确定。此外，谷歌很可能会在做出任何实际判决之前将此事提交最高法院。

这条新闻是针对普通人的，所以关于到底发生了什么是相当光鲜的。我们开始尝试理解这一切。我们从[米凯拉·巴里]那里找到了一篇很好的文章，讲述了法院之前发现的事情。有三个主要部分:

*   有 37 个 API(应用程序编程接口)声明一字不差地取自 Java。如果你不熟悉 Java，这就像一个 C 头文件。
*   Google 反编译了 8 个安全文件并使用。
*   rangeCheck 函数——9 行 Java 代码——在 Oracle 的 Java 和 Android 中完全相同。

谷歌的理由是，这是合理使用，有具体的法律定义。在 Hackaday，我们不是律师，所以我们会让你自己去查这个定义。然而，套用[波特·斯图尔特法官]的话，“我们可能无法定义合理使用，但当我们看到它时，我们知道它。”

反编译安全文件似乎有点多。在这方面可能有一些理由。然而，创建一个符合另一个 API 的 API 是侵权的想法是相当可怕的。例如，Linux 提供了与 Unix(或 POSIX)类似的 API。API*本身*不是知识产权由来已久。

至于 rangeCheck 函数，确实看起来是抄袭的。然而，如果你看看代码，认为它在窃取任何人的秘密是非常可笑的:

```
private static void rangeCheck(int arrayLen, int fromIndex, int toIndex)
 {
 if (fromIndex > toIndex)
   throw new IllegalArgumentException("fromIndex(" +
     fromIndex + > toIndex(" + toIndex+")");
 if (fromIndex < 0) 
     throw new ArrayIndexOutOfBoundsException(fromIndex);
 if (toIndex > arrayLen) 
    throw new ArrayIndexOutOfBoundsException(toIndex);
}

```

我们可以想到 arrayLen、fromIndex 和 toIndex 的其他名称，但是实现是非常明显的，你不这样认为吗？

这不是一个简单的案件。一个法院判谷歌胜诉，下一个法院判甲骨文胜诉。我们认为你可以采取相反的策略。如果你出于某种目的花了几年时间构建了一个超级 API，为什么不能保护它？然而，不知何故，这似乎并不正确。也许这就像[波特·斯图尔特]的名言。如果你的 API 获得了一个数组并乘以 10 的版权，看起来你不应该能够保护它。但是我们可以想象一些复杂的逻辑 API，我们可能觉得它是知识产权。我们一时想不出，但可以想象。

更进一步来说，最初的案例中有一个专利部分被成功地反驳了。然而，作出本周裁决的法院通常不会审理版权案件，只审理这一个案件，因为专利部分不再是争论的焦点。

顺便提一下，至少有一些 Java 代码被 GNU 公共许可证所覆盖。然而，谷歌的代码——至少是其中的一部分——受到 Apache 开放许可证的保护，这种许可证显然更加宽松和不兼容。这个 90 亿美元的数字源于甲骨文断言谷歌扼杀了对其 Java 移动产品的需求。

我们期待对此有很多评论。你的 API 是你的知识产权吗？或者它们像数学公式或算法一样，天生不受版权保护？如果是，你如何阻止大公司(或拥有合法资源的小公司)用无休止的琐碎 API 吞噬软件领域，用诉讼杀死所有人？