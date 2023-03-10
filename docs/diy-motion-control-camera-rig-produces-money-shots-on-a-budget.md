# DIY 运动控制相机钻机生产金钱拍摄的预算

> 原文：<https://hackaday.com/2016/07/18/diy-motion-control-camera-rig-produces-money-shots-on-a-budget/>

动作控制摄影可以拍摄出令人惊叹的图像，尽管商用机器人 *MoCo* 钻机很难负担得起。但是钱是什么呢？从曾经的机电垃圾和一个被黑掉的佳能 EF-S 镜头白手起家，【霍华德的】 [DIY 运动控制相机装备制作出了让我们震惊的电影镜头](http://howiem.com/wordpress/index.php/2016/07/14/hs-homemade-motion-control/)。

[![moco_movinghead](img/4a1f6b0ad4fa46686f9df1c744ec81d9.png)](https://hackaday.com/wp-content/uploads/2016/07/moco_movinghead.png) 【霍华德】大约一年前开始这个项目，进行一些有针对性的实验。这些不仅会评估他从各个方向收集的组件的适用性，还会评估他自己收集足够的机电一体化知识以使整个事情工作的能力。在习惯了步进电机、Teensies 和 Arduinos 之后，他将一个旧的摇头迪斯科灯改造成了摄像机的云台。增加了一个线性轴，随着自由度的增加，需要更复杂的控制手段。

使用 Swift 编程语言，[Howard]编写了一个[主机程序](https://github.com/howiemnet/MotionControl)，它可以自动检测众多基于步进电机和伺服电机的轴，并将位置数据传输到各自的基于 LC 的控制器。对于[专业动画艺术家](http://push-pictures.com/)来说，这些镜头不仅仅是漂亮而稳定的镜头:当他开始添加完全匹配的 CGI 层时，真正的魔法发生了。因此，他还编写了一些 Python 脚本，允许他从 Blender 中的虚拟装备手动控制他的 MoCo 装备，还可以直接从他的 3D 场景中导出相机轨迹。

 [![moco_setup](img/d8f518fd8038064af2beffc757c0582a.png "moco_setup")](https://hackaday.com/2016/07/18/diy-motion-control-camera-rig-produces-money-shots-on-a-budget/moco_setup/)  [![moco_blender_2](img/986c1a62ffb7603a17797b74fe8bb0dc.png "moco_blender_2")](https://hackaday.com/2016/07/18/diy-motion-control-camera-rig-produces-money-shots-on-a-budget/moco_blender_2/)  [![moco_lens](img/67bf25e95305fc380a9dc057ac3cd56a.png "moco_lens")](https://hackaday.com/2016/07/18/diy-motion-control-camera-rig-produces-money-shots-on-a-budget/moco_lens/) 

除了 4 轴相机支架和旋转平台之外，[Howard]还需要找到一个[电子跟随对焦机制](http://howiem.com/wordpress/index.php/2016/07/07/motion-control-canon-ef-lens-hacking/)来保持现在移动的物体在焦点上。由于佳能 EF-S 协议[已经被逆向工程](https://pickandplace.wordpress.com/2011/10/05/canon-ef-s-protocol-and-electronic-follow-focus/)，他决定接入相机和镜头之间的 SPI 控制总线，以利用其内部的环形电机。虽然自动对焦镜头中的压电/超声波马达实际上不是为绝对定位而制造的，但一系列测试表明，佳能 EF-S 17-55mm IS USM 镜头可以重新对焦几百次，仍然可以回到足够接近的起始位置。警告:[霍华德]不得不打开 600 镜头并在上面钻孔。他告诉我们，回想起来，他的妻子在项目进行期间没有离开他是一个奇迹。

经过几次反复的机械改进，运动控制装备现在已经完成，并且第一个剪辑已经被录制和编辑。它们太棒了。只有藏在(霍华德的)地下室里的 [6 轴机械臂](https://www.youtube.com/watch?v=5w25CeFTkQ0)告诉我们，他只是在为真正的比赛热身。欣赏下面的视频，但不要错过关于这个项目如何产生的完整的三集视频纪录片[。](http://howiem.com/wordpress/index.php/2016/07/14/hs-homemade-motion-control/)

 [https://www.youtube.com/embed/rWuKmWKicro?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rWuKmWKicro?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

