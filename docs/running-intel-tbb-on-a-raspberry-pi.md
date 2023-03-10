# 在树莓派上运行英特尔 TBB

> 原文：<https://hackaday.com/2016/12/01/running-intel-tbb-on-a-raspberry-pi/>

Raspberry Pis 的用途似乎是无限的，每天都有新的应用程序推出，而且看不到尽头。但是，尽管它们功能多样，树莓派仍然缺乏纯粹的处理能力，这已经不是什么秘密了。因此，当您在处理处理器密集型项目时，需要进行一些认真的优化，以尽可能多地利用 Raspberry Pi。

当然，完成这种优化的最简单的方法就是简单地将运行的内容减少到最基本的部分。例如，如果你的项目甚至不使用显示器，那么运行 GUI 就没有意义。然而，另一个策略是确保您实际上使用了 Raspberry Pi 提供的所有可用处理能力。在[sagiz]的案例中，这意味着使用英特尔的开源线程构建模块在他的 OpenCV 项目中实现更好的并行性。

正如您可能猜到的，这并不像在终端中键入“apt-get install tbb”那么简单。这是因为英特尔 TBB 在 Raspbian 中不可用，因为很难创建一个在 ARM 上运行的版本。但是，[sagiz]能够创建一个工作版本，并在他的项目页面上提供。使用他的新构建，他能够将 OpenCV 速度提高 30%，这绝对是一个不小的数目！

 [https://www.youtube.com/embed/IjLl_FgbPxk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IjLl_FgbPxk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你想在 Raspberry Pi 上开始使用 OpenCV，一定要[看看这个指南](http://hackaday.com/2013/03/04/using-opencv-with-the-raspberry-pi/)。这会让你有一个好的开始。