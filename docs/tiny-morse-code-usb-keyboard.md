# 微型莫尔斯电码 USB 键盘

> 原文：<https://hackaday.com/2017/01/25/tiny-morse-code-usb-keyboard/>

过去，我们在这里展示了不少[mitxela]的项目，其中许多都有被贴上“最小”标签的倾向。他的[莫尔斯电码 USB 键盘 Mk II](https://mitxela.com/projects/morse_code_usb_keyboard_mk_ii) 增加了这个列表。这是一个周六下午的项目，几个零件被粘在一块 perf-board 上，允许使用莫尔斯键作为 USB 键盘。这个项目不是新的或新鲜的，但我们在试图找出作者的零件箱中莫尔斯键的用途时偶然发现了它。你可以通过阅读文本并在键盘上键入来练习传输，然后在电脑上查找，看看是否有错误。或者你可以通过让朋友帮你打卡来练习接收。无论哪种方式，这都是磨练技能和准备无线电操作员执照考试的好方法。

该项目是他早期项目的后续，在早期项目中，他通过 RS-232-USB 转换器将莫尔斯键直接连接到计算机，并让代码完成所有工作。这被证明是一个非常耗费资源、不切实际的项目，并让他在下一次做对了。硬件非常简单。一个 ATtiny85、一个压电蜂鸣器、一些去耦电容以及一些电阻和齐纳二极管，以实现安全的 USB 接口。该设计提供了一个直键，但在 ATtiny 中还留有一个备用引脚，以支持抑扬格键或侧滑键。没有调速，目前是硬编码的。这对于用户来说不是很友好，而且[mitxela]建议在 ATtiny 的最后一个引脚上增加一个速度电位计。这将阻止使用抑扬格/侧扫键。或者，你可以[使用 ATtiny 上的 RST 引脚作为(弱)IO](http://www.technoblogy.com/show?LSE) 。RST 引脚可以读取 5V 至 2.5V 之间的模拟值，并在电压低于 2.2V 时复位。或者只使用另一个微控制器作为最后手段。

对于 USB 接口，[mitxela]在浪费了一些时间试图重新发明轮子之后，正在使用 [V-USB 库](https://www.obdev.at/products/vusb/index.html)。由于它是作为 HID 设计的，所以不需要任何驱动程序——插上电源，操作系统会将其检测为键盘。他借用了 [EasyLogger](https://www.obdev.at/products/vusb/easylogger.html) 项目的代码来使用内部振荡器，帮助释放 IO 管脚。为了检测输入的字符，他的代码使用了一长串比较语句，而不是字典查找。编写这段代码很繁琐，但它使识别更快，因为大多数字符可以在不到五次的比较中被识别出来(一次 dit = E，两次 dits = I，三次 dits = S，依此类推)。这个“[树](https://upload.wikimedia.org/wikipedia/commons/c/ca/Morse_code_tree3.png)”更容易弄清楚。

如果你想看看他的其他一些“小”项目，再看看最小的 MIDI 合成器、[最小的 MIDI 合成器！](http://hackaday.com/2016/05/08/smallest-midi-synth-again/)和[阿蒂尼 MIDI 插头合成器](http://hackaday.com/2016/03/30/the-attiny-midi-plug-synth/)。

 [https://www.youtube.com/embed/tUNjKQWjo80?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tUNjKQWjo80?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

