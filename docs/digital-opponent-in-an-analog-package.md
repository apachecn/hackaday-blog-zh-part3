# 模拟封装中的数字对手

> 原文：<https://hackaday.com/2016/07/08/digital-opponent-in-an-analog-package/>

不满足于目前国际象棋计算机的选择，更喜欢真实棋盘和棋子的感觉，[Max Dobres]决定他最好的选择是[建造自己的](http://chess.fortherapy.co.uk/home/)。

8 毫米 MDF 板上的浅色和深色木材单板创造了一个足够薄的板，可以添加 led 来显示移动，并在每个空间中添加 10 毫米 x 1 毫米的钕磁铁来触发簧片开关。LED 以矩阵形式布线，并通过 MAX7219 LED 驱动器连接到 Arduino Uno，而簧片开关通过蜈蚣卡连接。[Dobres]指出，您需要测试簧片开关的位置是否正确——否则它们可能无法检测到零件！

 [https://www.youtube.com/embed/f4WUa8H0cPo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f4WUa8H0cPo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



一个小 LCD 屏幕和四个按钮也连接到 Arduino，用于配置选项许多选项、计算机难度和游戏风格，而 Raspberry Pi 充当主计算机。

Raspberry Pi 使用棋盘 2.05 作为规则集，并考虑了特殊的移动(如顺道和阉割)。它目前不受支持，但其创作者约翰埃里克森允许使用。国际象棋程序 Stockfish 是实际的引擎；一定要调整人工智能的技能，因为它默认的 ELO 是 2600！不幸的是，这是一个相当挑剔的程序，只能在 Python 2.7 上运行。如果你对此不感兴趣，[Dobres]提供了一个其他选项的[不错的列表](http://chess.fortherapy.co.uk/home/chess-computer-links/)来帮助你构建自己的版本。

他最近[更新了他的设计](http://chess.fortherapy.co.uk/home/a-wooden-chess-computer/design-ideas-for-easy-to-build-beaglebone-black-chess-computer/),并在过程中取消了对 Arduino 的需求——特别是如果你使用 Pi Zero 的话——大大降低了这个项目的成本。这应该给你的预算留下足够的空间来建造一个机器人让[为你](https://hackaday.com/2015/03/15/lonely-build-yourself-a-chess-robot/)行动！

[via [Max Dobres](http://chess.fortherapy.co.uk/home/)