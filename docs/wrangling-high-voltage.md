# 争夺高电压

> 原文：<https://hackaday.com/2016/06/15/wrangling-high-voltage/>

使用高压就像使用高压管道一样。你可以在你的水管里发现一个漏洞，当然你会修理它。现在你已经修复了那个漏洞，你可以增加更多的压力，有时会出现另一个漏洞。我也有过同样的经历，不过是在高压线路上。在足够高的电压下，大约 30kV 或更高，泄漏表现为嘶嘶声和电晕，后者表现为受激离子从泄漏处喷射出的蓝色辉光。试着调高电压，嘶嘶声变成了尖叫。

为什么高压会发生漏电？我发现可视化原因的最好方法是可视化电场。电场存在于正负电荷之间，可以被描绘成电场线(如下左图所示。)电场线越密，电场越强。

 [![Weak and strong electric fields](img/8f8ac50e61a9ea2c5bb61740ec1b392d.png "Weak and strong electric fields")](https://hackaday.com/2016/06/15/wrangling-high-voltage/electric_fields_weak_and_strong/) Weak and strong electric fields [![Ionization in electric fields](img/ee2c36fb1f16fe5db3209f1cda654038.png "Ionization in electric fields")](https://hackaday.com/2016/06/15/wrangling-high-voltage/electric_fields_ionization/) Ionization in electric fields

更强的电场是空气发生电离的地方。如右上方的“碰撞”示例所示，带负电荷的电子离开导电表面(可以是电线或设备的一部分)并与附近的中性原子碰撞，将其转化为离子，从而发生电离。碰撞可以导致电子附着到原子上，将原子变成带负电的离子，或者碰撞可以从原子上敲下另一个电子，将原子变成带正电的离子。在上面的“剥离”例子中，强电场可以更直接地影响事物，从中性原子中剥离一个电子，再次将它变成正离子。还有其他效应，如电子雪崩和光电效应。

在这两种情况下，我们都想把这些电子留在导电的电线或其他表面上，它们的损失构成了一种非常真实的泄漏。

## 圆形表面与尖点

![Flat surfaces and sharp points affecting electric fields](img/ec36a568c9b5412823e9ca5e1c938949.png)

Flat surfaces and sharp points affecting electric fields

导线或表面的几何形状可以使空气中的电场变强。看右边的插图，比较两种情况。其中一个有两个相对的平面，你可以看到产生的磁场相对较弱。但是在另一种情况下，一个表面具有尖点，并且在该尖点附近产生的场很强。所以那个尖点可能会泄漏。平坦表面不必是平坦的。仅仅把一个尖点弄圆，形成一个圆形的表面，往往就能走很长的路。

哪里来的锋利点？一个明显的位置是导线的尖端，或者多股绞合导线的多个尖端。这种情况存在于两根电线缠绕在一起的地方。在下面的照片中，你可以看到同样的线路连接到一个高压电容器，但左边的灯是亮着的，右边的灯是关着的，这使得泄漏清晰可见，就像一个蓝色的电晕。看起来像喷射流的电晕是两根绞合线缠绕在一起的地方。该连接已被黑色绝缘胶带包裹，你可以看到它显然没有帮助。

 [![HV capacitor with twisted wire connection](img/b2c945718f62c2b4398fbbe6fd1ea4f6.png "HV capacitor with twisted wire connection")](https://hackaday.com/2016/06/15/wrangling-high-voltage/twisted_wires_leak_in_light_an-2/) HV capacitor with twisted wire connection [![Corona at twisted wires and capacitor plate](img/94f04b458a3f6b3effdde4e538fadbed.png "Corona at twisted wires and capacitor plate")](https://hackaday.com/2016/06/15/wrangling-high-voltage/twisted_wires_leak_in_dark_corona_visible_an-2/) Corona at twisted wires and capacitor plate

你也可以在上面的照片中看到尖点的另一个来源。电容器是由多层聚乙烯片隔开的两块方形铜板。铜板很薄，因此边缘会自动形成一个尖点。果然，顶板周围有大量可见的电晕或泄漏。具有良好圆角的更厚的板将是一种改进，因为产生的电场会更弱。

也许最意想不到的罪魁祸首是一根直径很小的金属丝，即使沿着它的长度，它也可能成为一个尖点。最明显例子是升降机，其中电晕射流用于产生升力并使升降机飞行。下面你可以再次看到同样的事情与灯打开和关闭。在提升器中，一根三角形细金属丝与铝箔裙分开，它们的电极性相反。请注意，箔片也有泄漏，主要是在角落，但也沿其长度。人们已经努力通过围绕支撑水平轻木棒折叠箔片来使箔片的顶部边缘变圆。然而，在金属丝和金属箔之间产生了火花，这些火花在金属箔上炸出了洞。这些洞有锋利的边缘，是你在箔片上看到的大部分泄漏的原因。

 [![Lifter parts showing the thin wire and aluminum foil](img/7770a61dd7513d722ab44702bef8e7fe.png "Lifter parts")](https://hackaday.com/2016/06/08/high-voltage-please-but-dont-forget-the-current/lifter_light_an/) Lifter parts [![Lifter in the dark with bluish ionization](img/675c3d47fceab5319dfc5c53807ef2e4.png "Lifter in the dark with bluish ionization")](https://hackaday.com/2016/06/08/high-voltage-please-but-dont-forget-the-current/lifter_dark_an-2/) Lifter in the dark with bluish ionization

## 防漏绝缘

防止高压漏电的第一道防线应该始终避免尖锐点或边缘。这实际上是从源头上解决问题。然而，如果你不能做到这一点，或者如果你可以，只是需要更多的帮助，那么你可以添加绝缘。

正如你在上面看到的，绝缘胶带并不总是有效的，而且在这些电压下，也不是一个很好的解决方案。胶带不太适合尖锐的边缘或尖端。相反，更好的解决方案是在表面涂上一层会变硬的液体，与表面形成紧密贴合。也许最好的绝缘材料是电晕涂料，在电子商店可以买到。顾名思义，电晕涂料是一种专门为此目的设计的涂层，防止或减少蓝色电晕。当风干时，照片中的电晕掺杂物具有 2200 伏/密耳的击穿电压，如果加热干燥则为 4100 伏/密耳。击穿电压顾名思义就是给定厚度下材料断裂的电压。2200 伏特/密耳意味着 1 密耳(1/1000 英寸)厚的涂层将在 2200 伏特下击穿。两倍厚的涂层可以承受两倍的电压，等等。

 [![Corona dope bottle](img/7d270b2acce79e7a1aa853be245b7d6b.png "Corona dope bottle")](https://hackaday.com/2016/06/15/wrangling-high-voltage/corona_dope_bottle_cr/) Corona dope bottle [![Applying corona dope to a plate's edges](img/a5f778381af92190a5443459f3c0c1bf.png "Applying corona dope to a plate's edges")](https://hackaday.com/2016/06/15/wrangling-high-voltage/corona_dope_applying_cr/) Applying corona dope to a plate’s edges

我用过的另一种涂层是蜡。艺术商店里可以买到大量的石蜡，杂货店里可以买到用于装罐的蜡。在下面的照片中，我已经在炉子上熔化了蜡，并把它倒入一个电容器模具中。(编辑熔化蜡时，确保使用双锅炉。将装有蜡的锅放入另一个沸水锅中。始终观察这个过程，以防所有的水都烧干了。)我甚至在像瓶盖一样的小圆柱形容器里做了电气连接，并在里面装满了蜡。我也用过各种环氧树脂，不管我当时有什么。有了这两种材料，你可以制作相当厚的层。在下面的照片中，你可以看到一个树脂电容器，我已经走了极端，甚至在侧面涂上了蜡。

 [![Pouring melted wax into a capacitor mold](img/08b9108db92cc9dc14d5bd619b19fff2.png "Pouring melted wax into a capacitor mold")](https://hackaday.com/2016/06/15/wrangling-high-voltage/wax_pouring_in_capacitor_mold_cr/) Pouring melted wax into a capacitor mold [![Resin and wax covered capacitor](img/4310f2d07edafddb4f50719c5fd5375a.png "Resin and wax covered capacitor")](https://hackaday.com/2016/06/15/wrangling-high-voltage/resin_and_wax_covered_capacitor_cr/) Resin and wax covered capacitor![Voltage multiplier board in mineral oil](img/157acc2007e94c7a692a5edef85bf18b.png)

Voltage multiplier board in mineral oil

还有一种绝缘技术是将连接或者整个电路板浸在油中，在我的例子中是矿物油。这里显示的是一个高压电源，其中整个[科克罗夫特-沃顿电压倍增器](https://en.wikipedia.org/wiki/Cockcroft%E2%80%93Walton_generator)板浸在聚氯乙烯管中的矿物油中。我从药店买了 500 毫升瓶装的矿物油。

电线上不是有绝缘层吗？确实如此，但击穿电压也适用于该绝缘。你可以买专门为高压制造的电线，它有很高的额定电压。打开一台旧的 CRT 型电脑显示器，你会看到一根厚厚的绝缘电线连到阴极射线管上。金属线本身只有 18 号左右，其余都是绝缘的。

 [![High voltage wire (red) going into CRT](img/1b1c41e4007970ac3283d1e65f2f0ed0.png "High voltage wire (red) going into CRT")](https://hackaday.com/2016/06/15/wrangling-high-voltage/hv_wire_going_into_crt_tube_cr/) High voltage wire (red) going into CRT [![Stripped high voltage wire](img/974f1d989c84342256838bd402429cc4.png "Stripped high voltage wire")](https://hackaday.com/2016/06/15/wrangling-high-voltage/high_voltage_wire_cr/) Stripped high voltage wire

## 远离地面/其他极性

但是如上所述，电场存在于两个极性之间。如果只有一根电线从高压电源连接到设备，那么另一个极性在哪里？电线所在的桌子可以作为另一个极性。我让电线穿过桌面，并不是所有的电线都与桌子紧密接触，当电源打开时，任何稍微离开桌面的电线部分都显示出对桌子的明显吸引力。电线真的动了。与平板相比，圆形截面的导线更尖锐，因此，如上图所示，导线附近的电场更强。如果强度足以电离空气，而绝缘的击穿电压太低，电线就会漏电。

这种情况也不仅限于桌面。有了足够强的电场，周围房间里的物体就能提供另一种极性。

 [![Raised high voltage wiring for a lifter](img/ea8f46d0a52ad2b1e3f2c1ade404018b.png "Raised high voltage wiring for a lifter")](https://hackaday.com/2016/06/15/wrangling-high-voltage/lifter_raised_hv_wiring_cr/) Raised high voltage wiring for a lifter [![High voltage resistors raised in the air](img/db9b538ce9d787f925563946a111724f.png "High voltage resistors raised in the air")](https://hackaday.com/2016/06/15/wrangling-high-voltage/hv_probe_raised_connections_cr/) High voltage resistors raised in the air

正如上面的照片所示，我通过将电线悬挂在空中，创建传输线来解决这个问题。我把电线放在塑料药瓶，玻璃罐，任何不导电的材料上。在左上的照片中，通向升降机的高压线(见照片的左上角)位于一个药瓶和一个玻璃容器上。然而，地线在右边，正如你在最右边看到的，可以接触桌子的侧面。右边的照片显示了在原型制作阶段制作高压探针时，塑料药瓶上的一堆高压电阻在空中升起。

但是那些瓶瓶罐罐不也起到了桌面的作用吗？如果桌面有导电性就不会。我发现层压桌面是一个相当不导电的表面，但如果上面有灰尘或水分，这是经常存在的，那么它就会导电，可以充当另一个电极。

## 建立良好的关系

我有两种联系方式。一个是给连接提供大量的圆形表面，为电荷扩散提供大量的空间，从而产生微弱的电场。另一个是在绝缘的同时尽量减少锐边。

例如，我收集圆形的金属球，并在上面打螺纹孔，以便用螺栓固定(见下面左边的照片)。留意商店里的金属球。抽屉把手是一个来源。我还从直径半英寸的铜棒上切下几块，锉平并用砂纸打磨成圆形(照片中左三)。)然后通过将金属丝缠绕在螺栓的螺纹上并拧紧螺栓来进行连接。我还养成了一个习惯，通过在电线上安装环形连接器来去除尖锐的电线末端。为了标准化，我制作了#20 1/4”螺纹孔，并使用家得宝五金件箱中的短匹配螺栓，然后使用 12-10 AWG 1/4”环形连接器。

 [![Metal balls and ring connectors](img/26d7e8a53e20588ae187c571a7def25b.png "Metal balls and ring connectors")](https://hackaday.com/2016/06/15/wrangling-high-voltage/metal_balls_and_ring_connectors_sc/) Metal balls and ring connectors [![Butt connectors and custom connectors](img/0cfe24a9523d7162c6d873464fab2439.png "Butt connectors and custom connectors")](https://hackaday.com/2016/06/15/wrangling-high-voltage/butt_connectors_and_custom_connectors_sc/) Butt connectors and custom connectors

如右图所示，对于绝缘连接方法，我剥去电线的两端，焊接在业余爱好商店买的短铜管上。我发现它们非常适合 16-14 AWG 对接连接器。我还在电线末端附近裹上绝缘胶带，足以紧贴地填满对接连接器的末端。

对于不太定制的方法，您可以搜索您所在地区的各种连接器。我喜欢我的方法，所有电线都以圆柱形连接器结束，然后通过对接连接器进行连接，因为这消除了任何不匹配的连接器问题，如果您最终需要连接两个母连接器或两个公连接器，就会出现这种问题。

## 布线类型

我已经谈到了细导线充当尖点的问题，因此导线厚度是需要考虑的因素。我还提到了导线绝缘的击穿电压问题。就我而言，我很久以前就储备了外径为 1/8”的绝缘 16 AWG 绞线。绝缘厚度有所帮助，但材料也是一个考虑因素。我的只是随机选择的，是某种形式的橡胶。但我能从一卷中买到大量的这种油，而且它保持得相当好，尽管我见过它在绝缘材料轻微受损时沿其长度泄漏。

 [![Coil of thickly rubber insulated wire](img/4d6ba2062720937317510dc70f2dcfd2.png "Coil of thickly rubber insulated wire")](https://hackaday.com/2016/06/15/wrangling-high-voltage/coil_of_high_voltage_wire_sc/) Coil of thickly rubber insulated wire [![Thick rubber insulation](img/ef47b2fc1ad46de8cd6ed3b1045f00c7.png "Thick rubber insulation")](https://hackaday.com/2016/06/15/wrangling-high-voltage/high_voltage_wire_end_sc/) Thick rubber insulation

另一种我在高压应用中见过但我自己从未用过的电线是球链。我猜圆球消除或最小化了尖锐点的问题，模仿大直径的电线。我想这些仍然需要暂停他们作为传输线。如果你有这些经验，请让我在评论中知道你做了什么，以及任何提示或需要注意的问题。

这就是我如何利用高电压将尽可能多的电压和电流输送到我想要的地方。我在高功率、高电压 DC 上的记录是在一个房间里测得的 85kV 电压，我没有发现任何漏洞，也就是说，在我像水管工一样跑来跑去把所有的漏洞都堵上之后。

有没有扯到高压电？如果是这样，请让我们知道您使用的任何提示或技巧。这些高压知识的瑰宝来之不易，我们都想听听。一如既往，有趣的不仅仅是成功。当你试图让电子流服从你的意愿时，你遇到了什么问题？