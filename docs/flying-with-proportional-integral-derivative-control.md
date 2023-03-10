# 比例-积分-微分控制飞行

> 原文：<https://hackaday.com/2016/05/18/flying-with-proportional-integral-derivative-control/>

你的四轴直升机正停在你北面 100 英尺的地方，它的摄像头正好指向目标。悬停做得很好，所有遥控发射器控制在中立位置。 *风力稍有增强，现在直升机在北方 110 英尺处。你用你的控制杆调整它的位置，但是当你这么做的时候，风停了，你超过了修正值。另一股风把它从不止一个方向推离目标，挫败感掠过你的嘴唇:啊啊啊！！你答应自己买一台有位置保持功能的新飞行电脑。*

带有智能控制器的多机是如何保持位置的？他们使用一种叫做*比例-积分-微分* (PID)控制的技术。这是一个在几乎所有可以想象的控制系统中都能找到的概念。要使用 PID，您的直升机需要测量当前位置和运动的传感器。

用于位置控制的典型传感器是 GPS 接收器和惯性~~管理~~测量单元(IMU ),由加速度计、陀螺仪和可能的磁力计(罗盘)组成。高度控制需要气压计或其他测量地面高度的工具。利用传感器融合技术结合原始数据，计算机可以确定多机的位置、运动和高度。但是计算出恰到好处的修正，而不超过或低于目标，这就是 PID 发挥作用的地方。

在本文中，我们不讨论传感器或融合，只讨论 PID 过程，因为它是控制系统广泛适用的支柱。我们将通过手动驾驶直升机来直观地了解 PID 是如何工作的。但请记住，这个例子是说明性的，并不是 100%准确，因为我们人类在控制时做的远不止简单的 PID。

让我们从一些数学术语和符号定义开始。你希望直升机悬停的位置是*设定点* *(SP)* 。那有 100 英尺远。当前位置是*过程值(PV)* 。它漂流了 110 英尺。设定值和过程值之间的差值就是*误差* *(e)* 。那是 10 英尺的漂移。计算的输出是*控制* *输出* *(C)* ，进而改变系统的控制输入。

有三个参数控制 PID 环路如何对误差做出反应，每个 PID 项一个参数。这些被称为*增益*，分别是比例、积分和微分的 *Kp、Ki、*和 *Kd* 。

# 比例控制

你又一次在没有控制输入的情况下让直升机在 100 英尺外很好地盘旋。风力增强，现在高度为 110 英尺。您添加控制输入来恢复它。投入多少？如果它到了 120 英尺呢？你可能会为 120 英尺增加比 110 英尺更多的输入，因为你想让它快速回到 100 英尺。这就是比例控制。直升机离得越远，你用越多的输入把它带回来。

数学很简单。将误差计算为设定值和过程变量之间的差值，并将结果乘以比例增益:

![\begin{aligned}  e &= SP - PV \\  C &= K_p * e \\  \end{aligned}  ](img/3cd422fec296cf51d92812fefd6ef50d.png)

