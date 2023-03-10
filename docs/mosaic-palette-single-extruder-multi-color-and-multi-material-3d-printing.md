# 马赛克调色板:单挤出机多色多材料 3D 打印

> 原文：<https://hackaday.com/2016/06/20/mosaic-palette-single-extruder-multi-color-and-multi-material-3d-printing/>

对于多色和多材料的 3D 打印，已经提出并实施了许多解决方案，从喷嘴中的颜色混合到需要手动更换细丝的脚本。早期提出的一个解决方案是手动将灯丝拼接在一起，制作一个定制的线轴。打印机将正常打印，但灯丝会变色。这工作得相当好，但是它是乏味的，并且它不是完全可能控制在模型上颜色变化发生的地方。

你会在下面的图片中找到一些更成功的手工拼接技巧的例子。向下滚动一点，找到我们在 2016 年湾区创客大会上对 [Mosaic Manufacturing](http://www.mosaicmanufacturing.com/) 的采访。他们有一种新产品，以精确为最终目标，使细丝拼接过程自动化。它解锁单挤出机打印机，使其像多挤出机模型一样运行，无需停止和启动。

 [![Terminus's Ultrasonic Splicer http://www.thingiverse.com/thing:297380](img/6ab6f31fe0ce1ad2279c2b1f97590ce1.png "setup2_display_large")](https://hackaday.com/2016/06/20/mosaic-palette-single-extruder-multi-color-and-multi-material-3d-printing/setup2_display_large/) Terminus’s Ultrasonic Splicer [http://www.thingiverse.com/thing:297380](http://www.thingiverse.com/thing:297380) [![Malcom's Handheld Splicer http://www.thingiverse.com/thing:16258](img/106e35aae2a7b7878c3972538873d524.png "SplicerMK2upcloseopen_display_large_display_large")](https://hackaday.com/2016/06/20/mosaic-palette-single-extruder-multi-color-and-multi-material-3d-printing/splicermk2upcloseopen_display_large_display_large/) Malcom’s Handheld Splicer [http://www.thingiverse.com/thing:16258](http://www.thingiverse.com/thing:16258) [![RichRap's Filament Joiner http://www.thingiverse.com/thing:297380](img/24ae48123b2a141491babf8c7770a0a8.png "Filament_joiner_display_large_display_large")](https://hackaday.com/2016/06/20/mosaic-palette-single-extruder-multi-color-and-multi-material-3d-printing/filament_joiner_display_large_display_large/) RichRap’s Filament Joiner [http://www.thingiverse.com/thing:297380](http://www.thingiverse.com/thing:297380)

Mosaic 完成了上述两种方法的非常困难的组合。他们的旗舰产品是一台他们称之为“调色板”的机器。这是自动接丝机。多达四个不同的细丝可以进入调色板，它将拼接他们在确定的间隔。这本身就很酷，如果只是为了省去手工拼接和缠绕定制线轴的繁琐。

然而，Palette 真正的杀手锏是与它一起运行的软件。调色板可以从任何切片器获取任何正确准备的多材质文件的 GCODE 输出，然后精确地组合和拼接灯丝。除了在细丝路径的某个地方粘贴一个编码器之外，这可以在不修改它的情况下馈入任何打印机。结果与双挤出机或四挤出机的设置没有区别。

 [https://www.youtube.com/embed/KlJQBmv9a0I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KlJQBmv9a0I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![Kill me... it whispers. Free me from this torment.](img/a52e107c3b299db23dd3762d7bfdef51.png)](https://hackaday.com/wp-content/uploads/2016/06/47.jpg)

“Kill me…” it whispers, “free me from this torment.”

现在，这并没有真正降低多挤出机装置的复杂性。事实上，有人会说在某些方面它更复杂。话说回来，人们只需要看看令人厌恶的 ORD Solutions 5 挤出机 3D 打印机，就可以看到，如果不是光，至少是温和的光芒。

如果我们对这两种解决方案做一个快速的比较，我们可以看到两者的一些优点和缺点。Mosiac 最大的缺点是材料的性能必须相当接近。例如，将聚碳酸酯和 Ninjaflex 拼接在一起可能行不通。多挤出机装置允许长丝之间有更多的变化，以及完全不同的挤出机装置。例如，完全有可能用一个 0.4 毫米的喷嘴来打印物体的主体，然后用另一个 0.2 毫米喷嘴的挤压机在印刷品上打印出精细的文本。

最大的优势是与打印机的现有挤出机设置的集成。考虑一台 delta 打印机。为了很好地印刷，它通常需要用于可能最轻的挤出机组件的鲍登装置。在一个三角形的末端增加五个喷嘴会产生可怕的结果。它会震动，发出可怕的响声，最终在这个过程中自我毁灭。马赛克只是简单地坐在挤出机冷端的前面，长丝通常在这里进入，并做它的事情。这也适用于普通打印机，挤压机越轻越好。

对于大多数用户来说，调色板将满足他们的需求。他们可以将它添加到店里的任何打印机上，进行颜色和材料混合。正如 Mosaic 在这个视频中显示的那样，由于 PLA 中充满了几乎所有的纤维和灰尘，制造商现在可以在 PLA 外壳中制作导电路径。

 [https://www.youtube.com/embed/buGUIb1SF6A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/buGUIb1SF6A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



让调色板正常工作是一个相当大的挑战。制造自动拼接器是一个挑战。任何 3D 打印过的人都知道挑剔的打印机是如何处理直径稍大的细丝的。机械调色板是相当复杂的。它可以吸入多达四种不同的细丝，对它们进行测量，然后精确拼接。然后，它将新制成的灯丝输送到打印机。

[![The Pallet is quite a complicated assembly with a complex filament path.](img/1e0e8922df9d56cb0a29bc27fae4400e.png)](https://hackaday.com/2016/06/20/mosaic-palette-single-extruder-multi-color-and-multi-material-3d-printing/img_0762/)

The Palette is quite a complicated assembly with a complex filament path.

[![The splicing mechanism stays lifted up until ready to perform a splice.](img/bf7fafe801d62b958dabce9f1e3ec907.png)](https://hackaday.com/2016/06/20/mosaic-palette-single-extruder-multi-color-and-multi-material-3d-printing/img_0755-2/)

The splicing mechanism stays lifted up until ready to perform a splice.

[![The mechanism performs a splice.](img/5af82c0696e7dca711e85a6b9a235b24.png)](https://hackaday.com/2016/06/20/mosaic-palette-single-extruder-multi-color-and-multi-material-3d-printing/img_0752/)

The mechanism performs a splice.

他们很快发现，即使细丝拼接正确，但打印出来的效果却不一致。结果是，大多数打印机挤出的细丝数量与它们声称的数量不同。很难让打印机完全校准，所以它只能挤出[预期量的灯丝](http://hackaday.com/2016/01/27/3d-printer-tool-set-your-extruder-steps-with-ease/)。他们的解决方案是“滚轮”如前所述，这只是一个旋转编码器，位于马赛克的出口端，尽可能靠近打印机的挤出机。Mosaic 根据打印机的运行情况使用它来校准拼接点。

[![Pallet getting certified.](img/61bb2718a8f9d154952c29636f49ffec.png)](https://hackaday.com/wp-content/uploads/2016/06/certupdate1pic3.png)

Palette getting certified.

至于之前提到的软件栈，Mosaic 已经决定开源了。他们有自己要迎合的核心人群，但人们不断想出该工具的酷用法，只要他们能破解它的固件。于是，马赛克做了每个公司[该做的事情](http://hackaday.com/2016/03/21/ask-hackaday-mrrf-edition-3d-printers-can-catch-fire/)，让他们黑。

Mosaic 已经成功启动了他们的产品，他们甚至已经发运了第一批承诺的产品。如果你想要一个，他们正在接受 Kickstarter 后单元的预购。要了解更多信息，我们强烈推荐[阅读他们的博客](http://www.mosaicmanufacturing.com/blogs/news)，它记录了他们从设计到制造的整个过程。这是一本很好的读物，甚至还涉及了消费制造中不太为人所知的方面，比如让你的产品获得 T4 认证。这是一个很酷的产品，它的完美程度显示了这个行业变得多么真实。