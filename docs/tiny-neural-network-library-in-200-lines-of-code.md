# 200 行代码的微型神经网络库

> 原文：<https://hackaday.com/2018/04/08/tiny-neural-network-library-in-200-lines-of-code/>

神经网络已经成为主流，拥有许多重型工具和库。如果你想在一台小电脑上安装一个网络，该怎么办？有[tinn——微小的神经网络](https://github.com/glouw/tinn)。如果你能用 C 或 C++编译器编译 200 行标准 C 代码，你就成功了。不依赖于其他代码。

另一方面，也没有太多的文档。但是，在头文件和两个例子之间，你应该能搞清楚。毕竟，代码并不多。存储库中的示例指导您从互联网下载一个[手写数字识别数据集](https://archive.ics.uci.edu/ml/datasets/semeion+handwritten+digit)。一旦它训练了这些数据，它会向您显示数据集中第一项的预期输出，然后处理第一项并向您显示结果。

为了简单起见，测试程序只使用第一个训练项目。但是，请记住，程序在训练期间会打乱数据，因此您不会总是得到相同的结果。下面是一个输出示例:

```
0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 0.000000 1.000000 
0.000294 0.000581 0.000000 0.000045 0.000101 0.002943 0.000000 0.000000 0.000408 0.998187
```

最上面一行是预期的结果。所有的数字都是零，除了最后一个，因为这是一个数字“9”输入。最下面一行显示了网络的结果。大多数值不是零，而是接近于零。最后一个值不完全是 1，但很接近。

您可能更喜欢在自述文件中查看更简单的程序:

```
#include "Tinn.h"
#include <stdio.h>

#define len(a) ((int) (sizeof(a) / sizeof(*a)))

int main()
{
   float in[] = { 0.05, 0.10 };
   float tg[] = { 0.01, 0.99 };
 /* Two hidden neurons */
   const Tinn tinn = xtbuild(len(in), 2, len(tg));
   for(int i = 0; i < 1000; i++)
     {
     float error = xttrain(tinn, in, tg, 0.5);
     printf("%.12f\n", error);
     }
   xtfree(tinn);
   return 0;
}
```

第一个数组是预期输入，第二个数组是预期输出。这个简单的程序实际上并不使用它训练的网络，但是`xtpredict`函数很容易添加。

如果你想要更多关于神经网络的资料，我们可以帮你。还有其他可用的[工具和技术](https://hackaday.com/2017/04/24/neural-networks-youve-got-it-so-easy/)的概要。