# 用离子推进升降机扩大视野

> 原文：<https://hackaday.com/2016/07/13/expanding-horizons-with-the-ion-propelled-lifter/>

像许多人一样，在经历了紧张的职业生涯建设期之后，大学是一个创造事物的干涸期。当然，一切都安定下来了，我终于打破了那段干旱期，开始研究我所谓的“非常规推进”。

我想远离“反重力”这个术语，因为我是一个科学迷，知道这种东西是可疑的。但我也怀疑可能有科学原理有待发现。不管怎样，我愿意试一试，而且试了几年。这也是我对高压世界……DC 的介绍。然而一切都是无效的，这意味着任何效应都可以通过某种形式的电离或库仑力来解释。虽然由于离子推进，转子上有很多旋转的东西，天平和天平上的重量也有变化，但我从来没有让任何东西真正飞起来。

所以当 2001 年一个叫做 Transdimensional Technologies 的小公司的视频出现时，一个三角形的，铝箔和金属线的东西，叫做升降机，实际上可以把自己推离桌子，我马上就要做一个。那时我已经有了足够的背景知识，可以确信它是用离子推进飞行的。事实上，鉴于我的背景，我能够在我的第一个版本中加入别人后来才想到的改进。

 [![Lifter parts](img/434ee67d6e6f75b4be56005f60d656ee.png "Lifter parts")](https://hackaday.com/2016/07/13/expanding-horizons-with-the-ion-propelled-lifter/lifter_flying_closeup_side_view_an/) Lifter parts [![Lifter flying](img/39352a93ad89b9c9feb13aff3392fb4b.png "Lifter flying")](https://hackaday.com/2016/07/13/expanding-horizons-with-the-ion-propelled-lifter/lifter_flying/) Lifter flying

对于那些从未见过举重运动员的人来说，这非常简单。可以把它想象成一个非常漏的电容。一个电极是三角形的铝箔裙。通常使用 1/6 英寸的轻木棒，与它间隔大约一英寸，是一根非常细的裸线(想想 30AWG ),形状也像三角形。在箔裙和金属丝之间施加高电压。结果是一股向下的气流围绕并穿过三角形的中间，升降机从桌子上飞了起来。但这只是对其工作原理的最基本的解释。我们必须深入！

### 不稳定的轻量级

对于一个成功的举重运动员来说，它必须非常轻。不可能把电源带走。一个典型的 4 英寸(100 毫米)长的升降机仅重 0.07 盎司(2 克)。

如果你曾经见过电压逐渐升高时升空，你会注意到它的飞行路径非常不稳定，直到电压足够高，它似乎悬停。事实是，飞行仍然是不稳定的，或者会是，如果不是三根线绑在腿上，将每个角落都拴起来。典型地，三角形的三条边产生的推进力是不均匀的，所以为了使它稳定，所有三条边都必须有足够的推进力来提升它们各自的边。这意味着最强的一方推进力超过了它的需要，而最弱的一方推进力正好是它需要的。压住它的线使它看起来很稳定。

就在第一架升降机起飞后不久，各种变化也出现了:多个三角形连接在一起，螺旋代替三角形，甚至用箔管代替直边裙。

我记得一个来自亚洲的(我好像记得是在日本，但我不确定)是房间大小，在一个大车库或仓库里飞行。有效载荷的记录是一个 98 克的六边形升降机[使用特制的 1000 瓦电源的 40kV 提升 102 克的有效载荷](http://blazelabs.com/l-c-hexspiral.asp)。这不是如何像钢铁侠一样飞行的答案。

 [![1000 watt high voltage power supply](img/941d7f03d2b9935a4657e968cf5989ea.png "1000 watt high voltage power supply")](https://hackaday.com/2016/07/13/expanding-horizons-with-the-ion-propelled-lifter/spiralhexv3_blaze_labs/) 1000 watt high voltage power supply [![100gsetup_blazelabs](img/f2066b4ab945de250e763173811fb47e.png "100gsetup_blazelabs")](https://hackaday.com/2016/07/13/expanding-horizons-with-the-ion-propelled-lifter/100gsetup_blazelabs/) 

## 它是如何工作的

升降机[利用离子推进](http://rspa.royalsocietypublishing.org/content/469/2154/20120623.abstract)飞行。关键是一个电极作为尖点，另一个电极作为光滑的边缘。细金属丝是尖点。我的通常是积极的。空气中任何电压足够高的尖点都会使其周围的空气电离。那是因为那里有很强的电场。箔裙是光滑的边缘，极性相反，在我的例子中是负极，接地。由于表面积大，那里的电场较弱，因此电离较少。我在第一个版本中所做的改进是将最靠近电线的箔片边缘弄圆，从而产生更弱的电场。当我试着跟随别人的计划而不绕圈时，让它起飞就更困难了。对于这种形式的离子推进来说，具有由尖锐且光滑的电极产生的不对称电场是必不可少的。

![How lifter ion propulsion works](img/a364ab81b00724aaff71418eb38d0094.png)

How lifter ion propulsion works

正离子被吸引到负极裙部。一些到达裙部并被中和，一些在途中与中性空气分子碰撞并给予它们动量。中性分子继续向下运动。由此产生的向下流动的射流是由这些中性分子组成的，尽管我发现一些证据表明一些正离子也能穿过裙边。在碰撞过程中，动量通过电场从离子传递到升降机。把电场想象成手臂和手，它们实际上是升降机的一部分，把离子想象成球。一个离子与一个中性原子碰撞就好比你手中的球撞上了另一个球。当球撞到一起时，它会把你的手推向相反的方向。同样的情况也会产生离子推进力。

电子也发挥了作用，但在我的例子中，由于导线带正电，电子在产生正离子方面的作用大于传递动量。

## 烟雾和真空测试

烟雾测试显示，大量的空气快速向下移动，穿过并围绕着三角形的中间。我已经用熏香的烟雾测试过了。这不仅清楚地显示了移动的气团，而且正如你在最后一张照片中所看到的，我捕捉到了一个发光的熏香碎片，它被移动的气团迅速带走了。

 [![Smoke flowing down middle of the lifter](img/83dd902b48ab8bbc5c4de93cdf0449b4.png "Smoke flowing down middle of the lifter")](https://hackaday.com/2016/07/13/expanding-horizons-with-the-ion-propelled-lifter/lifter_smoke_test_center_smoke_1/) Smoke flowing down middle of the lifter [![Burning embder flying away](img/792a22011c50ebb95367349d6a225209.png "Burning embder flying away")](https://hackaday.com/2016/07/13/expanding-horizons-with-the-ion-propelled-lifter/lifter_smoke_test_side_smoke/) Burning embder flying away [![Glowing piece flying away](img/f724bdf1f62da6e94f08dc46ae4d269a.png "Glowing piece flying away")](https://hackaday.com/2016/07/13/expanding-horizons-with-the-ion-propelled-lifter/lifter_flying_ember_03/) Glowing piece flying away

虽然在带有升降机和尖锐物体/光滑物体排列的真空室中有各种结果，但与飞行升降机相比，任何产生的运动总是微小的。有时，实验是一个沿着扭力线悬挂的装置，扭力线会产生微小的扭曲。更大的扭曲是通过根据运动的时间打开和关闭电源来实现的，但产生的更大扭曲只是共振的结果，就像当你在秋千的弧上的正确点施加力以使它荡得更高时发生的一样。

## 提示和技巧

许多试图驾驶升降机的人都失败了，因为他们的动力源不够强大。由 Transdimensional Technologies 制作的原始视频展示了一个大约 14 英寸圆顶的范德格拉夫发电机。我用我自己的 14 英寸圆顶 VDG 试了试，从蓝色的电离来看，它非常短，即使对于 2 英寸的举重运动员来说也是如此。

![PC monitor power supply powering lifter](img/9b07da673a69f46cd7e5cbce6061d96c.png)

PC monitor power supply powering lifter

要让一个 0.07 盎司(2 克)的升降机飞起来，需要 25kV 和 250 微安以上的电流(我愿意牺牲的模拟电表最高为 250 微安)。)我读过一个 0.18 盎司(5 克)的升降机需要 37 千伏和 1.7 毫安。为此，你说的是一个墙上供电的科克罗夫特-沃顿电压倍增器电源。一台[老式 CRT 电脑显示器就有这种功能，很容易适应](http://hackaday.com/2014/06/14/repurpose-an-old-crt-computer-monitor-as-a-high-voltage-science-project-power-supply/)飞行升降机。一些火花包含的电流足以损坏某些电源，尤其是电脑显示器电源。以防止使用大约 240 千欧至少 2 瓦的额定电阻与提升器的输入串联。我通常把它放在地面一侧，因为那里没有太多的[泄漏问题](http://hackaday.com/2016/06/15/wrangling-high-voltage/)。

请注意，我曾经试着从一个满是灰尘的地板上驾驶升降机，但没有成功。我怀疑灰尘被穿过裙子的正离子带正电。这将导致带正电荷的地板吸引带负电荷的裙子向下。所以远离多尘的表面。

但是让一个举重运动员飞起来的最好技巧是在完全黑暗的环境中进行——同时采取所有的安全预防措施。在黑暗中，电离的日冕看起来像蓝色的辉光。这样你就可以知道三角形的哪一边对升力有贡献。往往你会发现只是一面。在打开灯、关闭电源和升降机并使其放电后，尝试将另一侧的电线移近箔裙，或者将电离电线移远。如果你有火花，那么你把电线移得太近了。火花是离子推进的敌人，因为它们是产生离子的电场的短路。

 [![Lifter parts showing the thin wire and aluminum foil](img/7770a61dd7513d722ab44702bef8e7fe.png "Lifter parts")](https://hackaday.com/2016/06/08/high-voltage-please-but-dont-forget-the-current/lifter_light_an/) Lifter parts [![Lifter in the dark with bluish ionization](img/675c3d47fceab5319dfc5c53807ef2e4.png "Lifter in the dark with bluish ionization")](https://hackaday.com/2016/06/08/high-voltage-please-but-dont-forget-the-current/lifter_dark_an-2/) Lifter in the dark with bluish ionization

这是我举重经验中的一个脑残。你做过任何形式的离子推进吗？也许你在学校里做过更简单的旋转针形式？我们很想听听你的经历。请在下面的评论中告诉我们。