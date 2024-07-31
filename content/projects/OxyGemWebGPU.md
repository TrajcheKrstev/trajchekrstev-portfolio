+++
title = 'OxyGem - WebGPU'
draft = false
featured_image = "/images/OxyGemWebGPU.png"
summary = "**OxyGem** is an immersive game developed as part of a group project for the **Computer Graphics and Game Technology** course. In this game, you play as a researcher stranded in an underwater cave with limited oxygen. Your mission is to locate and collect magic gems scattered throughout the cave to activate a portal and escape before your oxygen runs out."
+++

**OxyGem** is an immersive game developed as part of a group project for the **Computer Graphics and Game Technology** course. In this game, you play as a researcher stranded in an underwater cave with limited oxygen. Your mission is to locate and collect magic gems scattered throughout the cave to activate a portal and escape before your oxygen runs out.

## Project Overview

### Gameplay

- **Objective**: Find and collect hidden magic gems to activate a portal for escape.
- **Challenge**: Manage your limited oxygen supply and navigate through the cave efficiently.

### Key Features

- **Game Engine**: Utilized a game engine provided by the course organizers as a foundation. All game logic was implemented in **JavaScript**.
- **Graphics**: Employed **WebGPU Shading Language** for advanced lighting, fog, and underwater effects, as well as model geometry.
- **User Interface**: Developed using **HTML** and **CSS** to create a responsive and intuitive interface.
- **3D Modeling**: Designed custom 3D models and scenes using **Blender**.

### Technical Details

The game leverages a variety of technologies and methodologies to deliver an engaging experience:

1. **Game Logic**: The core gameplay mechanics, including player movement, gem collection, and oxygen management, are implemented in JavaScript. This includes setting up event listeners for user interactions and updating the game state based on player actions and elapsed time.

2. **Graphics and Effects**: Advanced graphical effects such as lighting, fog, and underwater visuals are created using WebGPU Shading Language. These effects enhance the visual realism of the game and provide a more immersive experience.

3. **3D Models and Scenes**: All 3D models and the game environment were crafted in Blender. These models were then integrated into the game engine, allowing for dynamic interactions and animations within the game world.

4. **User Interface**: The game's user interface is built with HTML and CSS, ensuring a clean and user-friendly design. This includes elements like the oxygen meter, gem icons, and various modals for game instructions, win/lose conditions, and more.

5. **Audio Integration**: Background music and sound effects are integrated to enhance the gaming experience. This includes audio for gem collection, bubble pops, and other in-game events, creating a more engaging atmosphere.

### Core Implementation Snippets

- **Player Movement and Camera Control**: Implemented using a ThirdPersonController, which manages the camera's position relative to the player and handles input for movement.
- **Gem and Bubble Collection**: Logic for detecting and responding to player interactions with gems and bubbles, including updating the game state and triggering audio cues.
- **Radar System**: A custom radar system helps players locate gems within the cave, translating world coordinates to radar screen positions.

## Video Demonstration

{{<video src="videos/RGTI.mp4" type="video/mp4" preload="auto" >}}
