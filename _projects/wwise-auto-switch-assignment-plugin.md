---
title: Wwise Auto Switch Assignment Plugin
author: wen
categories: [Blogging, Demo]
tags: [Wwise]
pin: true
math: true
mermaid: true
image:
  path: /commons/devices-mockup.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  alt: Responsive rendering of Chirpy theme on multiple devices.
---

# Wwise Auto Switch Assignment Plugin
<https://youtu.be/mUuQFkw_r5c>

This tool is developed to allow audio designers to quickly assign switch units to their parent switch 
containers according to a defined rule. The plugin is developed with the JUCE framework and WAAPI, 
and users can install it directly into the Wwise editor.

Usually in Wwise, a designer has to drag the switch units to the switches one by one, which is 
time-consuming when a large number of switches need to be integrated. With the plugin, users can 
select multiple switch containers at the same time, assign them to a switch/state group (the plugin 
will automatically collect all the switch/state groups in the project), and automatically assign their 
child containers to each switch based on a specific rule. In this demo video, the matching rule is to 
let the middle word or suffix of the child switch container match the switch name. Other matching rules
are still welcome to be applied to the plugin.

The plugin holds the design idea of "partial automation", providing flexibility to the integrators 
and allowing them to customize the operating unit. It simplifies the integration process with just a 
few clicks on the designed UI and adapts to common situations when users need to make switch 
assignments. No matter how many switch containers with different types of switches need to be handled, 
or even if there are nested switch structures to deal with, the plugin makes the integration process 
much easier.
