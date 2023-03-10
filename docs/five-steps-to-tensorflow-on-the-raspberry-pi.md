# 树莓派上张量流的五个步骤

> 原文：<https://hackaday.com/2018/05/18/five-steps-to-tensorflow-on-the-raspberry-pi/>

如果你有大约 10 个小时可以打发，你可以使用[Edje Electronics]的说明[在一个树莓 Pi 3](https://www.youtube.com/watch?v=WqCnW_2XDw8) 上安装 TensorFlow。平心而论，你照看孩子的时间大约是一个小时。剩下的时间用来建造东西，你不需要看着它前进。你可以在下面的视频中看到所需的步骤。

您需要至少带有 16 GB SD 卡的 Pi 和至少带有 1 GB 可用空间的 USB 驱动器。这不仅包含软件，还允许您创建一个交换文件，这样 Pi 将有足够的虚拟内存来构建所有需要的东西。

构建步骤不仅要创建 TensorFlow，还要创建 Bazel，这是 Google 基于 Java 的构建系统。TensorFlow 的版本和 Bazel 的版本之间存在依赖关系，因此您必须确保版本匹配，如视频中所述。

该视频基于 GitHub 上的一些旧指令，但这些指令不是最新的，视频中涵盖了所需的更改。

考虑到编译需要多长时间，我们想知道[交叉编译是否是更好的选择](https://hackaday.com/2016/02/03/code-craft-cross-compiling-for-the-raspberry-pi/)。如果你需要这种设置的模型，你可以[总是在你的浏览器](https://hackaday.com/2018/04/16/tensorflow-in-your-browser/)中工作。

 [https://www.youtube.com/embed/WqCnW_2XDw8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WqCnW_2XDw8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

