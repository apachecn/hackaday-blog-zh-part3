# 美国宇航局知道流星在哪里

> 原文：<https://hackaday.com/2016/10/08/nasa-knows-where-the-meteors-are/>

美国宇航局一直在使用一个指向上方的分布式摄像机网络来跟踪明亮的流星体(“火球”)。虽然我们通常认为美国宇航局是价值数十亿美元的火箭飞船，但这次行动显然是有限的。这是一个名副其实的黑客。

[![droppedimage](img/7415aad3e6b72ee0c810622d308eb2a1.png)](https://hackaday.com/wp-content/uploads/2016/10/droppedimage.png)

基本的想法是，通过许多广角摄像机捕捉夜空，并进行一点点图像处理，识别夜空中的流星体应该是相当容易的。当足够多的相机捕捉到相同的流星体时，人们可以使用三角测量法在 3D 中反演流星体的[路径，估计其质量，等等。令人惊讶的是，在任何一个特定的夜晚](http://fireballs.ndc.nasa.gov/evcorr/20161005/20161004_004159A/event.png)，在[都能看到这么多。](http://fireballs.ndc.nasa.gov/20161005.html)

你可以从任何相机观看流星体事件的视频，观看相机直播，甚至下载流星体的轨道参数。我们正在为下一场大流星雨给这个网站做书签。

这部作品显然是基于[Rob Weryk]的 ASGARD 系统，不幸的是，该系统的代码无法获得。但是，用一台单板计算机、摄像机和 [OpenCV](http://opencv.org/) 一起破解一些东西应该不是很难。到目前为止，美国宇航局的项目仅限于美国，但我们想知道通过遍布全球的相机网络可以收集多少数据。那么你们中谁将接受我们的挑战？打造你自己的版本[让我们知道吧](http://hackaday.com/submit-a-tip/)！

在这个项目和[无线电流星动物园](http://hackaday.com/2016/08/30/citizen-scientist-radio-astronomy-and-more-no-hardware-required/)之间，我们惊讶于有这么多关于每晚落在我们身上的岩石火球的公开信息，这些火球最终将导致我们的灭绝。至少我们可以确定我们会把它拍下来。