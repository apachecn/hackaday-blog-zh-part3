# 可口可乐新的 3D 时代广场标志唤起了创意

> 原文：<https://hackaday.com/2017/09/02/coca-colas-new-3d-times-square-sign-invokes-inceptionism/>

可口可乐公司更新了他们在时代广场的标志，这个标志[有一个迷人的 3D 外观](http://www.coca-colacompany.com/stories/coca-cola-celebrates-with-fans-in-times-square-to-introduce-the-)，给人一种在电影《盗梦空间》中看到建筑物卷曲到天空的怪异感觉。这种 3D 效果是通过将标牌分割成一个由 1760 个 LED 屏幕组成的 68 * 42 *的矩阵来实现的，这些 LED 屏幕可以独立地向观众伸出，又可以收回。当然，我们去寻找实现细节。

![Moving Cube Module](img/9bec68594a7edae4e0a828dea834f2a9.png)

Moving Cube Module

在[可口可乐的网页上列出了参与整合的合作伙伴](http://www.coca-colacompany.com/stories/innovation/2017/coca-cola-times-square-sign-partner-credits),[Radius Displays](http://www.radiusdisplays.asia/radius-displays-partners-coca-cola-unveil-iconic-billboard-times-square/)被列为负责标志设计、制作、测试和安装支持。梳理他们的网站是第一步。遗憾的是，我们在那里没有找到详细的设计文档或幕后视频。我们确实找到了一张带有 28×28 led 矩阵的移动立方体模块的 CAD 图纸。假设这是准确的，那么总共有 1，379，840 个 led——试着从易贝订购这么多。编辑:一个正在测试的模块的幕后视频被发现并添加到下面。

所以接下来是专利搜索，这就是我们中头彩的地方。请继续阅读，查看结果并观看下面的登录视频。

搜索发现了可口可乐的三项相关专利，最近的一项是[美国 9，640，118 B2，显示设备](https://worldwide.espacenet.com/publicationDetails/originalDocument?CC=US&NR=2016133203A1&KC=A1&FT=D&ND=4&date=20160512&DB=&locale=en_EP)，于 2016 年 1 月提交，但于 2017 年 5 月公布。很明显他们已经研究了一段时间了。我们给出的链接是指向欧洲 Espacenet 专利网站的，因为谷歌似乎没有这些图纸。

 [![Actuator assembly - Fig. 10 from US2016133203](img/31505722ebbe33a53bda608d64c08af0.png "Actuator assembly - Fig. 10 from US2016133203")](https://hackaday.com/2017/09/02/coca-colas-new-3d-times-square-sign-invokes-inceptionism/actuator_assembly_fig_10_us2016133203/) Actuator assembly – Fig. 10 [![Communication - Fig. 13 from US2016133203](img/0843e8c7d51cded439e4772567442853.png "Communication - Fig. 13 from US2016133203")](https://hackaday.com/2017/09/02/coca-colas-new-3d-times-square-sign-invokes-inceptionism/communication_fig_13_us2016133203/) Communication – Fig. 13

可口可乐的这项专利读起来像是时代广场标志的详细概述。它有 35 个图形，包括与我们在 Radius Display 网站的 CAD 绘图中看到的相同的致动器组件。这项专利涵盖了从硬件到软件的所有领域，处理缩放问题，甚至内容创建程序。

这里有一些专利中提到的显著特征，尽管我们不能保证它们真的出现了。致动器组件被分成模块，例如，模块可以由 5 排 5 个组件组成。这是为了使安装更有效，并更好地处理由于天气造成的压力。还有一个物理锁定机制，以防止执行器在极端风力的情况下移动。每个组件的显示和移动都是以同步的方式完成的，据说这样可以确保在移动到下一个组件之前，生成的图像是连贯的。正如专利的图 13 所示，这里有一个高水平的并行用于管理所有的执行器和屏幕。在图中，以太网被用作通信协议，但在专利中给出了更多选项。这只是专利中的一小部分。它实际上是一本很好的读物。

虽然可口可乐的广告视频显示了它的许多观点，但我们在下面包含了 Radius Displays 的第二个视频，它更侧重于标志，我们认为更好地展示了它。

这个 3D 标志应该让黑客读者想起我们之前报道过的麻省理工学院的变形表。他们的视频不再工作，但你可以在麻省理工学院的页面[找到一个不同的视频。](http://tangible.media.mit.edu/project/inform/)

可口可乐的视频:

 [https://www.youtube.com/embed/geMEB8zJLiU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/geMEB8zJLiU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Radius 显示器的视频:

[https://player.vimeo.com/video/229196000](https://player.vimeo.com/video/229196000)

编辑:运动测试模块的视频。视频是由提供扁平电缆的 Cicoil 公司制作的。(感谢 JH 和 jason701802 在评论中指出这一点。)

 [https://www.youtube.com/embed/1DaCrQIdhsk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1DaCrQIdhsk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

