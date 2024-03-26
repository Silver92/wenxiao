---
title: Dynamic Space Detection Component
author: wen
categories: [Blogging, Demo]
tags: [Spacial Audio, Unreal, Wwise]
pin: true
math: true
mermaid: true
image:
  path: /commons/devices-mockup.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  alt: Responsive rendering of Chirpy theme on multiple devices.
---

# Dynamic Spacial Audio Component
<https://youtu.be/UcmTNhhbLqU>

This component is a new solution to implement the spatial audio effect in a dynamic space. 
It is developed as an actor component in the Unreal engine, with the API of the Wwise Unreal 
integration.

The main idea of this component is to assume that the room around the character is dynamically 
changing in volume and shape as the character keeps moving in the world. Thus, a fixed aux channel 
set in a room is not suitable for this situation. Instead, the model splits the space around the 
character into planes. It calculates the relative distance of each plane to generate a plane pattern. 
Based on the shape of the plane pattern and the approximated volume, the component will send the 
spatial data as RTPCs to the Wwise audio engine, triggering the corresponding audio parameters set 
by the designer.

With the designed plane pattern, the relative position of the character in the current space can be 
located. We can now know if the character is in the corner of the room or in the middle of the room. 
This information can help shape the details of the spatial rooms. Among the current solutions, it is 
usually assumed that all acoustic features are uniform in one fixed room. Usually, only one set of 
effects (reverb, delay, etc.) is applied to a space. Using this model, the designer can specify the 
acoustic features in different parts of the room. The additional parameters provided by the component 
can control the diffraction rate within the reverb effect, the delay panning direction if the 
character is in the corner of a large space, or the volume ratio of the aux channels.

The demo video shows an example of a dynamic spatial effect made by this solution. The voices of the 
character are sampled from the marine unit in Starcraft2. The component in the game detects the 
relative position of the main character. If the character moves close to the corner, the component 
will send parameters to the Wwise audio engine and adjust the reverb panning of the current space, 
making the corner direction less reverberant and the open direction more reflective. More detailed 
acoustic settings are still applicable to the scene.
