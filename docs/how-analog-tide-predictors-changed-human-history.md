# 模拟潮汐预报如何改变人类历史

> 原文：<https://hackaday.com/2015/10/08/how-analog-tide-predictors-changed-human-history/>

如果你像我一样完全是内陆国家，你可能会梦见海浪拍打海岸，但你可能不会太在意潮汐。从渔民到冲浪者，再到沿海地区的工程师，海洋潮汐的运动实际上对许多群体都非常重要。潮汐随时间的变化对那些研究世界气候变化的人来说是有用的数据。

早期潮汐预测是基于观察到的与月相有关的变化。如今，潮汐预测是通过数字计算机快速完成的。但第一台专门制造的机器是缓慢而精确的模拟计算设备，随着它们的发展，可以考虑越来越多的潮汐成分，这些成分代表了产生潮汐的天体位置的变化。这些计算奇迹中的一个甚至挽救了二战中盟军的诺曼底登陆或 D-Day。

![Tidal bulge caused by the Moon's gravitational pull. Image credit: NOAA](img/7b8320f67179415e398edb5a77579a10.png)

Tidal bulge caused by the Moon’s gravitational pull. Image credit: [NOAA](http://oceanservice.noaa.gov/education/kits/tides/tides03_gravity.html)

### 潮汐到底是什么？

在艾萨克·牛顿爵士的经典科学三部曲《原理》中，他提出了宇宙的粘合剂是组成它的物体的引力的观点。牛顿提出地球的海潮受月球的引力控制，在较小程度上受距离和太阳的影响。月球的引力导致离它最近的海水出现峰值。在地球的另一边有一个等量的峰值，因为惯性抵消了重力。海洋中的这些峰被称为潮汐隆起。

![Illustration of a continental margin from Science Clarified](img/1b9660c077766d380d0f1de1f4f38fa3.png)

Illustration of a continental margin from [Science Clarified](http://www.scienceclarified.com/landforms/Basins-to-Dunes/Continental-Margin.html)

牛顿没有考虑到大陆对潮汐行为的影响。任何特定海岸的低潮和高潮之间的距离称为潮差。在每一条海岸线下面，都有一系列洋底，在那里洋壳与大陆壳相遇。这种毕业被称为大陆边缘。只要发现宽阔的大陆边缘，潮汐隆起往往会产生更高的潮汐。相比之下，远离这些大陆边缘的岛屿往往潮汐较小。浅水河口会扭曲潮汐，导致它上升得更快。

潮汐行为受到许多其他因素的影响，包括当地的天气模式。海上的风会把潮汐拉得更远，而内陆的风会夸大潮汐的高度。海岸靠近地球的两极会增加潮差。

![Thousands of obstacles built by the Germans along the beaches of Normandy. Image credit: Military History Now](img/6ebf90de5c7bbba84a2ba2171fbdb1b9.png)

Thousands of obstacles built by the Germans along the beaches of Normandy. Image credit: [Military History Now](https://i2.wp.com/militaryhistorynow.com/wp-content/uploads/2014/06/Bundesarchiv_Bild_101I-719-0243-33_Atlantikwall_Inspektion_Erwin_Rommel_mit_Offizieren.jpg)

### 海边障碍跑道

对盟军来说，策划诺曼底登陆可不是件容易的事。纳粹占领的法国这一地区的潮差超过了六米，潮水以每小时一米多的速度上涨。这意味着如果盟军在退潮时登陆，将有一大段海滩需要穿越。德国人非常清楚潮汐表的价值，他们确信盟军会在涨潮时到达。在德国人元帅·欧文·隆美尔的指挥下，他们沿着海滩建造了数以千计的大型障碍物。他们把障碍物建在潮差的一半处，这样它们在涨潮时会变得模糊，在涨潮时会完全被淹没。希特勒称之为“大西洋墙”的这一部分的目的是摧毁盟军船只的起落架，如果他们在预期的高潮到来的话。

然而，关于在海滩上建造数百万个障碍物的事情是这样的:当退潮时，它们可以很明显地被看到，尤其是从空中。事实上，在 1944 年早春的几个月里，盟军看到它们像兔子一样繁殖。隆美尔确信船只会在涨潮时到达，但盟军现在知道这是不可能的。

### 手摇潮汐计算器

法国数学家和物理学家皮埃尔·西蒙·拉普拉斯建立了牛顿的潮汐理论。他推导出了描述海洋根据月亮和太阳的引力运动的方程，并发现所有的潮汐能都集中在少数频率上。拉普拉斯方程建立在质量和动量守恒原理的基础上，计算每个天文频率的能量。他认为这些计算是准确预测潮汐的最佳方法。

拉普拉斯的流体动力学方法在潮汐预测中首先被威廉·汤姆孙使用，他后来成为开尔文爵士。汤姆逊谐波法的主旨是收集潮汐数据，并使用拉普拉斯方程分析频率。虽然有效，但这种方法涉及大量费力的计算，用机械方法可以快得多。

![William Thomson/Lord Kelvin's first tide predictor. Image credit: UK Science Museum](img/321fe64c3d3d632dd4dd6627eeec01a8.png)

William Thomson/Lord Kelvin’s first tide predictor. Image credit: [UK Science Museum](http://www.sciencemuseum.org.img/ManualSSPL/10300041.aspx)

汤姆森创造了一台模拟计算机，在一个连续的图表上绘制潮汐运动，说明一段时间内的潮汐高度。这个装置是用手摇曲柄操作的。转动曲柄驱动成对的齿盘，每个齿盘代表一个潮汐分量，例如十二小时二十五分钟的太阴[半日](http://oceanservice.noaa.gov/education/kits/tides/tides07_cycles.html)周期。给定圆盘对的比率决定了上层圆盘移动的速度。

这种运动通过连接两者的连杆传递到一个轮子上。在圆盘末端，杆连接到许多销中的一个。针的位置决定了潮汐分量的相位和振幅。所有的组成部分都被一个共同的带连接在一起，这个系统将圆盘的旋转运动转化为笔在图上显示的正弦运动。

后来被称为开尔文潮汐机器(你一定会喜欢这个名字)，这个设备可以在大约四个小时内预测一年的潮汐数据。他的第一次迭代可以将十个潮汐分量相加。开尔文最终制作了三个版本，复杂性不断增加，最后一个版本总共有 24 个组件。

![William Ferrel's tide-predicting machine from the early 1880s. Image credit: U.S. Dept. of Commerce](img/8f229baad54c8c06ef00a9980e94ac6e.png)

William Ferrel’s tide-predicting machine from the early 1880s. Image credit: [U.S. Dept. of Commerce](https://commons.wikimedia.org/wiki/File:099-ferreltpm.jpg#/media/File:099-ferreltpm.jpg)

大约在同一时间，威廉·费雷尔正在为美国海岸和大地测量局建造一台类似的机器。费雷尔的潮汐预报器解释了 19 种不同的潮汐成分。不过，它的工作原理与汤姆森的机器有点不同。一系列的刻度盘和刻度显示了连续的高潮和低潮时期的时间和高度，而不是绘制曲线。操作员从左侧用一只手转动它，记下结果。这些数字被复制到表格中，并用于为一般海洋航行创建潮汐表。费雷尔的机器从 19 世纪 80 年代早期一直使用到 1910 年。它被美国 2 号潮汐预报机取代，该预报机能够将 37 个潮汐分量相加。这台机器，也被称为“老黄铜大脑”(又一次，一种计算设备的惊人名称)，在被计算机取代之前，已经使用了 55 年。

### 进攻日

虽然这些机器可以在一个下午预测一年的潮汐活动，但对数据的谐波分析需要几周时间才能完成。进入二战后，美国军方根据来自老要员的消息，在太平洋和其他地方进行了几次成功的两栖登陆。

在英国，利物浦潮汐研究所的亚瑟·托马斯·杜森负责潮汐预报。正是杜森对盟军诺曼底登陆做出了惊人的预测。杜森需要获得当地的潮汐数据，但英国人只有附近港口的信息。浅水效应和当地天气对潮汐行为的影响等因素使得无法根据港口数据对着陆点进行插值。如果潮水涨得太快，浅水效应真的会打乱拆除障碍物的计划。

![Image credit: Physics Today magazine](img/1c8e340e1f40aaed1d5499eaca64255b.png)

Image credit: [Physics Today magazine](http://scitation.aip.org/content/aip/magazine/physicstoday/article/64/9/10.1063/PT.3.1257)

秘密的英国侦察队秘密地在敌人的海滩上收集浅水数据，并把它送给杜森进行分析。让事情更加复杂的是，特工们不能直接告诉杜森入侵计划是针对诺曼底海滩的。所以他不得不从威廉·伊恩·法夸尔森发给他的调和常数中计算出来，法夸尔森是皇家海军水文局的潮汐主管。他使用了开尔文预测器的第三次迭代和另一台机器。这些被保存在不同的房间里，以免被同一个炸弹带走。

1944 年初春，盟军发现大西洋墙障碍后，该任务不得不重新评估。新计划？退潮后立即登陆，并派遣爆破队炸毁障碍物，建立安全通道。这样，较大的船只可以在涨潮时进港，放下部队，然后返回大海。

这个计划由于英吉利海峡沿岸的海滩位置而变得更加复杂，他们几乎不得不在晚上穿过那里。盟军需要计算出第一道曙光和晚起的月亮出现在低潮时的时间。1944 年 6 月的三天完全符合这个要求:5 日^日，6 日^日，7 日^日。

### 身体不适

尽管艾森豪威尔将军选择了 6 月 5 日为诺曼底登陆日，但天气却不太好。风太大了，无法着陆。幸运的是，他的工作人员预测天气会有所好转，这使得 6 月 6 日^(T3 成为现实。隆美尔认为天气和不利的潮汐将完全阻止盟军，所以他大大减少了奥马哈海滩以外的部队，并离开了他的岗位。其余的，正如他们所说，都是历史了。)

[主图:美国 2 号潮汐预报机通过 [NOAA](https://tidesandcurrents.noaa.gov/predma2.html)