# 一键键盘是在亚毫米设计中锻炼出来的

> 原文：<https://hackaday.com/2018/05/19/one-key-keyboard-is-exercise-in-sub-millimeter-design/>

正如[Glen]所描述的，他决定设计[单键 USB 键盘](http://bikerglen.com/blog/presenting-the-single-esc-key-usb-keyboard/)的唯一真正目标是看看他可以使用 Cherry MX 按键开关构建多小的功能键盘，并且每一毫米的分数都被计算在内。制作一个单键 USB 键盘是一回事，但从头开始制作一个易于组装的合身外壳需要精心设计，幸运的是，[Glen]已经很好地记录了这一点。(顺便提一下，Cherry MX 交换机有多种质量和功能，不同的型号通过它们的颜色来识别。[Glen]正在使用一种樱桃 MX 蓝，这种蓝色在键盘中很常见，因为它有触感和可听见的咔嗒声。)

[![](img/8e135428897be1e427c1ea6aaf6f83a2.png)](https://hackaday.com/wp-content/uploads/2018/05/one-key-keyboard-square.jpg) 【格伦】一步一步地讲述制造一台似乎每个细节都很重要的设备的设计挑战，并从头到尾解释问题和解决方案。实现 USB 2.0 只需要一个 PIC16F1459、一个 USB micro-B 连接器和三个电容器，但还添加了一些其他组件，包括 LED，以帮助事情向前发展。外壳需要格外小心，因为不仅需要安装电路板和安装的元件，还需要考虑其他设计因素，如螺钉埋头孔的深度和角度、USB 连接器周围的安装深度和间隙，并考虑 USB 电缆本身的包覆成型高度，以便小型设备实际上位于外壳上，而不是电缆成型的任何部分。最重要的是，还必须遵守外壳本身的最小特征尺寸和壁厚的一些设计规则，外壳是用尼龙打印的 SLS 3D。

PCB、外壳、软件和材料清单(针对单键和三键版本的键盘)都有文档记录，可在项目的 [GitHub 资源库](https://github.com/bikerglen/small-keyboards)中获得。[Glen]还强调了使用光导管将嵌入式 LED 重定向到外壳上其他地方的可能性；这让人想起了他在[使用 3D 打印制作定制 LED 条形图的早期作品](https://hackaday.com/2017/05/16/3d-printing-custom-led-bar-graphs/)。