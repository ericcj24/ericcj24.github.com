---
layout: post
title: "Spectrogram on Android"
tags: [Android,DSP,signal processing]
author_name: CJ
author_uri: ericcj24.github.io
---

A spectrogram could display several qualities of sound in a graphical
way. It could map out the frequency of the sound component, color-code
its intensity at each frequency.

As part of my Embedded DSP lab, we built this spectrogram program on
Android platform. It records the sound, use [Android NDK
package](http://developer.android.com/tools/sdk/ndk/index.html) to embed
C code into Android program to process the sound with Fourier Transform
and outputs its spectrogram.

![](/images/posts/2013-07-03/spectrogram.png)

<p align="center">
pic 1

</p>
pic 1 shows the spectrogram of human voice, with different harmonics and
intensity at each harmonic

The program’s sampling frequency is set at 8000Hz, thus it could detect
highest frequency of 4000Hz without aliasing.

This is part of the Embedded Digital Signal Processing (DSP) lab, the
code of this program could be found
[here](https://github.com/ericcj24/Spectrogram-DSP-Android-App)
