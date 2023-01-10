# 动画进度条显示液晶显示器的新花样

> 原文：<https://hackaday.com/2016/08/06/animated-progress-bar-tricks-arduino/>

A small LCD screen can be extremely helpful with small microcontroller projects. Not everything needs to communicate to a fancy server using an ESP8266\. However, if the simplicity of the character displays irks you, it’s possible to spice them up a little bit with custom characters and create animations, like [Fabien] did with his [animated Arduino progress bar](https://www.carnetdumaker.net/articles/faire-une-barre-de-progression-avec-arduino-et-liquidcrystal/). ([Google Translate from French](https://translate.google.com/translate?hl=fr&sl=fr&tl=en&u=https%3A%2F%2Fwww.carnetdumaker.net%2Farticles%2Ffaire-une-barre-de-progression-avec-arduino-et-liquidcrystal%2F))The project started out simply enough: all [Fabien] needed was a progress bar. It’s easy enough to fill in the “characters” on the 2×16 character LCD screen one-by-one to indicate progress, and the first version of this did exactly that. The second version got a little bit fancier by adding a border around the progress bar and doubling its resolution, but the third version is where knowing the inner machinations of the microcontroller really paid off. Using a custom charset reuse optimization, [Fabien] was able to use 19 custom characters at a time when the display will normally only allow for eight. This was accomplished by placing the custom characters in memory in the correct order, to essentially trick the microcontroller into displaying them.These types of microcontroller hacks get deep into the inner workings of the microcontroller and help expose some tricks that we can all use to understand their operation on a deeper level. Whether you’re [using PWM to get a microcontroller to operate a TV](https://hackaday.com/2016/07/08/cute-usart-trick-brings-pwm-to-ir-leds/), or creating the [ATtiny-est MIDI synth](https://hackaday.com/2016/05/08/smallest-midi-synth-again/), these tricks are crucial to getting exactly what you want out of a small, inexpensive microcontroller.