表格和图表显示了直升机偏离设定点的运动和恢复。注意直升机稳定在 106 英尺，而不是设定点。这种偏移是比例控制数学所固有的。

 [![PIN P Only](img/e8d08cdbeb75b0ab4dfa80d7c1fac68d.png "PIN P Only")](https://hackaday.com/2016/05/18/flying-with-proportional-integral-derivative-control/pin-p-only/) 

电子表格实现了完整的 PID 过程。为了仅证明比例增益，所需要的是将积分和导数增益设置为零，这使得积分和导数项为零。

如果系统不产生大的误差，比例增益本身是有用的。通常，系统至少需要比例积分(PI)或比例微分(PD)控制。

# 积分控制

尽管有风，你还是让直升机回到 100 英尺。现在控制不再处于中立位置，但需要一些输入来保持 100 英尺的距离。将直升机带回到设定点并保持在那里需要 PID 的整体部分。

积分通过保持误差的总和来查看误差随时间的历史。积分方程需要一个变量，求和值 *(* *Si)，*，它是每个误差乘以 *Ki 后的和。*比例分量如上计算，并加到积分分量上。

![\begin{aligned}  S_i &= S_i + (K_i * e) \\  C &= K_p * e + S_i \\  \end{aligned}  ](img/ecdea208c70031cba864802e9a3e3cd6.png)

讨论中更常见的另一种形式是保持误差的总和，并将总和乘以 *Kp* 。如果 PID 运行时 *Kp* 的值改变，这种形式会导致一个问题，称为*凸起*。这可能不会发生在我们的系统中，但对于长期运行的流程(如炼油厂)来说是一个问题。

同样，图表显示了直升机远离设定点的运动和恢复。请注意，使用 PI 时直升机在 9 秒内稳定，而仅使用 p 时需要大约 12 秒。积分往往会使您更快地回到设定点。

 [![PID P&I](img/5afef407597bf6159f6932a88f181a40.png "PID P&I")](https://hackaday.com/2016/05/18/flying-with-proportional-integral-derivative-control/pid-pi/) 

积分的一个潜在问题是*积分*饱和。如果出现非常大的误差，或者设定值发生很大的变化，求和可能会累积到一个很大的值。这可能导致超出系统能力的控制值。对于直升机，控制值可能试图驱动马达达到其能力的 120%。消除这种积累可能需要很长时间，并可能引入超调，即直升机返回到 100 英尺设定点并继续飞行。处理这个问题的两个最简单的方法是要么限制求和可以达到的值，要么在过程稳定之前禁止积分。对于我们的项目，限制总和可能是最容易的。

# 导数调节

你再次开始把直升机从 110 英尺的位置拉回，但是你不知道风的强度。当直升机开始返回时，你观察它返回的速度，如果直升机返回的速度没有你希望的那么快，就增加输入。你在判断直升机飞行的距离。另一种说法是，你看到的是误差的变化。这是误差的导数。

导数的计算引入了另一个变量，前面的*误差* *(ep)* 。当前误差和先前误差之间的差乘以导数增益。PD 的计算方法是将 P 值和 D 值相加。当前误差被保存为前一个误差，用于下一个计算周期。

![\begin{aligned}  C &= (K_p * e ) + K_d * (e_p - e) \\  e_p &= e \\  \end{aligned}  ](img/6c72edfa4a1d1f6441738778fb81cc02.png)

图表显示了 PD 控制下的直升机运动。这里，没有积分，直升机没有回到设定点，而是停在大约 104.5 英尺，仅比 P 有所提高。到达稳定位置的时间也是大约 12 秒。

 [![PID P&D](img/af3535fb04e29c96ef2efa70d2d2db27.png "PID P&D")](https://hackaday.com/2016/05/18/flying-with-proportional-integral-derivative-control/pid-pd/) 

# 周期

下一步是向您展示完整的 PID，但还有另一个因素需要考虑，即处理周期之间的时间。为了清楚起见，我把这个留在上面了。如果 PID 以规则的间隔被处理，上面的等式将正常工作，也许由中断驱动。但是如果间隔不恒定，则必须对积分和导数计算进行调整。这需要使用每次 PID 计算之间经过的时间。这是**【dt】*的时差。添加 *dt* 因子后，PID 控制值的变化很小，只是之前计算的总和:*

 *![\begin{aligned}  e &= SP - DV \\  S_i &= S_i + (K_i * e * dt) \\  C &= (K_p * e) + S_i + K_d * (e_p - e) / dt \\  e_p &= e \\  \end{aligned}  ](img/981f1b72b0992bbb4c1951f8f6c2601a.png)

积分现在乘以 *dt* 。因此，总和就是一段时间内的误差。如果误差时间很长，积分变得更大，以更快地迫使直升机回到设定点。如果时间很短，则只增加一个小的校正。

同样，导数除以 *dt* 放大控制值。

图表显示了处理直升机偏转和返回的完整 PID。由于使用了积分项，直升机返回到设定点并稳定在大约 9 秒。但是它相当接近 7 秒时的设定点，这比早期的方法要好。

 [![PID With Time](img/2bdfc436936cae4b5909c27c061507ad.png "PID With Time")](https://hackaday.com/2016/05/18/flying-with-proportional-integral-derivative-control/pid-with-time/) 

我使用的时间是 0.5 秒，但是当它被放进图表时，直升机只移动了 105 英尺。我将风速和直升机的速度加倍，因此移动了 110 英尺，以便更容易比较所有的图表。

# PID 调节

为过程的最佳控制设置 PID 是一门黑色艺术。调整三个增益是*调整*。确定良好的 PID 增益是困难的，因为它们相互影响，并且不总是以可预测的方式。有许多论文和讨论建议如何调整 PID。自调优的概念在 PID 时代就已经存在，但是没有通用的方法来实现这一点。

如果你看看上面四个图表中的增益，你会发现每个图表都使用了不同的值。这些是我通过试验不同的增益，为每组计算获得的最佳值。我有两个目标。首先，尽快让直升机稳定下来。第二，不要超过设定值。第一个几乎总是调优的目标。第二个是任意的，但是它帮助限制了我需要做的测试的数量。像直升机这样的一些过程可以容忍超调。其他的则不能，过冲实际上会导致整个系统的损坏。

# PID 分类代码

一个非常基本的 PID 类的代码，至少足以让你开始，是一个简单的等式实现。类声明是:

```

//
//-------------------------------------------------------------------------------------------------
class PID {
public:
	PID(const double p_gain, const double i_gain, const double d_gain, double setpoint);

	const double calculate(const double current_value, const double time_interval);

private:

	double mProportionalGain;
	double mIntegralGain;
	double mDerivativeGain;
	double mSetpoint;

	double mIntegralSum {0};
	double mPreviousError {0};
};

```

只有两个班级成员。一个是类构造函数，用于初始化 PID 计算的增益和设定点值。另一个执行 PID 计算。

构造函数和计算的实际类代码是:

```

//
//-------------------------------------------------------------------------------------------------
PID::PID(const double p_gain, const double i_gain, const double d_gain, double setpoint) :
		mProportionalGain(p_gain), mIntegralGain(i_gain), mDerivativeGain(d_gain), mSetpoint(setpoint) {
}
//-------------------------------------------------------------------------------------------------
const double PID::calculate(const double current_value, const double time_interval) {
	const double error = mSetpoint - current_value;

	const double proportional = mProportionalGain * error;

	const double integral = error * mIntegralGain * time_interval;
	mIntegralSum += integral;

	const double derivative = mDerivativeGain * (mPreviousError - error) / time_interval;
	mPreviousError = error;

	return proportional + mIntegralSum + derivative;
}

```

我用这段代码复制了我的电子表格的结果，但是如果不做更多的工作，我不会把它放在机器人上。一组更有用的代码是由 Brett Beauregard 开发的 Arduino PID 库。在他的项目博客中，[【布雷特】解释了代码](http://brettbeauregard.com/blog/2011/04/improving-the-beginners-pid-introduction/)，尤其是引入的使其更加健壮和有用的变化。一个基于[Brett 的]代码的[交互式 PID](http://codinglab.blogspot.be/2016/04/online-pdi-trainer.html) [模拟](http://codinglab.blogspot.be/2016/04/online-pdi-trainer.html)在[Raul 的]编码实验室博客上。

我们主要考虑了环境因素对系统的破坏。PID 在改变系统动作方面也很有用。我们把直升机定位在离我们 100 英尺远的地方。PID，实际上是多个 PID，相互作用以将其保持在该位置。多个 PID 控制倾斜、旋转、高度和方位，并在出现错误时进行纠正。如果我们决定直升机应该离我们 120 英尺，再高 20 英尺，控制器实际上可以改变设定点，让 PID 将误差校正到新的设定点。

PID 是控制系统的主力，任何使用机器人或其他交互系统的黑客都应该知道。这里的示例代码只是一个起点，让您感受一下算法是如何工作的。*