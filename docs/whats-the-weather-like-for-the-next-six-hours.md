# 接下来的六个小时天气怎么样？

> 原文：<https://hackaday.com/2016/05/04/whats-the-weather-like-for-the-next-six-hours/>

自从我们意识到我们有了从算命师的帐篷里拿出来的技术后，可以预测未来的魔法发光球体就一直是一个很受欢迎的东西。我们非常喜欢[jarek319]对这个概念的解释。

神秘地坐在他的伞架上方，一根黑色的绳子提供了算命所需的精灵，一个白色的立方体播放了一个动画，模拟接下来六个小时的室外天气。如果他看到有水滴落下，他知道在离开家之前要带一把伞。如果他看到雷雨，他知道拿起玻璃纤维伞芯的伞，以防止富兰克林先生早期工作的亲密重复。
 这个项目的核心是一块某种描述的 ESP8226 项目板。led 是 WS2812B 可单独寻址的 led 矩阵。他将它编程为 ping [OpenWeather](http://openweathermap.org/api) 并获取当前状态。之后，他开始为显示器编写循环动画。

这个箱子是一个盒子，顶部有一层白色丙烯酸树脂。丙烯酸很好地扩散了 led，在休息后的视频中看起来真的很好。

 [https://www.youtube.com/embed/2kd0L9-TXOY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2kd0L9-TXOY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

