# 张量流简介

> 原文：<https://hackaday.com/2017/04/11/introduction-to-tensorflow/>

在 90 年代，我非常喜欢编写神经网络软件，并且我一直渴望尝试使用 [TensorFlow](https://www.tensorflow.org/) 创建一些软件。

谷歌的机器智能框架是现在的新热点。当 TensorFlow [可以安装在 Raspberry Pi](https://github.com/samjabrahams/tensorflow-on-raspberry-pi) 上时，使用它变得非常容易。在很短的时间内，我制作了一个以二进制计数的神经网络。所以我想我应该把我目前学到的东西传授给大家。希望这能让其他想尝试的人，或者只是想深入了解神经网络的人更容易。

## What Is TensorFlow?

引用 TensorFlow 网站的话，TensorFlow 是一个“使用数据流图进行数值计算的开源软件库”。我们所说的“数据流图”是什么意思？这才是最酷的部分。但在我们回答这个问题之前，我们需要谈一谈简单神经网络的结构。

![Binary counter neural network](img/e38db12ddfe7fa950efd9c8c4dadca97.png)

Binary counter neural network

## 神经网络基础

一个简单的神经网络有一些输入单元。它也有隐藏单元，所谓的隐藏单元是因为从用户的角度来看，它们实际上是隐藏的。还有输出单位，从中我们得到结果。旁边还有偏置单元，用于帮助控制隐藏单元和输出单元发出的值。连接所有这些单元的是一堆权重，这些权重只是数字，每个权重都与两个单元相关联。

我们向这个神经网络灌输智能的方法是给所有这些权重赋值。这就是训练神经网络所做的，为这些权重找到合适的值。在我们的示例中，一旦完成训练，我们将把输入单元分别设置为二进制数字 0、0 和 0，TensorFlow 将处理其间的所有内容，输出单元将神奇地分别包含二进制数字 0、0 和 1。如果你错过了，它知道二进制 000 后面的下一个数字是 001。对于 001，它应该吐出 010，依此类推直到 111，其中它会吐出 000。一旦这些重量被正确设置，它就会知道如何计数。

![Binary counter neural network with matrices](img/ba01e9cf6a5d02e235f3e1731b0db3e9.png)

Binary counter neural network with matrices

“运行”神经网络的一个步骤是将每个权重的值乘以其输入单元的值，然后将结果存储在关联的隐藏单元中。

我们可以把单位和重量重画成数组，或者 Python 中所谓的列表。从数学的角度来看，它们是矩阵。我们在图中只重画了其中的一部分。将输入矩阵与权重矩阵相乘涉及简单的矩阵乘法，从而产生五元素隐藏矩阵/列表/数组。

## 从矩阵到张量

在 TensorFlow 中，这些列表被称为张量。矩阵乘法步骤被称为运算，或者用程序员的话来说是 op，如果你打算阅读 TensorFlow 文档，你必须习惯这个术语。进一步说，整个神经网络是张量和对其进行运算的运算的集合。它们合在一起构成了一幅图。

 [![Binary counter's full graph](img/b658d7c46e5f1958b22dcd7d2c6776a2.png "Binary counter's full graph")](https://hackaday.com/2017/04/11/introduction-to-tensorflow/tb_bincounter_full_graph/) Binary counter’s full graph [![layer1 expanded](img/5e23724cf26f0b75fcd4f1d38e49e54a.png "layer1 expanded")](https://hackaday.com/2017/04/11/introduction-to-tensorflow/tb_bincounter_expanded_graph/) layer1 expanded

这里显示的是为 [TensorBoard 拍摄的快照，TensorBoard 是一种用于可视化图形](http://hackaday.com/2017/03/24/ten-minute-tensorflow-speech-recognition/)以及在训练期间和之后检查张量值的工具。张量是线，写在线上的是张量的维数。连接张量的是所有的 ops，尽管您看到的一些东西可以双击以展开更多细节，就像我们在第二张快照中对第 1 层所做的那样。

最底部是 x，我们给占位符 op 起的名字，它允许我们为输入张量提供值。从它向左上方的线是输入张量。继续沿着这条线走，你会找到矩阵乘法运算，它用输入张量和另一条通向矩阵乘法运算的张量进行矩阵乘法运算，张量代表权重。

所有这些只是为了让您对什么是图及其张量和 ops 有一个感觉，让您更好地理解我们所说的 TensorFlow 是一个“使用数据流图进行数值计算的软件库”。但是我们为什么要创建这些图表呢？

## 为什么要创建图表？

目前稳定的 API 是 Python，一种解释型语言。神经网络是计算密集型的，一个大型网络可能有数千甚至数百万个权重。通过解释每一步来计算将会花费很长时间。

因此，我们创建了一个由张量和 ops 组成的图，描述神经网络的布局、所有数学运算，甚至变量的初始值。只有在我们创建了这个图之后，我们才把它传递给 TensorFlow 所说的会话。这就是所谓的延迟执行。该会话使用非常高效的代码运行图形。不仅如此，许多操作，如矩阵乘法，[可以在受支持的 GPU](https://www.tensorflow.org/tutorials/using_gpu) (图形处理单元)上完成，会话将为您完成这些操作。此外，TensorFlow 被构建为能够跨多台机器和/或 GPU 分布处理。给它一张完整的图表就可以做到这一点。

## 创建二进制计数器图

这是我们二进制计数器神经网络的代码。你可以在 GitHub 页面上找到完整的源代码。请注意，其中有额外的代码用于保存 TensorBoard 使用的信息。

我们将从创建张量和 ops 图的代码开始。

```
import tensorflow as tf
sess = tf.InteractiveSession()

NUM_INPUTS = 3
NUM_HIDDEN = 5
NUM_OUTPUTS = 3

```

我们首先导入`tensorflow`模块，创建一个供以后使用的会话，并且，为了使我们的代码更容易理解，我们创建了几个包含网络中单元数量的变量。

```
x = tf.placeholder(tf.float32, shape=[None, NUM_INPUTS], name='x')
y_ = tf.placeholder(tf.float32, shape=[None, NUM_OUTPUTS], name='y_')

```

然后，我们为输入和输出单元创建占位符。占位符是一个 TensorFlow 运算，我们稍后将为其提供值。`x`和`y_`现在是新图中的张量，每个都有一个`placeholder` op 与之关联。

你可能想知道为什么我们把形状定义为二维列表的`[None, NUM_INPUTS]`和`[None, NUM_OUTPUTS]`，为什么把第一维定义为`None`？在上面的神经网络概述中，看起来我们会一次给它一个输入，并训练它产生一个给定的输出。不过，如果我们一次给它多个输入/输出对，也就是所谓的批处理，效率会更高。第一个维度是每批中输入/输出对的数量。在我们实际给出一个之前，我们不会知道一批中有多少个。事实上，我们在培训、测试和实际使用中使用相同的图表，因此批量大小不会总是相同的。所以我们现在使用 Python 占位符对象`None`作为第一维的大小。

```
W_fc1 = tf.truncated_normal([NUM_INPUTS, NUM_HIDDEN], mean=0.5, stddev=0.707)
W_fc1 = tf.Variable(W_fc1, name='W_fc1')

b_fc1 = tf.truncated_normal([NUM_HIDDEN], mean=0.5, stddev=0.707)
b_fc1 = tf.Variable(b_fc1, name='b_fc1')

h_fc1 = tf.nn.relu(tf.matmul(x, W_fc1) + b_fc1)

```

接下来是创建神经网络图的第一层:权重`W_fc1`，偏差`b_fc1`，以及隐藏单元`h_fc1`。“fc”是一个约定，意思是“完全连接”，因为权重将每个输入单元连接到每个隐藏单元。

`tf.truncated_normal`产生多个 op 和 tensorss，这些 op 和 tensor 随后会将标准化的随机数分配给所有权重。

`Variable`操作被赋予一个值来进行初始化，在本例中是随机数，并在多次运行中保持它们的数据。它们还可以方便地将神经网络保存到文件中，这是你在训练后想要做的事情。

您可以看到我们将在哪里使用`matmul` op 进行矩阵乘法。我们还插入了一个`add` op，它将增加偏置权重。`relu` op 执行我们所说的激活功能。矩阵乘法和加法是线性运算。仅使用线性运算，神经网络可以学习的东西非常有限。激活函数提供了一些非线性。在 relu 激活函数的情况下，它将任何小于零的值设置为零，所有其他值保持不变。信不信由你，这样做打开了另一个可以学习的世界。

```
W_fc2 = tf.truncated_normal([NUM_HIDDEN, NUM_OUTPUTS], mean=0.5, stddev=0.707)
W_fc2 = tf.Variable(W_fc2, name='W_fc2')

b_fc2 = tf.truncated_normal([NUM_OUTPUTS], mean=0.5, stddev=0.707)
b_fc2 = tf.Variable(b_fc2, name='b_fc2')

y = tf.matmul(h_fc1, W_fc2) + b_fc2

```

第二层的权重和偏差设置与第一层相同，但输出层不同。我们将再次进行矩阵乘法，这次是将权重和隐藏单元相乘，然后加上偏差权重。我们把激活函数留给了下一段代码。

```
results = tf.sigmoid(y, name='results')

cross_entropy = tf.reduce_mean(
tf.nn.sigmoid_cross_entropy_with_logits(logits=y, labels=y_))

```

Sigmoid 是另一个激活函数，类似于我们上面遇到的 relu，它提供非线性。我在这里使用 sigmoid，部分原因是因为 sigmoid 等式产生的值介于 0 和 1 之间，非常适合我们的二进制计数器示例。我使用它也是因为它适用于多个输出单元可以有一个大值的输出。在我们的例子中，为了表示二进制数 111，所有的输出单元都可以有较大的值。当进行图像分类时，我们想要完全不同的东西，我们想要一个输出单元产生一个大的值。例如，如果图像包含长颈鹿，我们希望表示长颈鹿的输出单元具有较大的值。像 [softmax](https://en.wikipedia.org/wiki/Softmax_function) 这样的东西对于图像分类来说是个不错的选择。

仔细看，似乎有些重复。我们似乎插入乙状结肠两次。我们实际上是在创建两个不同的并行输出。`cross_entropy`张量将在神经网络的训练中使用。`results`张量将在我们稍后运行训练好的神经网络时使用，不管它是为了什么目的而创建的，在我们的情况下是为了好玩。我不知道这是不是最好的方法，但这是我想到的方法。

```
train_step = tf.train.RMSPropOptimizer(0.25, momentum=0.5).minimize(cross_entropy)

```

我们添加到图表中的最后一块是培训。这是根据训练数据调整所有权重的一个或多个操作。请记住，我们仍然只是在创建一个图表。实际的训练将在我们运行图表时进行。

有一些优化器可供选择。我选择`tf.train.RMSPropOptimizer`是因为，像 sigmoid 一样，它适用于所有输出值都很大的情况。对于像做图像分类时一样分类的东西，`tf.train.GradientDescentOptimizer`可能更好。

## 训练和使用二进制计数器

创建图表后，是时候进行培训了。一旦经过训练，我们就可以使用它了。

```
inputvals =  [[0, 0, 0], [0, 0, 1], [0, 1, 0], [0, 1, 1], [1, 0, 0], [1, 0, 1],
              [1, 1, 0], [1, 1, 1]]
targetvals = [[0, 0, 1], [0, 1, 0], [0, 1, 1], [1, 0, 0], [1, 0, 1], [1, 1, 0],
              [1, 1, 1], [0, 0, 0]]

```

首先我们有一些训练数据:`inputvals`和`targetvals`。`inputvals`包含输入，每个输入都有相应的`targetvals`目标值。对于`inputvals[0]`我们有`[0, 0, 0]`，期望输出是`targetvals[0]`，也就是`[0, 0, 1]`，以此类推。

```
if do_training == 1:
  sess.run(tf.global_variables_initializer())

  for i in range(10001):
    if i%100 == 0:
      train_error = cross_entropy.eval(feed_dict={x: inputvals, y_:targetvals})
      print("step %d, training error %g"%(i, train_error))
      if train_error < 0.0005:
        break

    sess.run(train_step, feed_dict={x: inputvals, y_: targetvals})

  if save_trained == 1:
    print("Saving neural network to %s.*"%(save_file))
    saver = tf.train.Saver()
    saver.save(sess, save_file)

```

`do_training`和`save_trained`可以硬编码，并根据每次使用进行更改，或者可以使用命令行参数进行设置。

我们首先检查所有这些`Variable`运算，让它们初始化张量。

然后，我们从底部到`train_step`张量运行图表多达 10001 次，这是我们添加到图表中的最后一个东西。我们将`inputvals`和`targetvals`传递给`train_step`的 op 或 ops，这是我们使用`RMSPropOptimizer`添加的。这是调整所有权重的步骤，使得给定的输入将导致接近相应的目标输出。如果目标输出和实际输出之间的误差很快变得足够小，那么我们就跳出了循环。

如果你有数千个输入/输出对，那么你可以一次给它其中的一个子集，就是我们前面提到的那批。但是这里我们只有八个，所以我们每次都给他们。

如果我们愿意，我们也可以将网络保存到一个文件中。一旦它训练好了，我们就不需要再训练了。

```
else: # if we're not training then we must be loading from file

  print("Loading neural network from %s"%(save_file))
  saver = tf.train.Saver()
  saver.restore(sess, save_file)
  # Note: the restore both loads and initializes the variables

```

如果我们没有训练它，那么我们就从一个文件中加载训练好的网络。该文件仅包含具有`Variable`操作的张量的值。它不包含图形的结构。因此，即使在运行已经训练好的图表时，我们仍然需要代码来创建图表。有一种方法可以使用[元图](https://www.tensorflow.org/programmers_guide/meta_graph)从文件中保存和加载图形，但是我们在这里不这么做。

```
print('\nCounting starting with: 0 0 0')
res = sess.run(results, feed_dict={x: [[0, 0, 0]]})
print('%g %g %g'%(res[0][0], res[0][1], res[0][2]))
for i in range(8):
res = sess.run(results, feed_dict={x: res})
print('%g %g %g'%(res[0][0], res[0][1], res[0][2]))

```

无论哪种情况，我们都要试一试。请注意，我们从图形的底部向上运行它，直到我们上面讨论过的结果张量，这是我们在利用训练好的网络时特别创建的重复输出。

我们给它 000，希望它返回接近 001 的值。我们传递返回的内容，返回并再次运行它。我们一共运行了 9 次，足够从 000 数到 111，然后再回到 000。

![Running the binary counter](img/c4d64aade454e5d2132f3af672427663.png)

Running the binary counter

这是成功训练和后续计数期间的输出。请注意，它在循环中训练了 200 步。偶尔，它会完成所有 10001 个步骤，但没有充分减少训练错误，但一旦你成功地训练并保存了它，那就不重要了。

## 下一步

正如我们所说，二进制计数器神经网络的代码在我们的 github 页面上。你可以从那里开始，从头开始，或者使用 [TensorFlow 网站](https://www.tensorflow.org/)上的许多教程中的任何一个。让它在硬件上做些什么肯定是我的下一步，从[这个机器人身上获得灵感【卢卡斯·比沃德】让它识别他工作室周围的物体](http://hackaday.com/2016/10/09/tensorflow-robot-recognizes-objects/)。

您正在使用或计划使用 TensorFlow 做什么？请在下面的评论中告诉我们，也许我们会在以后的文章中尝试一下！