# CUDA 就像拥有一台超级计算机

> 原文：<https://hackaday.com/2018/03/19/cuda-is-like-owning-a-supercomputer/>

超级计算机这个词经常被使用。例如，最初的 Cray-1 运算速度约为 150 MIPS，内存约为 8 兆字节。现代的英特尔 i7 CPU 可以达到近 250，000 MIPS，内存不太可能少于 8g，可能还会更多。当然，MIPS 不是一个很好的性能数字，但显然，一台高端 PC 比旧的 Cray 要强大得多。问题是，这永远不够。

[![](img/acd63d71f101bd48c156cf5c9ab1758f.png)](https://hackaday.com/wp-content/uploads/2018/03/cray1.jpg) 今天的计算机必须处理海量的像素、视频数据、音频数据、神经网络和长密钥加密。正因为如此，视频卡在过去被称为矢量处理器。也就是说，它们被优化为并行地对多个数据项进行操作。使用显卡处理进行计算有一些标准，今天我将向您展示使用 CUDA——NVIDIA 专有库来完成这项任务是多么简单。您也可以使用 OpenCL，它可以在许多不同种类的硬件上工作，但是我将向您展示它有一点冗长。

## 先吃甜点

作为一个成年人的好处之一就是你可以先吃甜点，如果你想吃的话。本着这种精神，我将向您展示两段代码，展示使用 CUDA 是多么简单。首先，这里有一段被称为“内核”的代码，它将在 GPU 上运行。

```
__global__
void scale(unsigned int n, float *x, float *y)
{
  int i = threadIdx.x;
  x[i]=x[i]*y[i];
}
```

有几件事需要注意:

*   __global__ 标签表明这个函数可以在 GPU 上运行
*   变量“I”的设置给出了当前的矢量元素
*   此示例假设有一个大小合适的线程块；否则，`i`的设置会稍微复杂一些，你需要在计算之前确认`i < n`

那么这个内核怎么叫呢？简单:

```
scale<<<1,1024>>>(1024,x,y);
```

当然，细节决定成败，但事情就是这么简单。在这种情况下，内核将`x`中的每个元素乘以`y`中相应的元素，并将结果留在`x`中。该示例将使用一个线程块处理 1024 个数据项，该线程块包含 1024 个线程。

您还需要等待线程在某个时候结束。一种方法是调用`cudaDeviceSynchronize()`。

顺便说一下，我使用 C 是因为我喜欢它，但是你也可以使用其他语言。例如，下面来自 NVidia 的视频显示了他们如何用 Python 做同样的事情。

 [https://www.youtube.com/embed/dPQnFXD7DxM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dPQnFXD7DxM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 网格、块等

[![](img/4b3b2d14c12d4a7705f78e954760469e.png)](https://hackaday.com/wp-content/uploads/2018/03/1200px-nvidia_quadro_fx_4000_agp.jpg) 细节当然有点丑，尤其是你想最大化表现的时候。CUDA 从你那里抽象出视频硬件。这是一件好事，因为您不必将您的问题与特定的视频适配器相适应。如果你真的想知道你正在使用的 GPU 的细节，你可以通过 API 查询或者使用开发者工具包附带的`deviceQuery`例子(稍后会有更多)。

例如，这里是我的设置的一部分输出:

```
CUDA Device Query (Runtime API) version (CUDART static linking)
Detected 1 CUDA Capable device(s)
Device 0: "GeForce GTX 1060 3GB"
CUDA Driver Version / Runtime Version 9.1 / 9.1
CUDA Capability Major/Minor version number: 6.1
Total amount of global memory: 3013 MBytes (3158900736 bytes)
( 9) Multiprocessors, (128) CUDA Cores/MP: 1152 CUDA Cores
GPU Max Clock rate: 1772 MHz (1.77 GHz)
Memory Clock rate: 4004 Mhz
Memory Bus Width: 192-bit
L2 Cache Size: 1572864 bytes
. . .
Maximum number of threads per multiprocessor: 2048
Maximum number of threads per block: 1024
Max dimension size of a thread block (x,y,z): (1024, 1024, 64)
Max dimension size of a grid size (x,y,z): (2147483647, 65535, 65535)
Maximum memory pitch: 2147483647 bytes

```

其中一些很难弄清楚，直到你了解更多，但关键是有九个多处理器，每个都有 128 个核心。时钟约为 1.8 GHz，内存也很大。另一个重要的参数是一个块最多可以有 1024 个线程。

那么什么是线程呢？还有一个街区？简单来说，一个线程运行一个内核。线形成可以是一维、二维或三维的块。一个块中的所有线程都在一个多处理器上运行，尽管不一定是同时运行。块被放在一起形成网格，网格也可以有一维、二维或三维。

[![](img/5f44c78e7bf7b2d7d9fdd72156b0e812.png)](https://hackaday.com/wp-content/uploads/2018/03/gridblock2.png)

所以还记得上面那行写着`scale<<>>`？它使用包含一个块的网格运行 scale 内核，该块中有 1024 个线程。迷茫？随着您尝试使用它，它会变得更加清晰，但其思想是将可以共享资源的线程分组，并并行运行它们以获得更好的性能。CUDA 使您所要求的工作在您所拥有的硬件上达到了一定的限制(比如，本例中每块 1024 个线程)。

## 网格步幅循环

那么，我们能做的一件事就是让我们的内核更加智能。我之前展示的简单示例内核每个线程只处理一个数据项。如果有足够的线程来处理数据集，那就没问题。通常情况下，情况并非如此。您可能有一个非常大的数据集，并且需要分块进行处理。

让我们来看一个愚蠢但能说明问题的例子。假设我有十个数据项要处理。这是愚蠢的，因为由于设置的开销，使用 GPU 处理十个项目可能是无效的。但是请原谅我。

由于我有很多多处理器，所以让 CUDA 做一个包含十个线程的块是没有问题的。然而，你也可以要两块五块的。事实上，您可以请求一个包含 100 个线程的块，它会忠实地创建 100 个线程。您的内核需要忽略所有会导致您越界访问数据的错误。CUDA 很聪明，但没那么聪明。

然而，真正强大的是当您指定的线程少于您拥有的项目时。这将需要一个包含不止一个块的网格，并且一个正确编写的内核可以计算多个值。

考虑这个内核，它使用所谓的网格步长循环:

```
__global__
void scale(unsigned int n, float *x, float *y)
{
 unsigned int i, base=blockIdx.x*blockDim.x+threadIdx.x, incr=blockDim.x*gridDim.x;
 for (i=base;i&lt;n;i+=incr) // note that i&gt;=n is discarded
   x[i]=x[i]*y[i];
}

```

这做同样的计算，但在一个循环中。基本变量是要处理的第一个数据项的索引。`incr`变量保存下一个项目有多远。如果您的网格只有一个块，这将退化为一次执行。例如，如果`n`是 10，我们有一个由 10 个线程组成的块，那么每个线程将获得一个唯一的基数(从 0 到 9)和一个 10 的增量。因为任何基数加 10 都会超过`n`，所以循环在每个线程中只会执行一次。

然而，假设我们要求一个有五个线程的块。那么线程 0 将获得基数 0 和增量 5。这意味着它将计算项目 0 和 5。线程 1 将获得具有相同增量的基数 1，因此它将计算 1 和 6。

当然，您也可以要求块大小为 1 到 10 个块，每个线程都在自己的块中。根据您所做的工作，所有这些情况都有不同的性能影响。为了更好地理解这一点，我编写了一个简单的示例程序供您试验。

## 软件和设置

假设你有一个 NVidia 显卡，你要做的第一件事就是[安装 CUDA 库](https://developer.nvidia.com/cuda-downloads)。您的 Linux 存储库中可能有一个版本，但请跳过它。它可能已经老得不成样子了。您也可以为 Windows(见下面的视频)或 Mac 安装。一旦你设置好了，你可能想要构建例子，尤其是`deviceQuery`例子，以确保一切正常并检查你的特定硬件。

你必须通过`nvcc`而不是你的系统 C 编译器来运行 CUDA 源文件，按照惯例这些文件有一个`.cu`扩展名。这让 CUDA 可以解释内核调用周围的尖括号等特殊情况。

 [https://www.youtube.com/embed/cL05xtTocmY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cL05xtTocmY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 一个例子

我已经在 [GitHub](https://github.com/wd5gnr/gocuda) 上发布了一个非常简单的例子。你可以用它在 CPU 和 GPU 处理上做一些测试。这段代码创建了一些内存区域并初始化它们。它还可以选择使用传统的 CPU 代码进行计算。然后，它还使用两个内核中的一个在 GPU 上执行相同的数学运算。一个内核是用于基准测试或正常使用的。另一个有一些调试输出，可以帮助您了解发生了什么，但是对执行时间没有好处。

通常情况下，你会选择 CPU 或 GPU，但如果你两者都做，程序会比较结果，看看是否有任何错误。它还可以有选择地从数组中转储一些字，这样您就可以看到发生了什么。我没有做很多错误检查，所以这对于调试来说很方便，因为如果发生错误，您会看到结果并不是您所期望的。

下面是程序的帮助文本:
[![](img/a95ab0edde844b60db88c35d490e82eb.png)](https://hackaday.com/wp-content/uploads/2018/03/gocuda11.jpg)

例如，要进行测试以展示块和网格如何处理十个项目，请尝试以下命令:

```
./gocuda g p d bs=10 nb=1 10
./gocuda g p d bs=5 nb=1 10

```

要生成大型数据集，您可以将`n`设为负值，它会将其作为 2 的幂。例如，-4 将创建 16 个样本。

## 是不是更快？

虽然这不是超级科学的，但当使用 GPU 或 CPU 时，您可以使用任何方法(如 Linux 上的`time`)来计时程序的执行。您可能会感到惊讶，GPU 代码的执行速度并不比 CPU 快多少，事实上，它通常更慢。这是因为我们的内核非常简单，现代 CPU 有自己的处理数组的技巧。您必须尝试更复杂的内核才能看到更多的好处。请记住，根据您的硬件，设置所有内存传输会有一些开销。

您还可以使用 CUDA 软件中包含的`nvprof`来获得运行在 GPU 上的东西的大量详细信息。试着将`nvprof`放在上面两个示例`gocuda`行的前面。您将看到一个报告，显示复制内存、调用 API 和执行内核所花费的时间。如果你也去掉“p”和“d”选项，你可能会得到更好的结果。

例如，在我的机器上，使用一个有十个线程的块需要 176.11 微秒。通过使用一个有五个线程的块，这个时间减少到了 160 微秒。不多，但是它展示了在一个线程中做更多的工作如何减少线程设置开销，当您做更多的数据处理时，这些开销会增加。

## OpenCL(打开 CL)

OpenCL 与 CUDA 有许多相同的目标，但它的工作方式不同。其中一些是必要的，因为它处理更多的设备(包括非 NVidia 硬件)。我不会评论太多的复杂性，但我会注意到你可以在 [GitHub](https://github.com/Dakkers/OpenCL-examples/blob/master/example00/main.cpp) 上找到一个简单的例子，我想你会同意，如果你不知道任何一个系统，CUDA 的例子更容易理解。

## 后续步骤

还有很多东西要学，但一次就够了。你可以浏览一下[文档](http://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html#programming-model)来获得一些想法。如果您的代码更加动态，并且有很多方法来组织内存和线程，那么您可以及时编译。真正的挑战是通过共享内存和优化线程使用来获得最佳性能。这有点像象棋。你可以学习动作，但成为一名优秀的球员需要更多。

没有英伟达硬件？你现在甚至可以在云中使用 CUDA。你可以看看 NVidia 的安装说明视频。

 [https://www.youtube.com/embed/1-NCTRKPfnw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1-NCTRKPfnw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



请记住，当你创建一个处理几兆字节图像或声音数据的程序时，你正在控制一台在 1976 年会让[西摩·克雷]流口水的超级计算机。