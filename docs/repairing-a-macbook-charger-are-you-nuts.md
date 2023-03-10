# 用开心果修理 Macbook 充电器

> 原文：<https://hackaday.com/2018/01/04/repairing-a-macbook-charger-are-you-nuts/>

笔记本充电器面临艰难的生活。它们被反复插上插下，卷成一团，塞进袋子里，扔来扔去，总的来说受到的待遇相当差。将这一点与相当轻便的设计结合起来，笔记本电脑充电器在几年后出现故障并不罕见。通常是连接器先走。当我发现自己面对一个故障的 Macbook 充电器时，情况就是这样，我认为这是一个简单的修复方法。唉，我错了。

不像大多数个人电脑制造商依赖简陋的桶形插孔及其现成的变体，苹果喜欢在 Macbook 系列上使用 Magsafe 连接器。这种连接器有许多优点，例如在有人被电缆绊倒的情况下可以快速释放，并且它可以插入而不用考虑方向。然而，这并不是最容易解决的问题。当充电器开始失灵时，我注意到两个症状。第一个是，充电器只有在电缆的方向完全正确的情况下才能工作。另一个是，即使当它充电时，连接器也会变得非常热。这让我怀疑间歇性连接是罪魁祸首，而且是相当糟糕的连接；高电阻导致发热问题。

[![Charger cable worn out near connector](img/5725fb70436d18dc967aeed9913e2650.png)](https://hackaday.com/2018/01/04/repairing-a-macbook-charger-are-you-nuts/vlcsnap-error649-b/)

Our starting point – a badly worn and frayed Macbook charger. I found it interesting to see that the shield was in two layers, wound in alternate directions.

[![Cutting magsafe enclosure with side cutters](img/2eda0e27c5c2f77162f61b0a67cd3ce9.png)](https://hackaday.com/2018/01/04/repairing-a-macbook-charger-are-you-nuts/removing-magsafe-enclosure-with-side-cutters/)

Sidecutters weren’t the best tool for the job, but they’re what I had lying around. The soft metal is fairly easy to cut with hand tools.

在这一点上，与任何其他充电器一样，你可以拿出你可信赖的侧剪，剪下末端，然后在 Digikey 上轻轻一点就可以得到一个替换部件。用 Magsafe？没有骰子。替换零件根本不可用，这是专有连接器的常见问题。不管怎样，我尽力去解决这个问题。我开始用偏口钳剥去连接器背面的金属外壳，最后用角磨机。实际上，Dremel 是这项工作的完美工具，但我还是坚持了下来。在非常惊愕之后，我把连接器剥开，并且能够识别问题。

Macbook 充电器的电缆由聚四氟乙烯护套的中心导体组成，然后由两层以相反方向缠绕的屏蔽层包围。中心导体焊接到一个连接到 Magsafe 连接器 V+引脚的插片上，屏蔽层连接到另一个插片上，通向 GND。问题是，在使用多年后，电缆的不断弯曲导致屏蔽线束随着时间的推移而断裂，最终导致接触不良或没有接触。这解释了我们看到的症状，所以我相信我已经找到了根本原因。在清理完连接器的焊片后，我刚刚剥去了充电器的电线，把所有东西都焊回原位。用万用表对引脚进行了几次检查，表明一切都连接正确，将充电器插回 Macbook 表明维修成功。

### 噢，疯子！

![](img/78eff594f7c273911d90fe2cbf6b650d.png)

Filling the shell with epoxy is a delicate process. Be sure to avoid getting any glue on the spring contacts; this is an easy way to ruin the connector permanently.

现在只有一个小问题需要解决。虽然充电器可以使用，但由于铝外壳已被移除，因此很难插入和移除。这一点，加上现在暴露在外的电线，意味着必须采取一些措施。我决定为连接器做一个新的保护盖，幸运的是，我手头有完美的零件。

你有没有试过打开一个没有裂开的开心果？凡人没有工具是不行的。开心果壳可以很好地充当连接器的保护外壳。Magsafe 放在里面，外壳填充了环氧树脂，将所有东西固定在一起，并使电线绝缘。

很难将连接器保持在外壳内的适当位置；如果我要再次解决这个问题，我会在用环氧树脂填充外壳之前，用强力胶将连接器固定到位。不管怎样，我坚持了下来。由于我不小心购买了 24 小时，而不是 5 分钟的环氧树脂，经过了比预期更长的等待后，它被固化了。快速整理一下文件，一切都准备好了。

我很高兴把充电器修好了。开心果包装被证明是一个值得的解决方案，在拆卸和重建后，给连接器带来了急需的坚固性。它得到了奇怪的盯着这里和那里，因为在一天结束时，有一个开心果伸出充电端口。

![](img/a0eddfd80e16272fc1f8e91126594cf0.png)

Is it perfect? No. Does it work? Yes.

但是，嘿，有时候这就是你为进步付出的代价。

从根本上说，使用专有连接器是一件非常痛苦的事情。它们很难找到来源，如果无法修复，它们会使设备完全瘫痪。然而，只要有一点毅力和创造力，如果你有勇气去尝试，有时还是有可能扭转局面的。

 [https://www.youtube.com/embed/-8zzeDjmq6M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-8zzeDjmq6M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

