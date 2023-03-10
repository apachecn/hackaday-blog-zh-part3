# 在 Hackaday 上开发:HaDge 更新-这是一个黑客

> 原文：<https://hackaday.com/2016/01/19/developed-on-hackaday-hadge-update-its-a-hack/>

关于 Hackaday con 徽章的工作仍在断断续续地进行，最近几周我们取得了一些良好的进展。HaDge 将是一个在所有会议上使用的会议徽章，能够在徽章之间进行通信。

从上次的[开始，我们同意以 Atmel D21 为基础，这是一款 32 位 ARM Cortex M0+处理器。为了获得一些原型板来帮助软件开发，我们决定在处理 HaDge 之前完成设计](http://hackaday.com/2015/10/30/developed-on-hackaday-hadge-is-back-to-the-drawing-board/) [HACK](https://hackaday.io/project/8007-hack) 。HACK 是[Michele Perla]发起的一个项目，我们已经吸收了它作为 HaDge 的原型平台。我们想要一个紧凑的微控制器板，因此选择了 SAM D21E——一个带 26 个 IO 的 32 引脚封装。

[Michele Perla]在更大的 32 针 SAM D21G 的基础上设计了 HACK，并使用 Eagle 绘制了原理图和布局。使用 [Eagle to KiCad](http://hackaday.com/2015/12/27/eagle-to-kicad-made-easy/) 脚本，他很快转换了项目并开始制作电路板布局。我接手后卫队，并致力于使他的[示意图](https://github.com/MickMad/HACK/blob/master/kicad/pdf/hack.pdf) (pdf)“漂亮”，并建立一个示意符号库。当[Michele]完成电路板布局时，我在为我们将使用的各种足迹收集 STEP 模型，其中大部分我可以通过[3dcontentcentral.com](http://www.3dcontentcentral.com/)获得。少数我做不到的是用 FreeCAD 从零开始做的。使用 FreeCAD 将 STEP 模型转换为 VRML。使用[Maurice]的 [KiCad Stepup 脚本](http://hackaday.com/2015/11/08/kicad-script-hack-for-better-mechanical-cad-export/)，我们能够获得 HACK 板的完整 STEP 模型。

HACK 现在已经准备好进行电路板制造和组装。我们计划制作大约 20 块电路板，分发给开发人员，用于开发软件。GitHub 存储库中有所有最新的文件，包括 KiCad 源文件、pdf、gerbers、数据表和图像。该板将与试验板兼容，并具有城堡状焊盘，以便作为模块直接焊接。如果您想参与 HaDge 的软件或硬件开发，请在 HACK 项目页面上通过群发消息通知我们。

在即将发布的帖子中，我们会提出一些想法，说明既然黑客攻击已经完成，我们打算如何推进 HaDge。敬请关注。