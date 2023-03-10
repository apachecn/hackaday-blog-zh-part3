# 嵌入埃利奥特:音频回放与直接数字合成

> 原文：<https://hackaday.com/2016/02/12/embed-with-elliot-audio-playback-with-direct-digital-synthesis/>

直接数字合成(DDS)是一种样本回放技术，它有助于在不增加硬件的情况下将少量音频添加到项目中。想让你的机器人在撞到墙上时发出哎哟声吗？还是吹长笛独奏？当然，你*可以*只买一个便宜的 WAV 播放屏蔽或模块，然后把所有的样本写到 SD 卡上。那么你就不必了解微控制器如何产生音调音频，可以跳过本专栏的其余部分，继续你的生活。

[![Harmonic distortion down ~45db on an Arduino](img/a9546cf2bec9822176b2802b2bee1fbe.png)](https://hackaday.com/wp-content/uploads/2016/02/scope_2.png)

~45db signal to noise ratio from an Arduino

但这不是我们做事的方式。我们将把音频数据嵌入到代码中，用绝对最少的额外硬件来回放它。我们也将获得过程的控制权。如果您想要更快或更慢地弹奏样本，或者添加颤音效果，您将需要亲自动手。我们将向您展示如何获取单个数据样本，并以您喜欢的任何音高回放它。DDS 过于简单，即使您使用固定频率的时钟，它也是一种使这些音高修改成为可能的方法。

这里使用的相同技术可以将您的微控制器变成一个便宜而令人愉快的函数发生器，使用 PWM 可以在 100 千赫以下工作，而且速度更快，模拟输出更好。Hackaday 自己的[Bil Herd]有一个关于数字信号生成硬件方面的很好的视频帖子[，如果你想走这条路，它是这个帖子的一个很好的伴侣。但我们在这里将重点放在音频上，因为它更容易，更实用，也更有趣。](http://hackaday.com/2014/11/24/direct-digital-synthesis-dds-explained-by-bil-herd/)

我们将从您想要回放的音频的*样本*开始，这是一些与麦克风或类似设备在固定时间点测量的电压水平相对应的数据。要播放样本，我们只需让微控制器以完全相同的速度输出这些电压。假设您的“模拟”输出是通过 PWM 实现的，但也可以是您选择的任何其它数模转换器(DAC)。每个采样周期，代码都会查找一个值，并将其写入 DAC。搞定了。

(事实上，除了从 SD 卡的文件系统中读取数据，并可能有一些板载放大，这就是那些小 WAV 播放器单元正在做的所有事情。)

## 音调控制

在最简单的例子中，如果样本回放速率等于输入采样速率，样本将以与它被录制时完全相同的音高回放。您可以通过加快回放速度来提高音调，反之亦然。最明显的方法是改变样本回放时钟。每个周期你回放一个下一个样本，但你改变样本之间的时间，给你想要的音高。这对于一个样本非常有用，如果你有无限可变的回放速率。

[![Woof!](img/a6f9e801014db9c4442b47dfe9531cf6.png)](https://hackaday.com/wp-content/uploads/2016/02/scope_23.png)

Woof!

但是让我们假设你想用你的狗叫的样本来演奏贝多芬的第五交响曲。你需要多种声音以不同的速度回放样本来制作不同的音高。以这种简单的方式演奏多个音高，将需要多个样本回放时钟。

这就是 DDS 的用武之地。这个想法是，给定一个采样波形，您可以通过根据需要跳过或重复采样点来播放来自固定时钟的几乎任何频率。有效地做到这一点，并以最小的附加失真，是 DDS 的诀窍。DDS 有其局限性，但主要取决于您使用的处理器。如今，你可以买到射频 DDS 芯片，它可以输出高达数百兆赫的非常干净的采样正弦波，具有惊人的频率稳定性，因此你知道这种方法是合理的。

## 例子

让我们用一个简单的例子把事情具体化。假设我们有一个 256 字节长的单周期波形样本，每个 8 位字节对应一个时间点的单个测量电压。如果我们以每个样本 10 微秒的速度回放这个样本，我们将得到 1 / (10e-06 * 256) = 390.625 Hz 的音高，在钢琴中间的“G”周围。

想象一下，我们的回放时钟不能走得更快了，但我们仍然想演奏音高稍微高一点的“A ”, 440Hz。如果我们一开始只采样了 227 字节的数据，我们就可以播放“A”:1/(10e-06 * 227)= 440.53，但是现在想这个有点晚了。另一方面，如果我们忽略其中的 29 个样本，我们就会在那里。同样的逻辑也适用于演奏较低的音符，但顺序相反。如果一些样本被播放两次，甚至更多次，你可以任意降低循环的重复率。

在跳过样本的情况下，您可以只砍掉最后 29 个样本，但这将严重扭曲您的波形。你可以想象将 29 个样本分散到 256 个样本中，然后以这种方式删除它们，这样效果会更好。DDS 则更进一步，在采样波形的每个周期中移除不同的均匀间隔样本。它通过一些简单的数学运算来完成。

[![accumulator_wheel](img/b94604a0c93ca19be56e87d447f031c6.png)](https://hackaday.com/wp-content/uploads/2016/02/accumulator_wheel.png) 症结在于*蓄电池*。我们将 256 个样本嵌入到一个更大的空间中，也就是说，我们将创建一个包含更多步骤的新计数器，这样我们样本中的每一步都对应于我们更大的计数器(累加器)中的许多数字。在我下面的示例代码中，256 步中的每一步都有 256 个计数。因此，为了每周期前进一个样本，我们需要将 256 加到较大的计数器上。要走得更快，你每期加 256 以上，要走得更慢，加得更少。除了实现细节之外，就这些了。

在这里的图表中，因为我不能画出 1，024 个刻度线，我们在累加器中有 72 个步骤(绿色外环)和 12 个样本(内部，蓝色)。每个样本对应累加器中的六个步骤。我们将累加器每周期推进四步(红线)，您可以看到第一个样本如何播放两次，然后下一个样本只播放一次，等等。最后，样本的播放速度会比每个时间段取一个样本时慢。如果增量超过六步，一些样本会被跳过，波形会播放得更快。

## 实施和构建

因此，让我们将它编码并闪存到 Arduino 中进行测试。GitHub 上有[代码，你可以跟着看。我们将进行三个演示:一个工作的基本实现，一个工作得更好的改进版本，最后一个播放狗叫的单个样本的愚蠢版本。](https://github.com/hexagon5un/barking_dogs_dds_demo)

[![Filter "circuit"](img/e460deeebeab1f90f5c191af3d836195.png)](https://hackaday.com/wp-content/uploads/2016/02/dds-sch1.png)

Filter “circuit”

总的来说，我们将使用滤波 PWM 产生模拟输出波形，并使用 AVR 芯片中的硬件级 PWM 控制来实现。简而言之，有一个定时器，从 0 到 255 重复计数，并在开始时打开一个引脚，在指定的最高值时关闭。这使我们能够以最小的 CPU 开销创建快速 PWM 信号，并且它使用定时器。

[![Still some jaggies left. Could use better filter.](img/c5218271dbffa37c2b99ab33562f09fa.png)](https://hackaday.com/wp-content/uploads/2016/02/scope_4.png)

Still some jaggies left. Could use better filter.

我们将使用另一个定时器，它定期触发并运行一些代码，称为中断服务程序(ISR)，将电流样本载入 PWM 寄存器。我们所有的 DDS 代码都将存在于这个 ISR 中，所以这就是我们关注的全部。

如果这是你第一次直接使用微控制器上的定时器/计数器，你会发现一些配置代码，你真的不必担心。您只需要知道它设置了两个定时器:一个尽可能快地运行并控制音频输出的 PWM 引脚，另一个运行以便持续调用特定的代码块，在本例中为每秒 24，000 次。

话不多说，ISR 来了:

```

struct DDS {
    uint16_t increment;
    uint16_t position;
    uint16_t accumulator;
    const int8_t* sample;   /* pointer to beginning of sample in memory */
};
volatile struct DDS voices[NUM_VOICES];

ISR(TIMER1_COMPA_vect) {
    int16_t total = 0;

    for (uint8_t i = 0; i &lt; NUM_VOICES; i++) {
        total += (int8_t) pgm_read_byte_near(voices[i].sample + voices[i].position);

        /* Take an increment step */
        voices[i].accumulator += voices[i].increment;
        voices[i].position += voices[i].accumulator / ACCUMULATOR_STEPS;
        voices[i].accumulator = voices[i].accumulator % ACCUMULATOR_STEPS;
        voices[i].position = voices[i].position % SAMPLE_LENGTH;
    }

    total = total / NUM_VOICES;
    OCR2A = total + 128; // add in offset to make it 0-255 rather than -128 to 127
}

```

代码做的第一件事是定义一个(全局)变量，它将保存我们想要的尽可能多的声音的状态，由`NUM_VOICES`定义。每个声部都有一个`increment`,它决定每个样本输出在累加器中采取多少步。`position`精确记录我们的波形数据中 256 个样本中的哪一个正在播放，`accumulator`记录其余的。这里，我们还允许每个声音从内存中回放不同的波形表，所以代码需要跟踪每个`sample`开始的地址。改变回放的样本很简单，只需将这个变量指向不同的内存位置，我们将在后面看到。具体来说，您可以想象这个样本内存包含正弦波中的点，但实际上任何重复的波形都可以。

 [![scope_7](img/fa541605ed982563bdf159b6b97bb94a.png "scope_7")](https://hackaday.com/2016/02/12/embed-with-elliot-audio-playback-with-direct-digital-synthesis/scope_7/)  [![scope_6](img/95fd3306a92459dc622d00085790b49d.png "scope_6")](https://hackaday.com/2016/02/12/embed-with-elliot-audio-playback-with-direct-digital-synthesis/scope_6/)  [![scope_8](img/f57443224f64372294146d78c3275ce9.png "scope_8")](https://hackaday.com/2016/02/12/embed-with-elliot-audio-playback-with-direct-digital-synthesis/scope_8/)  [![scope_10](img/056890099263dcc606bc7933bf112966.png "scope_10")](https://hackaday.com/2016/02/12/embed-with-elliot-audio-playback-with-direct-digital-synthesis/scope_10/) 

因此，让我们深入了解 ISR，以及日常工作的核心。每个更新周期，不同声部的输出总和在`total`中计算。对于每个声音，从存储器中读取当前样本，添加到`total`中，然后递增到下一步。在这里我们可以看到`accumulator`是如何工作的。`increment`变量被添加到`accumulator`中。当`accumulator`大于每个样本的步数时，`position`变量开始移动。接下来，使用模操作符将`accumulator`收缩回未计算值的余数，并且如果需要，使用另一个模来回绕样本位置。

### 组织？？模数？？

如果你以前使用过微控制器，现在你的脑海中可能会响起警铃。AVR 没有内置的除法例程，因此可能会占用大量 CPU 资源。而模运算符就更差了。也就是说，除非除数或模数是 2 的幂。在这些情况下，除法相当于将二进制数向右移动 2 的幂的位数。

类似的操作使得模是可容忍的。例如，如果您希望一个数以 8 为模，您可以简单地丢弃所有对应于值 8 或更高的二进制位。因此，`x % 8`可以被实现为`x & 0b00000111`，其中该逻辑与仅保留最低有效的三位。如果你与你内心的比特翻转器不合拍，这可以被看作是一个细节——但是只要知道当你选择 2 的幂作为除数时，如果你的编译器知道如何有效地实现它们，除法和模不一定是坏消息。

这让我们到了程序的最后。样本值相加在一起，因此现在需要除以声部数量并以中点为中心，以符合 PWM 输出寄存器要求的 8 位范围。一旦该值被载入存储器，PWM 硬件将在下一个周期输出正确的波形。

 [https://www.youtube.com/embed/1f1Pfhbeabg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1f1Pfhbeabg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 风雅

上面的 ISR 已经相当精简了。它避免使用任何会降低速度的`if`语句。但事实证明我们可以做得更好，这种优化的形式通常是 DDS 的呈现方式。请记住，我们以每秒 24，000 次的速度运行这个 ISR(在本例中)——ISR 内部的任何加速都会对整体 CPU 使用率产生很大影响。

我们要做的第一件事是确保我们只有 256 个样本。这样，我们可以通过简单地使用一个 8 位变量作为样本值，来去掉将样本索引限制在正确范围内的那一行。只要`sample`索引中的位数与样本长度匹配，就会自动翻转。

我们可以使用相同的逻辑将上面的`sample`和`accumulator`变量合并成一个变量。如果我们有一个 8 位的`sample`和一个 8 位的`accumulator`，我们将它们组合成一个 16 位的`accumulator`，其中最高的 8 位对应于样本位置。

```

struct DDS {
    uint16_t increment;
    uint16_t accumulator;
    const int8_t* sample;   /* pointer to beginning of sample in memory */
};
volatile struct DDS voices[NUM_VOICES];

ISR(TIMER1_COMPA_vect) {
    int16_t total = 0;

    for (uint8_t i = 0; i &lt; NUM_VOICES; i++) { total += (int8_t) pgm_read_byte_near(voices[i].sample + (voices[i].accumulator &gt;&gt; 8));
        voices[i].accumulator += voices[i].increment;
    }
    total = total / NUM_VOICES;
    OCR2A = total + 128; // add in offset to make it 0-255 rather than -128 to 127
}

```

您可以看到，我们已经从`DDS`结构中完全删除了`position`值，并且 ISR 在代码行方面得到了显著的简化。(实际上，它的运行速度也快了 10%左右。)之前我们在`sample + position`播放样本，现在我们在`sample + (accumulator >> 8)`播放样本。这意味着有效的`position`值在`increment`的每 256 步中只会前进一次——只有当所有的低 256 步都被步进时，高 8 位才会改变。

顺便说一句，如果你以 10 为基数来思考这个问题，这一点都不奇怪。在第三个数字翻转到 100 之前，你习惯于数到 99。这里，我们仅使用最高有效位来表示采样步长，最低有效位的数量决定了在采取一个步长之前需要增加多少。这种方法本质上是将 16 位`accumulator`作为一个[定点](https://en.wikipedia.org/wiki/Fixed-point_arithmetic) 8.8 `position`值，如果这有助于澄清事情的话。(如果不是，我以后肯定要写点定点数学的东西。)但这就是它的主旨。

这是我所知道的在没有除法运算的处理器上实现 DDS 程序的最有效的方法，但它能够相当快地进行位移。这当然是经典的方式。问题是样本数必须是 2 的幂，每个样本的步数必须是 2 的幂，并且两者之和必须符合某个标准变量类型。在实践中，对于大多数机器来说，这通常意味着具有 8 位步长的 8 位样本或具有 16 位步长的 16 位样本。另一方面，如果只有一个 7 位样本，则可以只使用 9 位作为增量。

## 闲荡:狂吠的狗

作为最后一个例子，我想再重复一遍同样的事情，但是是一个简单的回放例子。在上面的演示中，我们播放了不断循环播放的重复波形。现在，我们想播放一次样本，然后退出。这也给我们带来了开始和停止播放的问题。让我们看看这一点在这位新 ISR 中是如何发挥作用的。

```

struct Bark {
    uint16_t increment = ACCUMULATOR_STEPS;
    uint16_t position = 0;
    uint16_t accumulator = 0;
};
volatile struct Bark bark[NUM_BARKERS];

const uint16_t bark_max = sizeof(WAV_bark);

ISR(TIMER1_COMPA_vect) {
    int16_t total = 0;

    for (uint8_t i = 0; i &lt; NUM_BARKERS; i++) {
        total += (int8_t)pgm_read_byte_near(WAV_bark + bark[i].position);

        if (bark[i].position &lt; bark_max){    /* playing */
            bark[i].accumulator += bark[i].increment;
            bark[i].position += bark[i].accumulator / ACCUMULATOR_STEPS; 
            bark[i].accumulator = bark[i].accumulator % ACCUMULATOR_STEPS;
        } else {  /*  done playing, reset and wait  */
            bark[i].position = 0;
            bark[i].increment = 0;
        }
    }
    total = total / NUM_BARKERS;
    OCR2A = total + 128; // add in offset to make it 0-255 rather than -128 to 127
}

```

这里的代码与其他两个代码大致相似。在这里，犬吠的波表恰好有 3040 个样本长，但由于我们是一次播放样本，而不是循环播放，所以这并不重要。只要每个位置的步数(`ACCUMULATOR_STEPS`)是 2 的幂，除法和模运算就能很好地完成。(为了好玩，把`ACCUMULATOR_STEPS`从 256 改成 255，你会看到整个事情慢慢地停止了。)

这里唯一的区别是有一个`if()`语句检查我们是否已经播放完波形，当我们播放完样本时，我们明确地将`increment`设置为零。波表中的第一步是零，因此不递增等同于保持沉默。这样，我们的调用代码只需要将`increment`值设置为非零值，样本就会开始播放。

 [https://www.youtube.com/embed/m8HTUx1ZR_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m8HTUx1ZR_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果您还没有，您至少应该加载这些代码，并浏览一下主体，看看它在开始和停止、按调子弹奏音符等方面是如何工作的。在第一个例子中制作“合成器”波形时，以及对采样波形进行编码以便与类似的简单 DDS 例程一起使用时，也有一些想法。如果你想从自己说“Hackaday”的例子开始，并在你的代码中运行它，你会在用 Python 写的 *wave_file_generation* 文件夹中找到你需要的一切。如果你在任何地方遇到困难，请在评论中跟我争论。

## 结论

DDS 是一个强大的工具。事实上，它比我们在这里展示的还要强大。您可以在高达 44 kHz 的频率下运行这个例程，就像您的 CD 播放器一样，但当然是在 8 位采样深度而不是 16 位。你将不得不满足于两个或三个声音，而不是四个，因为这样的速度真的让 Uno 内可怜的小 AVR 很累。有了更快的 CPU，你不仅可以得到 CD 质量的音频，还可以在上面进行实时信号处理。

更别提什么芯片了，比如 ADI 公司的高速 DDS 芯片，易贝只需几美元就能买到。对于正弦波，它们以非常高的速度和频率精度做着完全相同的事情。它们与在 Arduino 上用软件实现 DDS 来让狗叫相差甚远，但原理是一样的。