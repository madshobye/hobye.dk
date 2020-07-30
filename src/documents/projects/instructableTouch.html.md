---
title: 'Touch Interface with Arduino'
layout: 'post'
tags: ['instructable','touch']
date: '2012-06-01'
picture: 'https://lh4.googleusercontent.com/-vH-tuKFfvCE/T9JjU1t2sPI/AAAAAAAAHdE/HFTGqW2MCNE/s603/Screen+Shot+2012-05-30+at+13.36.22.png'
abstract: 'At CHI 2012, I was introduced to the Touché interface. Touché is a new sensing technology that can not only detect a touch event, but simultaneously recognize complex configurations of the human hands and body during touch interaction. Developed by Disney Research Lab, Touché significantly enhances touch interaction in a broad range of applications, from enhancing conventional touchscreens to designing interaction scenarios for unique use contexts and materials. For example, you can add complex touch and gesture sensitivity not only to computing devices and everyday objects, but also to the human body and liquids. I asked my friend DZL if he could design a version that worked on the Arduino platform.'
publisher: 'Instructables'
---

<iframe src="http://player.vimeo.com/video/43106290" width="620" height="348" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

I had the honor to meet them at CHI2012 in Texas and I discussed with them whether it would be possible to convert their system into the Arduino platform. Their immediate reaction was that the Arduino would not be able to generate good enough frequencies. I asked my friend DZL if he could solve this problem and this was his solution to the problem:

*The Touché hardware uses a really fancy Direct Digital Synthesizer IC from Analog Devices. It generates a really pure sine wave signal with frequencies between 1kHz and 3.5MHz with high resolution. While the Arduino is capable of generating frequencies in this range the signal is a square wave with lots of harmonic frequency components and really low frequency resolution.*

*Simply using this signal with the circuit described in the Touché paper result in a really messy frequency graph due to the harmonics from the square wave. The solution is to use the filtering properties of the LC circuit to our advantage. By measuring the signal after the inductor (coil) rather than before we only see a nice sine wave shaped signal free of all the unwanted frequency components. As a result we now see a peak in signal at resonance rather than a notch but the signal contains the same information.*

With DZL’s permission, the solution has been packaged as an instructable that can be found [here](http://www.instructables.com/id/Touche-for-Arduino-Advanced-touch-sensing/). I have made a simple graphing sketch that enables you to see the data and also do simple gesture recognition. Further, the instructable contains a step-by-step guide on how to build the circuit and upload the code. The only special components is a coil that can be made out of wire wrapped around a toilet paper roll.

**Links**
* [Instructable](http://www.instructables.com/id/Touche-for-Arduino-Advanced-touch-sensing/)
* [DZL](http://dzlsevilgeniuslair.blogspot.dk/2012/05/arduino-do-touche-dance.html)
* [Medea story](http://medea.mah.se/2012/05/diy-use-any-surface-as-a-touch-interface/)
