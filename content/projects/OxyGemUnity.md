+++
title = 'OxyGem - Unity'
draft = false
featured_image = "/images/OxyGemUnity.png"
summary = "**OxyGem - Unity** is an upgraded version of the original OxyGem - WebGPU, rebuilt using the powerful **Unity Game Engine**. This enhanced version maintains the core gameplay while leveraging Unity's extensive features to deliver a more refined and immersive experience."
+++

**OxyGem - Unity** is an upgraded version of the original [OxyGem - WebGPU]({{< ref "oxygemwebgpu" >}}), rebuilt using the powerful **Unity Game Engine**. This enhanced version maintains the core gameplay while leveraging Unity's extensive features to deliver a more refined and immersive experience.

## Project Overview

### Key Enhancements

- **Game Logic**: Rewritten entirely in **C#** to take full advantage of Unity's capabilities.
- **Shader Effects**: Utilized the **Shader Graph Unity Package** for creating advanced visual effects, such as the portal swirl effect and volumetric lighting.
- **Post Processing**: Implemented the **Post Processing Unity Package** to add a Low Oxygen Alert, enhancing the player's sense of urgency.
- **Movement System**: Employed the **Input System Unity Package** for smooth and responsive control of the submarine.
- **Underwater Effects**: Designed custom underwater effects using a **Unity Shader**, contributing to the game's atmospheric depth.

### Technical Details

1. **Game Logic in C#**: The game's core mechanics, including player movement, gem collection, and oxygen management, were developed using C#, enabling efficient and robust code management within Unity.

2. **Shader Graph for Visual Effects**: The Shader Graph was used to create complex visual effects. This included the portal's swirling animation and realistic volumetric lighting, which significantly enhance the visual appeal and immersion of the game.

3. **Post Processing for Alerts**: The Post Processing package allowed us to introduce a Low Oxygen Alert effect, which visually cues the player about their depleting oxygen levels, adding to the game's tension and urgency.

4. **Input System for Controls**: Unity's Input System package was implemented to handle player inputs, providing smooth and precise control over the submarine, making the gameplay experience more intuitive and engaging.

5. **Custom Underwater Shaders**: To achieve realistic underwater effects, we created custom shaders within Unity. These shaders simulate underwater light scattering and distortion, contributing to the overall immersive environment of the game.

### Video Demonstration

{{<video src="videos/RGTI2.mp4" type="video/mp4" preload="auto" >}}
