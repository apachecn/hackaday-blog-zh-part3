# 百万像素竞赛及其明显的赢家

> 原文：<https://hackaday.com/2017/02/07/the-megapixel-race-and-its-clear-winner/>

像任何受摩尔定律启发的竞赛一样，20 世纪 90 年代末到 21 世纪初的数码相机百万像素竞赛对每个制造商来说都是一个残酷的战场。随着智能手机的发展，它成为了两条战线上的战争，三星最终将 2000 万像素塞进了手持设备。虽然没有明确的消费者级相机赢家被宣布(三星最终将旗舰手机的相机降低到 1600 万像素，原因我们将讨论)，但这场比赛似乎已经结束，消失在一个甚至营销和广告集团都不愿意冒险的空白中。发生了什么事？

## 这项技术

摩尔定律的简要概述预测，给定计算机芯片上的晶体管密度应该每两年翻一番。数码相机的传感器非常相似，使用相同的硅来形成电荷耦合器件或 CMOS 传感器(一些 RAM 和其他数字逻辑技术中使用的相同 CMOS 技术)来检测撞击它的光子。意识到摩尔定律如何适用于数码相机图像传感器上的光电探测器数量并不是一个太远的飞跃。然而，像晶体管密度一样，在不良效应开始出现之前，在给定区域内安装多少光电探测器也是有限制的。

![cmos_image_sensor_mechanism_illustration](img/e5df481d5b2bb58206692f4ff73c98a3.png)

CMOS Image Sensor Mechanism Illustration, By User:たまなるたみ – drawing created myself, GPL, [https://commons.wikimedia.org/w/index.php?curid=371238](https://commons.wikimedia.org/w/index.php?curid=371238). Note that each pixel has its own amplifier.

自视频摄像管问世以来，图像传感器已经取得了长足的进步。在 70 年代，电荷耦合器件(CCD)取代了[阴极射线管](https://en.wikipedia.org/wiki/Video_camera_tube)成为主流的视频捕捉技术。CCD 的工作原理是将电容器排列成阵列，并用小电压偏置它们。当一个光子击中其中一个电容器时，它被转换成电荷，然后可以存储为数字信息。虽然仍有专门的 CCD 传感器用于一些利基应用，但现在大多数图像传感器都是 CMOS 类型的。CMOS 对每个像素使用光电二极管，而不是电容器，以及一些其他晶体管。CMOS 传感器的性能优于 CCD 传感器，因为每个像素都有一个放大器，可以更准确地捕捉数据。与同等尺寸的 CCD 相比，它们速度更快，更容易扩展，一般使用的元件更少，功耗更低。尽管有这些优势，但是当越来越多的传感器被集成到一块硅片上时，现代传感器仍然有许多限制。

虽然晶体管密度往往受到量子效应的限制，但图像传感器的密度却受到实际上是“嘈杂”图像的限制。材料内部的热波动会在图像中引入噪声，因此如果单个像素的电压阈值太低，以至于在不应该记录光子的时候错误地记录了光子，图像质量将会大大降低。这在 CCD 传感器中更明显(一种效应称为“[晕光](http://micro.magnet.fsu.edu/primer/digitalimaging/concepts/ccdsatandblooming.html)”)，但类似的缺陷也可能发生在 CMOS 传感器中。不过，有几种方法可以解决这些问题。

![cockfield-minco](img/93f2724ec84b0b58f798c725106b653c.png)

A sunrise picture taken with an entry-level DSLR at 1600 ISO. At this sensitivity, noise in the clouds can be seen in the form of random fluctuations of some pixels. This effect would be mitigated by a camera with a larger sensor, a lower sensor sensitivity with a longer shutter speed (which would blur the turbine blades) or a scene with more light. Photo  © 2016 by Bryan Cockfield

首先，可以提高电压阈值，以便随机热波动不会上升到阈值以上来触发像素。在 DSLR 中，这通常意味着改变相机的 [ISO 设置，其中较低的 ISO 设置意味着需要更多的光来触发像素，但随机波动不太可能发生。然而，从相机设计师的角度来看，较高的电压通常意味着更高的功耗和一些速度考虑，因此在这方面需要进行一些权衡。](http://digital-photography-school.com/iso-settings/)

热波动在图像传感器中引起噪声的另一个原因是像素本身靠得太近，以至于会影响它们的邻居。这里的答案似乎很明显:简单地增加传感器的面积，使传感器的像素更大，或者两者兼而有之。如果你有无限的空间，这是一个很好的解决方案，但是对于像手机这样的东西，这是不实际的。这就触及了大多数现代手机似乎实际上被限制在 1600 万到 2000 万像素范围内的核心原因。如果像素太小，无法增加百万像素，噪声将开始破坏图像。如果像素太大，图片的分辨率会很低。

也有一些非技术性的方法来增加图像的百万像素。例如，全景图像的百万像素计数将远远高于拍摄照片的相机的百万像素计数，因为全景图像的每个部分都具有完整的百万像素计数。还可以通过使用收集更多光线的镜头(光圈数较低的镜头)来减少任何照片单帧中的噪声，这允许摄影师使用较低的 ISO 设置来降低相机的灵敏度。

## 千兆像素！

当然，如果你有无限的面积，你可以制造几乎任何尺寸的图像传感器。有一些非常大，非常昂贵的相机被称为千兆像素相机，可以拍摄难以想象的细节。然而，它们的尺寸和成本是消费类设备的一个限制因素，因此通常仅用于专业用途。有史以来最大的图像传感器有近 5 平方米的表面，大小相当于一辆汽车。该相机将于 2019 年在南美洲的[大型综合巡天望远镜](https://www.lsst.org/)中投入使用，它将利用其 8.4 米的主镜捕捉夜空图像。如果这是消费品百万像素竞赛的一部分，它肯定会是赢家。

![design_of_the_lsst_camera](img/01a7947649371776a12a873f40bf6297.png)

LSST Image Sensor, By Todd Mason, Mason Productions Inc. / LSST Corporation – [https://www.lsst.org/sites/default/files/photogallery/Camera_CU-full.jpg](https://www.lsst.org/sites/default/files/photogallery/Camera_CU-full.jpg), CC BY-SA 4.0, [https://commons.wikimedia.org/w/index.php?curid=52230238](https://commons.wikimedia.org/w/index.php?curid=52230238)

综上所述，很明显，数码相机需要考虑的不仅仅是百万像素。相机的诸多方面，如物理传感器尺寸、镜头、相机设置、后处理能力、滤镜等。在达到图像传感器的实际极限之前，百万像素本质上是营销人员宣传其产品优越性的一种简单方式。超过一定限度，更多的百万像素不会自动转化为更好的图片。然而，正如已经提到的，百万像素数量可能很重要，但是如果必须的话，有很多方法可以弥补较低的百万像素数量。例如，即使在手机中，具有高动态范围的图像也正在成为标准，这也有助于消除对闪光灯的需求。无论你决定什么，如果你想开始拍出好照片，不要担心规格；出去拍些照片吧！

(标题图片:银河系中心部分的 VISTA gigapixel 马赛克，由欧洲南方天文台(ESO)制作，在知识共享署名 4.0 国际许可下发布。这是原始的 108，500 x 81，500，9 千兆像素图像的缩放版本。)