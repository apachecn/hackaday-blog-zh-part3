# 软件无线电中的 TEMPEST

> 原文：<https://hackaday.com/2017/06/25/tempest-in-a-software-defined-radio/>

1985 年，[Wim van Eck]发表了几份关于获取计算机系统电磁辐射信息的技术报告。在一项分析中，[van Eck]仅使用少量组件和一台电视机，就从数百米外的计算机系统中可靠地获得了数据。存在明显的安全隐患，现在处理高度机密数据的计算机系统被 TEMPEST shielded——这是美国国家安全局防止 van Eck phreaking 的规范。

范艾克演讲的方法多得令人敬畏。[Craig Ramsay]在 Fox，它展示了一种有趣的侧信道分析新方法[，使用现成的硬件](https://www.fox-it.com/en/wp-content/uploads/sites/11/Tempest_attacks_against_AES.pdf) (PDF 警告)，包括无处不在的 RTL-SDR USB 加密狗。

本研究的实验设置包括在两块 FPGA 板上实施 AES 加密，一块 SmartFusion 2 SOC 和一块 Xilinx Pynq 板。向电路板发出运行加密程序的信号后，对各种 SDR 进行模拟测量，记录、处理并恢复密钥的每个字节。

不同测试的结果表明，只要天线与被测设备直接接触，AES 密钥就可以在任何环境下可靠地提取出来。使用聚酯薄膜太空毯制成的简易法拉第笼，可以在 30 厘米的距离内可靠地取出钥匙。在消声室中，钥匙可以在一米的距离内取出。虽然这是一个概念验证，但如果这种攻击需要直接、物理地访问设备，攻击者使用这种方法就是白痴；物理访问是根访问。

然而，这是软件定义无线电的一种新颖用途。就实验本身而言，使用更相关的旁道分析设备可以更快地获得相同的结果。[例如，ChipWhisperer】可以使用电源信号分析提取 AES 密钥。ChipWhisperer 确实需要直接接触设备，但如果替代方案在一米之外不起作用，那应该不成问题。](http://hackaday.com/2014/08/20/the-chipwhisperer-at-defcon/)