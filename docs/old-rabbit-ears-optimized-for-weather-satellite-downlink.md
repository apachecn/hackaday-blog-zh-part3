# 老兔耳优化气象卫星下行

> 原文：<https://hackaday.com/2017/07/10/old-rabbit-ears-optimized-for-weather-satellite-downlink/>

与卫星通信似乎需要很多设备。一个花哨的天线和装满接收器、滤波器和放大器的机架似乎是入门级的装备。但是戴着一副旧兔子耳朵和 SDR 转换器听气象卫星？那也是个事儿。

曾经有一段时间，每台新电视都配有一对兔子耳朵。那些日子已经一去不复返了，但是[Thomas Cholakov (N1SPY)]设法在他的车库里找到了一个旧的电视偶极子，配有 300 欧姆的双线和扁平连接器。他把它配置成水平的 V 形偶极子排列，在 137 MHz 上监听 NOAA 气象卫星。天线分支大约分开 120°，每个调整到大约 20.5 英寸(52 厘米)长。长度使天线在正确的频率下谐振，v 形使辐射模式接近圆形，水平极化排除了附近 FM 广播波段的信号，并将模式指向天空。[Thomas]没有提到他如何将天线阻抗与 SDR 匹配，但在下面的视频中似乎有某种巴伦。卫星信号被解码并实时显示，结果令人惊讶地好。

跃跃欲试想听卫星但没有兔子耳朵？没问题——去找[一个烹饪锅](http://hackaday.com/2017/06/19/an-antenna-that-really-cooks-really/)然后开始做。

 [https://www.youtube.com/embed/5ulef0a8OSQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5ulef0a8OSQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

