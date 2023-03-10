# 用开尔文勋爵的雷雨从水中获得火花

> 原文：<https://hackaday.com/2017/03/27/getting-sparks-from-water-with-lord-kelvins-thunderstorm/>

在对我们最近关于 Wimshurst machines 的[文章的评论中，我们看到一些黑客从未听说过它们，这提醒我们，我们都有不同的背景和许多可以分享的东西。好吧，这里有一个我想听说过的人会更少。它甚至从未出现在任何一篇 Hackaday 文章中，那篇 Wimshurst 文章的评论中也指出了这一点。这是开尔文勋爵的滴管，又名开尔文勋爵的雷雨，](http://hackaday.com/2017/03/03/how-wimshurst-machines-work-high-voltage-from-the-gods/)[由](https://books.google.ca/books?id=2lgwAAAAIAAJ&pg=PA391&lpg=PA391&redir_esc=y#v=onepage&q&f=false)[威廉·汤姆森，第一代开尔文男爵](https://en.wikipedia.org/wiki/William_Thomson,_1st_Baron_Kelvin)于 19 世纪 60 年代发明，开尔文温标就是以他的名字命名的。这是一种从下落的水滴中产生高电压和火花的装置。

## 简要概述

 [![Kelvin water dropper parts](img/1372150aa8d4931d40b92dfc6bad5197.png "Kelvin water dropper parts")](https://hackaday.com/2017/03/27/getting-sparks-from-water-with-lord-kelvins-thunderstorm/kelvin_water_dropper_parts/) Kelvin water dropper parts [![Continuous water and drops](img/4d64d3791bc18da9641c4013106cee5a.png "Continuous water and drops")](https://hackaday.com/2017/03/27/getting-sparks-from-water-with-lord-kelvins-thunderstorm/continuous_water_and_drops/) Continuous water and drops

开尔文勋爵的《雷雨》是围绕水滴通过感应器下落的概念而创作的。两股水流从顶部蓄水池的小洞中流出。这些电流穿过两个金属圆筒，称为感应器，不与它们接触。如果下落的距离足够远，一股下落的水流在某一时刻会从连续的水流变成单个的水滴。

感应器垂直放置，使得当水通过感应器下落时，发生从连续水流到单个水滴的变化。为了看到这些水滴，上面右边的照片是用快速快门拍摄的。最后，水滴落入底部被称为接收器的金属罐中。

左边的接收器电连接到右边的电感器，右边的接收器电连接到左边的电感器。你可以在上面的照片中看到黄色和红色导线交叉的形式。

此外，电线连接到每个接收器，并前往火花隙的任何一侧。不时会有火花穿过缝隙。魔法。或者是？

## 它是如何工作的

1.  [![Step 1\. Starting](img/41e1730204e3bcdd3e405ccac0ebbf1f.png)](https://hackaday.com/wp-content/uploads/2017/03/step_1_starting.png) 要开始，某个地方必须有一些多余的电荷，要么是正电荷，要么是负电荷。通常是有的。假设正确的接收器有轻微的净负电荷。因为它连接到左电感，左电感也有轻微的负电荷。
2.  [![Step 2 Charging water](img/c00b890d7b428ba5590f36af6e0b8e4b.png)](https://hackaday.com/wp-content/uploads/2017/03/step_2_charging_water1.png) 这里才是真正神奇的地方。请记住，感应器是垂直放置的，连续的水流在此处分解成液滴。由于左边的感应器带负电，它排斥水中的负电荷。从蓄水池到感应器的连续水流就像电线一样，负电荷被排斥到蓄水池。但是这使得液滴落在带净正电荷的感应器下方。因为它们是单独的水滴，所以它们一直保持阳性，直到它们下面的左接收器。
3.  [![Step. 3 Charging other receiver and inductor](img/da1fda794d185510e06e172a6b678701.png)](https://hackaday.com/wp-content/uploads/2017/03/step_3_charging_other_receiver_and_inductor1.png) 左边的接收器是一个金属罐，与里面的水电接触，所以左边的接收器被那些带正电荷的水滴带正电。但是左边的接收器连接到右边的感应器。这意味着右边的电感也带正电。
4.  [![Step 4\. Charging water](img/65dafc7fb3d893645acccef546c94ef6.png)](https://hackaday.com/wp-content/uploads/2017/03/step_4_charging_water1.png) 右边的感应器也有一股连续的水流从上面进入，水滴从下面离开。由于感应器带正电，它排斥固体水流中的正电荷，使其流向上方的水库。与此同时，离开它的液滴带着净负电荷，落入下面的接收器中。
5.  [![Step 5\. More charging](img/fb56211b0474eb65ff6b73092cc07b9b.png)](https://hackaday.com/wp-content/uploads/2017/03/step_5_more_charging.png) 如果你还记得第一步，右边的水库是我们开始的那个，并且是稍微负的。现在，由于带负电的液滴落入其中，接收器变得更加带负电。由于右接收器连接到左感应器，这使得左感应器更负，这排斥了左侧流中的负电荷，而其下方的液滴带正电，并落入左接收器，使左接收器带正电，以此类推。
6.  [![Step 6\. Charging the spark gap](img/ad5cb2a02f5c14926a39eceb4c6abbc5.png)](https://hackaday.com/wp-content/uploads/2017/03/step_6_charging_the_spark_gap1.png) 于是右边的接收器变得越来越消极，而左边的接收器变得越来越积极。但是请记住，这两个接收器连接在火花隙的相对两侧。火花隙处的电极也变得越来越负和越来越正。也就是说，直到火花间隙两端的电压变得如此之强，以至于击穿了它们之间的空气，火花穿过间隙，将整个东西放电。但是当然，一些净电荷会留在某个地方，整个过程会重复。

## 扇形水滴和验电器

除了观看火花，还有一些额外的有趣方法来观察这种重复的充电和放电。一种方法是观察水滴落下时呈扇形散开，然后突然又笔直落下。

 [![Water fanning out. The camera speed was too slow to show individual drops.](img/1e7108f21e4f1924b19b900f6eda8a9a.png "Water fanning out. The camera speed was too slow to show individual drops.")](https://hackaday.com/2017/03/27/getting-sparks-from-water-with-lord-kelvins-thunderstorm/fanning_water_for_gif/) Water fanning out. Camera’s too slow for drops. [![Electroscope](img/28b1cd6f8669e769d425427eda347433.png "Electroscope")](https://hackaday.com/2017/03/27/getting-sparks-from-water-with-lord-kelvins-thunderstorm/electroscope_for_gif/) Electroscope

为什么会出现这种扇出现象？从电感器出来的液滴具有与电感器相反的电荷。例如，低于左电感的压降为正，而左电感为负。还要注意感应器的底部边缘在水滴的一侧。由于异性电荷相吸，感应器和其下方的液滴之间存在水平引力，从而使液滴产生侧向运动。

结果是液滴呈明显的扇形散开。随着电感充电越来越多，这种扇出变得越来越宽。也就是说，直到火花出现，放电一切。这时，液滴再次垂直下落，但随着电荷积聚，液滴开始呈扇形散开。

另一个有趣的观察充电和放电的方法是将验电器的终端放在感应器或接收器附近。随着电荷的积累，验电器的叶片会散开。但是当火花出现时，树叶会一起掉落

## 做大

有些建筑商使用类似淋浴喷头的东西让多条水流通过，而不是让一条水流通过每个感应器。下面是科学 YouTube 频道 Veritasium 的一个视频，展示了一个大型的非常科幻的开尔文勋爵滴管，它使用淋浴头。

它还有一个水泵来保持水的持续流动。你可能想知道如果你真的用了泵会发生什么，因为你要用电连接两个接收器。为了避免这种情况，接收器只是水滴落下的网眼。当水滴落下时，网格会带走它们的电荷。所以我想你可以说这些接收器接收电荷但不接收水。

 [https://www.youtube.com/embed/rv4MjaF_wow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rv4MjaF_wow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

