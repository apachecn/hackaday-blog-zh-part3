# 有风格的状态机！

> 原文：<https://hackaday.com/2016/10/10/the-collatz-o-matic-a-state-machine-with-style/>

如果你曾经认为用手算出一个排序序列是*好的*但是缺少按钮和灯光，那么【mechatronicsguy】的[排序序列](https://tinkerings.org/2016/10/06/the-collatz-o-matic/)已经帮你搞定了！

[![collatz-o-matic-closeup](img/8fd006800678126d71fa4cdd99b70d87.png)](https://hackaday.com/wp-content/uploads/2016/10/collatz-o-matic-closeup.jpg) 该设备是一种类型的[标签系统](https://en.wikipedia.org/wiki/Tag_system)计算器。【mechatronicsguy】解释了标签系统是一种类似图灵机的计算方法；它由不确定长度的读&写 FIFO 阵列(或磁带或队列)组成，在每一步，系统读取“头部”的符号，从“头部”删除固定数量的符号，并根据第一个符号是什么，将一个或多个符号附加到“尾部”。然后，无论新的符号在哪里，都重复这个过程。

Collatz-o-Matic 使用 RGB LED 字符串来表示队列，其设置方式如下:

1.  从队列前面删除两个符号(标签)。
2.  如果删除的第个符号是:
    1.  a–然后将 BC 写到队列的末尾
    2.  b–然后在队列末尾写下 A
    3.  c–然后将 AAA 写在队列的后面

数字就像任何其他符号一样容易表示，Collatz *猜想*是，无论你从哪个整数开始，系统([可能是](https://en.wikipedia.org/wiki/Collatz_conjecture))总是最终达到状态 1。下面嵌入了演示该设备的视频。

 [https://www.youtube.com/embed/5EdDBzXGQao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5EdDBzXGQao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



LED 灯条是不定长度胶带的巧妙替代品。与图灵机的相似之处是显而易见的，过去我们已经看到了图灵机的各种[物理实现——有些做工精致。](http://hackaday.com/2016/08/18/the-turing-tapes/)