---
title: Wwise Auto Switch Assignment Plugin
author: wen
categories: [Project]
tags: [Wwise]
pin: true
math: true
mermaid: true
---

{% include embed/youtube.html id='mUuQFkw_r5c' %}

The gadget is developed to allow audio designers to quickly assign switch units to their parent switch 
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
