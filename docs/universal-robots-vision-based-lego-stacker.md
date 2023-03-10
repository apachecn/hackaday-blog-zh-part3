# 基于视觉的通用机器人乐高积木

> 原文：<https://hackaday.com/2017/06/11/universal-robots-vision-based-lego-stacker/>

奥尔堡大学机器人视觉课程的托马斯·克尔贝克·叶斯柏森和他的同学使用 MATLAB 代码和 URscript 编写了一个通用机器人 UR5 来[堆叠 Duplo 砖块](http://blog.tkjelectronics.dk/2017/06/universal-robots-vision-based-lego-duplo-stacker/)。Duplo 砖块被堆砌成低保真度的《辛普森一家》角色——例如，黄色代表荷马的头部，白色代表他的衬衫，蓝色代表他的裤子。

砖块随机散落在附近的桌子上，而安装在桌子上方的摄像机扫描砖块，并帮助确定元素的位置、颜色和方向。这涉及到斑点分析，帮助计算机决定哪些像素是砖块的一部分，哪些不是。在运行了 4 连通递归 grassfire 算法后，计算机给每个像素一个数字，并将其分配给一个 blob。

为了确定方向(假定砖块都是正面朝上且不重叠)，斑点被分成象限，并且在每个象限内，测量斑点的中心与其最远像素之间的距离。这种技术不太可能对不是正方形的砖块起作用。每块砖的像素位置都被转换成笛卡尔坐标，这使得机器人可以轻松地捡起它。 [MATLAB 和 URscript 代码](https://github.com/mindThomas/URRobot-LEGOstacker)见【Thomas】的 GitHub。

寻找更多 UR5 项目？看看我们去年发布的 Sewbo 制衣机器人。

 [https://www.youtube.com/embed/fLyhVfCzkio?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fLyhVfCzkio?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

