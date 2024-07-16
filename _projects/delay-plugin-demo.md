---
title: Audio Delay Plugin Demo
author: wen
description: A VST audio plugin working on the digital audio workstations (DAW) on the windows platform. The plugin supports two types of delay time alignment which is able to convert to the other, helping the designer conviniently estamate the exact delay time and improve the proficiency in the post-production pipeline.
categories: [Project]
tags: [Dafx, Audio Signal Processing]
pin: true
---

{% include embed/youtube.html id='MWt1lQPuHfc' %}

An audio delay effect plugin is demostrated to improve the music and sound design experience. The delay effect is used to simulate the echo in the common space and enchance the sound effect. 5 sliders and 1 button are designed in this plugin:

Input:		A parameter to adjust the input signal level in dBFS.

Time:		A parameter to adjust the delay time for the delay signal.

Time/Beat Mode Button:  A button to align the delay time to the exact beat time or to turn the beat time to continuous time value

Feedback: 	A parameter to adjust the damping factor of the delay signal.

Dry/Wet: 	A parameter to adjust the dry/wet ratio of the output signal.

Output: 		A parameter to adjust the output signal level in dBFS.

The users adjust the parameters above to achieve the ideal soundscape for their sounds. In the time mode, the delay time parameter will be displayed as a time slider. The users adjust the delay time by modifing the slider knob to get the exact time they want. Three operations on the knob are supported. You can click to the knob then drag up and down or drag left and right, and even put the mouse on the knob and scroll the middle wheel. Each way will adjust the delay time value. Also, if the users click the time number above the knob, a text field will pop up to let the users input the delay time. And the users can just double click the knob to set the parameter to the default value.

{% include embed/youtube.html id='dQFpaYoQhg4' %}

{% include embed/youtube.html id='T9eBsL7SM2Y' %}

As the plugin is switched to the beat mode, the knob of the time becomes descrete in rhythm. The plugin will get the current BPM in the host and convert the delay time to the exact beat pattern. The users can easily drag or scroll the knob to choose the beat pattern they like.

{% include embed/youtube.html id='AIrypINn6Zs' %}

A practical feature deserved to mention is the Time/Beat Switch feature. The Time/Beat mode button provides the designer an easy way to test the delay time they want and quickly align the time to the beat by a simple click. The button saves the time to calculate the beat when the delay sound needs to follow some rhythm patterns. The users can also create some special rhythm patterns with the delay plugin, which creates some special sound effects patterns especially in some rhythm samples such as the drum beats.

Github: [https://github.com/Silver92/Delay-Audio-Plugin-Demo.git](https://github.com/Silver92/Delay-Audio-Plugin-Demo.git)