# 用激光和投影仪做的有趣的事情

> 原文：<https://hackaday.com/2016/05/02/curiously-delightful-things-done-with-lasers-and-projectors/>

Seb Lee-Delisle[围绕大型装置](http://seb.ly/)建立了自己的事业，这些装置利用强大的激光和高端项目让人们快乐。这是一份梦寐以求的工作，通过他的多学科技能组合、他的魅力能量以及驱使他看看如何通过现场互动来拓展可能性的思维方式，这份工作结出了硕果。

他在贝尔格莱德会议上的讲话是关于他的激光合成器项目的，但是我们很高兴他也谈到了他建造的一些其他装置。synth 本身涉及一些非常有趣的迭代设计，最终得到一个由可寻址 led 点亮的电容式触摸音频键盘。它控制一个投射形状和图像的激光来跟随音乐，由于一些非常有创意的编码，无论谁在键盘前听起来都很棒。随着谈话的展开，我们还听说了他的 PixelPyros，这实际上是一场人群控制的激光焰火表演。

请看下面他的演讲，休息后加入我们，了解更多细节。

 [https://www.youtube.com/embed/3gYJIEdqfQ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3gYJIEdqfQ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![PixelPyros by Seb Lee-Delisle](img/45e169373559d0cb1b76c2b8e6b969fc.png)](http://seb.ly/work/pixelpyros/) 如果你还没听说过[pixelpros](http://seb.ly/work/pixelpyros/)，那你可要吃一顿了。巨大的投影数字烟花本身就很酷，但如果观众控制了表演，那就有趣多了。然后，当你添加一个 11 瓦的激光器时，它开始变得增压。激光比投影仪更生动，两者的结合远远超过其部分的总和。当烟花燃放时，红外摄像机从后面观察屏幕，检测观众触摸屏幕的情况。由于 Seb 的软件，当烟花击中屏幕时，烟花会实时发射。

在这一点上，他认为自己沉迷于使用高能激光。他在 2014 年轰动的会议灯光秀上的工作令人叹为观止。该活动在~~一座大教堂~~牛津市政厅举行，Seb 混合激光的强度以突破屏幕并利用整个空间。风琴管上的 VU 计和从顶部射出的粒子非常壮观！

所有这些都只是他讨论[激光合成器](http://seb.ly/laser-light-synths/)项目的序言！完工后的项目被安装在一个以巨大的石柱为特色的建筑里。在每根柱子的底部周围是用户控制器，它们影响音乐和激光表演，激光表演在柱子上绘制可视化效果。虽然除了最接近的观众之外，其他人可能很难看到键盘，但所有人都可以看到这些列。

[![seb-lee-delisle-laser-light-synth-keyboard-prototype](img/bd2fa29c027b734a3110f50500e96574.png)](https://hackaday.com/wp-content/uploads/2016/05/seb-lee-delisle-laser-light-synth-keyboard-prototype.png) 控制器的硬件构建是一个伟大的故事。你在帖子顶部看到的是成品。每个键都装有 RGB LEDS。Seb 的诀窍是找到一种方法，将所有这些 led 与不会遮挡光线的电容式触摸控制器结合起来。

他从一大块铜开始，只是为了确保这个概念可行。然后，他用粘性铜带、导电涂料做实验，最后决定用乙烯切割器在铜箔上切割出波浪形图案。它用转移胶带粘在键盘的丙烯酸面板上。该图案不会阻挡 led，并通过巧妙使用焊接的铜引脚和铜亮片连接到电路板，以实现牢固的连接。

键盘很棒，但 Seb 还远远没有完成。他真的用一些惊人的代码让这个项目变得生动起来，让每个人都成为爵士音乐家。这是以定制的 Ableton Live 补丁的形式出现的，他用观众中的一名志愿者为我们演示了这个补丁。他们利用五声音阶来确保音高与音乐中已经发生的事情相匹配。节奏和音高一样重要，所以他还编写了定制的补丁，让音高随着节拍自动琶音，并随着节目的播放增加节奏。你得看着 Dex，这个没有音乐经验的志愿者，摇滚起来。

Seb 证明了艺术家的技能是没有界限的。不仅能看到他的最终产品，还能让他分享他是如何通过概念、原型、电子设备、外壳和软件实现最终产品的，这真是太棒了。他的演讲是一个很好的例子，说明了为什么你应该在过程的每一步记录你的构建。观众们狼吞虎咽地接受了他的介绍，你也会的！

【激光合成器控制器主图由 [Oleg Pulemjotov](http://www.ooohleg.com/) 拍摄】