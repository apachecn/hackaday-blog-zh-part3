# 外星人的电子学

> 原文：<https://hackaday.com/2015/10/06/electronics-for-aliens/>

我们被拥有“数百万”色彩和每英寸数百像素的显示器所包围。超“高保真”的声音产生我们认为是真实世界的逼真复制品。

当然事实并非如此，我们很少停下来思考我们的电子系统是如何围绕人类感知的局限性而被制造出来的。因此，为了探索这个问题，在这篇文章中，我们提出了这样一个问题:“外星人会如何看待人类科技？”。我们将假设一种生命形式，它能像我们一样感知周围的世界。但是已经大大提高了感知能力。鉴于这些能力，我们称它为 Oculako。

让我们从现在已经废弃的 CRT 显示器开始，看看我们假设的外星人是如何看待它的。下面的视频显示了一个每秒 10，000 帧的电视屏幕。

 [https://www.youtube.com/embed/lRidfW_l4vs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lRidfW_l4vs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们有限的视觉系统察觉变化[缓慢](http://vision.arc.nasa.gov/personnel/pavel/publications/TemporalSensitivity.pdf) (PDF)。人类[视觉暂留](https://en.wikipedia.org/wiki/Persistence_of_vision)以大约每秒 15 帧的速度生效。这将线条合并在一起，创建一个单一的图像。Oculako 处理图像的速度要快得多。所以看到屏幕上好像有一条线在跑。这种生物可能甚至不认为这是一种展示。

即使 Oculako 可以绕过这种缓慢的更新速度，它仍然有奇怪的红绿蓝点簇要对付。人类通过 400 至 700 纳米电磁波谱范围内的这三个重叠区域体验世界。

[![Human_spectral_sensitivity_small](img/4671410398a4f0a35cbf6b40f4c3633d.png)](https://hackaday.com/wp-content/uploads/2015/10/human_spectral_sensitivity_small.jpg) 

人类对颜色的敏感度【来源:】诺曼·科伦

在电子世界中，只有开发出能产生不同波长光的光源。所以我们模仿人眼的操作，混合这三种波长的光来欺骗我们的眼睛，让它相信看到的是单一的颜色。

这远不是所有动物都有的。狗只能看到绿色和蓝色。一些蝴蝶能看到从紫外线到红色的东西，但是它们有很多额外的感受器(5 个，横跨整个光谱),这给了它们更强的分辨颜色的能力。

所有这些与螳螂虾相比都相形见绌。螳螂虾在紫外线中的清晰度比我们在整个光谱中的清晰度要高。共有 12 种受体类型，它拥有任何已知动物中最好的视觉([尽管它可能没有很好地利用这一信息](http://www.nature.com/news/mantis-shrimp-s-super-colour-vision-debunked-1.14578))。

但是让我们假设 Oculako 远比这个好，它的受体是[光谱](https://en.wikipedia.org/wiki/Spectrograph)。以亚纳米的精度检测光谱中的波长。它的高分辨率眼睛能够很容易地分辨出我们显示器中的单个像素，它所看到的只是一个奇怪的不断变化的颜色马赛克，没有可辨别的意义。

### LCD、LED 和 DLP 显示技术

 [https://www.youtube.com/embed/nCHgmCxGEzY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nCHgmCxGEzY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![lcd-screens-under-a-microscope1](img/61c49512b0665f4dd8e42c942c1f9a76.png)](https://hackaday.com/wp-content/uploads/2015/10/lcd-screens-under-a-microscope1.jpg) 

普通液晶显示器在显微镜下，如同 Oculako 所见。[来源: [ExtremeTech](http://www.extremetech.com/computing/122725-what-the-ipad-3s-retina-display-looks-like-under-a-microscope) ]

LCD 和 LED 显示屏稍微好一点，至少 Oculako 看到的是完整的图像，但马赛克结构仍然存在，而屏幕刷新则沿着屏幕向下，相互融合。

如果 Oculako 遇到现代的 DLP 投影仪，它可能会大吃一惊。与在空间上混合红色、绿色和蓝色的 LCD 不同，DLP 在时间上混合颜色。有一些[很棒的](https://www.youtube.com/watch?v=9nb8mM3uEIc) [视频](https://www.youtube.com/watch?v=N4aUU3-PKQ4)解释了 DLP 投影仪核心的微镜的操作。但简单地说，DLP 投影仪是由成千上万个微镜阵列组成的，这些微镜将光反射到表面上或从表面反射出去，以产生图像。

[![dmd](img/d04d85f3f36a5b7a6d6288401e9ea597.png)](https://hackaday.com/wp-content/uploads/2015/10/dmd.jpg) 

来自 DLP 投影仪的微反射镜的 SEM 图像【来源:[Ben Krasnow](https://www.youtube.com/watch?v=9nb8mM3uEIc)

由于微反射镜是“开”还是“关”，因此需要其他技术来产生颜色和强度变化。为了产生更亮或更暗的像素，镜子使用[脉宽调制](http://www.loreti.it/Download/PDF/DMD/titj12.pdf) (PDF)。通过快速开关镜子，我们的眼睛被愚弄，以为我们看到了更亮或更暗的图像。为了产生不同的颜色，投影仪通过快速旋转的色轮过滤光线。这产生了一系列快速的红色、绿色和蓝色图像，我们反应缓慢的眼睛将这些图像在时间上混合在一起，产生一个看起来连续的彩色图像。

为了利用这一过程产生逼真的图像，微镜每秒钟来回摆动数千次。Oculako advanced eyes 可以轻松识别每一个镜头。

但更重要的是，Oculako 看不出这些不断变化的马赛克有什么道理。像所谓的 Lytro 一样，“光场”相机 Oculakos 的眼睛可以捕捉进入眼睛的光线的强度和方向。这使得它能够重建周围世界的 3D 图像，比我们的立体视觉更准确，比我们刚刚起步的 3D 电视和 VR 头戴设备产生的图像更好。

 [https://www.youtube.com/embed/f_DpYzEgnfQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f_DpYzEgnfQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 那是什么声音？

虽然我们的显示可能难以理解，但你可能会认为我们的声音再现肯定更好？不幸的是，情况并非如此。人类最好的耳朵只能听到 20KHz 及以下的声音。这是被其他动物能听到的吹走的。一些物种能够感知到 100 千赫的声音。因此，我们的扬声器发出的声音对 Oculako 来说显得低沉而沉闷。像潺潺流水声这样的自然声音，也会因为被我们的音频系统剪辑而无法识别。凭借其先进的听力，Oculako 甚至可以通过声音传输复杂的数据。

[![spectrographdata](img/925b5f9c4b425f3c05508f5951b9035f.png)](https://hackaday.com/wp-content/uploads/2015/10/spectrographdata.jpg)

Image data decoded from a spectrograph.

对于 Oculako 来说，我们的世界可能是一个令人困惑的地方。人们很容易陷入这样一个陷阱，认为其他生物，无论是陆地生物还是外星生物，都可以看到我们的用户界面，即使他们不理解这些界面。但是，对我们开发的视频和音频技术的这个小调查(以及黑客为阐明它们的构造所做的伟大工作)表明，它们非常狭隘地局限于我们特定的感官。

### 与外星人交谈

[![voyagerrecord](img/c4ee364596c5f2cf66a431a6d11a57c5.png)](https://hackaday.com/wp-content/uploads/2015/10/voyagerrecord.jpg)

The Voyager Golden Record

但是我们与外星生命交流的实际尝试呢？其中最著名的可能是[航海家金唱片](https://en.wikipedia.org/wiki/Voyager_Golden_Record)。

航海家号唱片本身就是一件迷人的艺术品，它类似于一张由黄金制成的普通长唱片。在一面，它被蚀刻了一个图形，该图形被设计来提供关于记录操作的指令，以及凹坑和凹槽如何被用来在盘上存储信息。

除了可能教[外星人说话](https://youtu.be/2ATVtP3BK64?t=85s)的音频记录，该记录还编码了[彩色图像数据](http://goldenrecord.org)。不可避免地，它可能会遇到这里描述的问题。一个增强的感觉系统(如螳螂虾)并不意味着更高的智力或轻松解读复杂信息的能力，因此数据可能仍然无法理解。

尽管如此，想出一个跨物种的交流机制还是一个非常困难的问题。特别是考虑到我们不知道任何其他有意识的生命形式，他们的感官可能是什么，我们在如何传递信息方面受到严重限制。鉴于 20 世纪 70 年代以来的技术进步，你会如何设计这个时代的黄金唱片？