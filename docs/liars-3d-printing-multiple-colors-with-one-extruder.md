# 骗子的 3D 打印:一台挤出机多种颜色

> 原文：<https://hackaday.com/2016/12/27/liars-3d-printing-multiple-colors-with-one-extruder/>

好的 3D 打印机现在有多个热端。你应该能够打印不同的颜色或打印支持材料。然而，我们很多人都没有多重热点。原来，你不必有多个热点结束打印多种颜色。要做到这一点，你需要很大的耐心，并愿意说出露骨的谎言。不过，别担心，你只是对一些计算机硬件和软件撒谎，所以那不算。

你可能已经看到人们谈论在层之间放置一个停顿来从一种颜色切换到另一种颜色。这是可行的，但它限制了你的选择。例如，如果你想把一些彩色文本放在不同颜色的背景上，你要么让文本突出来，要么让它在背景的“下面”。如果只有一台挤出机和热端，就不能齐平。我的方法麻烦多了，但能产生好的结果。

请记住，对于业余爱好级别的打印机，即使您有多台挤出机，多色打印也会有很多问题。这不是万灵药。但是你可以用一台类似的有多个打印头的打印机得到相同的结果。

## 底线在前面

这里有几张使用这种技术的测试照片。一台带有原料挤出机和热端的 [Monoprice Mini printer](https://hackaday.com/2016/06/13/review-monoprice-mp-select-mini-3d-printer/) 使用不同的 PLA 长丝制造它们。左边是一个测试立方体，在层的中间有一个色点(还有一些你看不到的顶面上的点)。右边是一块牌子，上面用对比色写着我的呼号。当然，在图片中很难分辨，但是有一个表面。文本与黄色表面的高度相同。

 [![dot](img/10e1078701975732f8af89b9470b8d0f.png "dot")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/12/dot.png?ssl=1)  [![wd5gnrsm](img/46ad47f84ba59d4f00ecabccbf1e692a.png "wd5gnrsm")](https://i0.wp.com/hackaday.com/wp-content/uploads/2016/12/wd5gnrsm.png?ssl=1) 

我没有花太多时间制作这些印刷品，因为我更专注于完善方法。图层高度不是很精细，填充稀疏，打印速度很快。然而，你可以花时间制作更好看的照片。你也可以使用你在“真正的”多重挤压打印机上使用的常用技术(如底漆塔、软泥护板等)。).

## 这个概念

正如我提到的，在两层之间停止打印机并在那一点关掉灯丝是过时的做法。通常，你会手动编辑你的 g 代码或者使用[一个简单的应用程序](http://prusaprinters.org/color-print/)或者[插件](https://github.com/smorloc/CuraPlugins/blob/master/ChangeFilamentAtZ.py)。我们甚至看到有人[只是计时](https://www.google.com/search?q=prusa+multicolor&oq=prusa+multicolor&aqs=chrome..69i57j0.3791j0j7&sourceid=chrome&ie=UTF-8#q=print+multiple+colors+one+extruder)。我想要一种不同的方法，不要把我限制在每层一种颜色。

诀窍就是撒谎。任何支持多重挤压的切片软件都有一种方法让你告诉它你有多少个挤压机。我用的是 Slic3r 和 Repetier 主机。在 Slic3er 的打印机设置中，有一个关于功能/挤压机的条目。我简单地告诉它，我有三台挤出机(你可以告诉它或多或少，但三似乎是一个很好的数字；以后随时可以改)。然后我在 Repetier 的打印机设置中做了同样的改变。如果你真的有多个头，你需要告诉程序它们相距多远以及其他细节。但是因为我们的只是假设，我们可以把偏移量设置为零，不需要包含任何其他信息。

当然，这并不是你需要做的全部。我还添加了自定义 g 代码设置，也在 Slic3r 的打印机设置下。特别是，我添加了这段定制代码用于工具更改:

```
M83 ; turn on relative movement for extruder 
G1 E-5.000000 F6000 ; retract filament 5mm 
G1 X0.000000 Y0.000000 F9000 ; home X and Y axis leave Z at current height 
G91 ; note: For Marlin this make E and XYZ relative; for some it just makes XYZ
G1 Z10.0 ; obviously, this limits your print height by this amount!
; Note Marlin treats relative different from others

M84 E ; release extruder stepper motor from 'holding' position 
@pause Change Filament for [next_extruder] and set [temperature_[next_extruder]] degrees ; pause print!
G90  ; back to absolute
G1 X0.000000 Y0.000000 F9000 ; upon resume, rehome X/Y in case position was bumped out 
G91  ; bring Z back
G1 Z-10.0
G90  ; and back to absolute
G1 E0 F6000 ; reset extruder, ready to push out plastic again 
G1 F9000 
M82 ; set extruder movement back to absolute ready for next layer
```

您可能想稍微改变一下这段代码，当然，您可以省略注释(分号和它们后面的所有内容)。基本思想是将细丝向上拉以减少渗出，移动到位置 0，0，然后使用@pause 使 Repetier 停止并提示。你现在可以换灯丝了。如果你想的话，你大概可以改变温度(我不需要)。如果你想得到干净的颜色，你必须清洗喷嘴(也就是说，运行挤出机，直到新的颜色出现)。如果你想要艺术淡色，你可以跳过这一步——完全由你决定。

当您退出暂停时，脚本将一切恢复原样，g 代码继续打印。当 g 代码试图切换挤压机时，你会得到一些“坏挤压机”的错误，但是——至少在我的机器上——它不会伤害任何东西。

顺便说一下，尝试移动所有相对的东西，以便脚本可以将头部放回正确的位置，这很有诱惑力。然而，我的打印机不支持越界，所以这并不实际。另一方面，Slic3r 假设您可能已经移动了东西，所以在刀具更换之后，它做的第一件事是移动回已知位置。然而，如果在 XY 平面上的旧位置上对齐，然后将 Z 轴下移，那就更好了。事实上，如果你有一点太多的挤压，你可以拖动你的打印头。然而，如果你的图层高度是准确的，你不应该有这个问题。

## 价格

没有免费的午餐。切片软件最大限度地减少了工具的变化，但你仍然厌倦了拉细丝进出。用两种颜色打印一个 400 层的章鱼，大概已经超出了大家的忍耐水平。你真的希望尽可能多的层是纯色，只是为了节省你手上的磨损和你的耐心。

您还需要计划您的模型，以便每种颜色都有足够的体积来展示。即使是多头机器也是如此。例如，在呼号牌上，如果呼号是一层紫色，在我通常用于打印的 80 到 100 微米的波长下，它不会很好地显示出来。同样，将浅色放在深色上需要更多的体积。大的东西你会有更好的结果。你可能不会把呼号降低到 4 点的文本大小。同样，这是真的，即使你有相同的喷嘴和层大小的多台挤出机。

## 制作模型

有几种方法可以表示多色模型。最常见的是简单地为每台挤压机创建一个单独的 STL 文件。即使我只有一台挤压机，为了让我的生活过得更好，我也需要单独的 STL 文件。

下一次我将向你展示我如何创建这些模型，以及如何将它们(或任何多挤出机 STL 文件)加载到 Repetier 主机中。工作量很大。但是，如果它能使完成工作和不得不把它送出去有所区别，也许它是值得的。同时，如果你想试验，你可以下载 STL 和源文件。