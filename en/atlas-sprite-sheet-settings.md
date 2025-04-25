---
title: Atlas / Sprite Sheet Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 12
permalink: /en/atlas-sprite-sheet-settings/
---

## Atlas / Sprite Sheet Settings (For Custom Visualizer)

*These settings control animation if the `Custom Visualizer Texture` is a sprite sheet.*

*   **Enable Animation (`_IsAnimatedTexture`)**:
    Tells the shader to treat the `Custom Visualizer Texture` as an animated sprite sheet.
*   **Animation Frame Count (`_AnimFrameCount`)**:
    The total number of frames in the animation sequence.
*   **Animation Speed (`_AnimSpeed`)**:
    Controls the playback speed of the animation.
*   **Frames Per Row / Column (`_AnimFramesPerRow`, `_AnimFramesPerColumn`)**:
    Defines the grid layout of frames within the sprite sheet texture.
*   **Frame Crop Amount (`_FrameCropAmount`)**:
    Zooms into each frame by cropping this percentage from the edges (0 to 0.25). 