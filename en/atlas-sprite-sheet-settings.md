---
title: Atlas / Sprite Sheet Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 12
permalink: /en/atlas-sprite-sheet-settings/
---

## Atlas / Sprite Sheet Settings (For Custom Visualizer)

*These settings control animation if the `Custom Visualizer Texture` is a sprite sheet.*

<dl>
  <dt><strong>Enable Animation</strong></dt>
  <dd><code>_IsAnimatedTexture</code>: Tells the shader to treat the `Custom Visualizer Texture` as an animated sprite sheet.</dd>

  <dt><strong>Animation Frame Count</strong></dt>
  <dd><code>_AnimFrameCount</code>: The total number of frames in the animation sequence.</dd>

  <dt><strong>Animation Speed</strong></dt>
  <dd><code>_AnimSpeed</code>: Controls the playback speed of the animation.</dd>

  <dt><strong>Frames Per Row / Column</strong></dt>
  <dd><code>_AnimFramesPerRow</code>, <code>_AnimFramesPerColumn</code>: Defines the grid layout of frames within the sprite sheet texture.</dd>

  <dt><strong>Frame Crop Amount</strong></dt>
  <dd><code>_FrameCropAmount</code>: Zooms into each frame by cropping this percentage from the edges (0 to 0.25).</dd>
</dl> 