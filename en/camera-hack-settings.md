---
title: Camera Hack Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 9
permalink: /en/camera-hack-settings/
---

## Camera Hack Settings

*This feature allows the shader effect (applied to an object like a quad) to display fullscreen under specific conditions (e.g., on a spectator camera view in VRChat), simulating a camera's viewfinder or screen.*

<dl>
  <dt><strong>Enable Camera Hack</strong></dt>
  <dd><code>_CameraHackEnabled</code>: Toggles the Camera Hack mode. Requires specific screen resolutions or `Bypass Resolution Check (Debug)` to be enabled. Won't activate in VR headset views.</dd>

  <dt><strong>Camera Hack Radius</strong></dt>
  <dd><code>_CameraHackRadius</code>: The maximum distance (relative to object size) the camera can be from the object for the hack to activate.</dd>

  <dt><strong>Border Size</strong></dt>
  <dd><code>_BorderSize</code>: Sets the size of the black border around the 4:3 content area when the Camera Hack is active and the `Show Information Overlay` is on.</dd>

  <dt><strong>Left Align Content</strong></dt>
  <dd><code>_LeftAlign</code>: When enabled, aligns the 4:3 content area to the left within the screen borders, instead of centering it.</dd>

  <dt><strong>Bypass Resolution Check (Debug)</strong></dt>
  <dd><code>_DisableResolutionCheck</code>: Allows the Camera Hack to activate regardless of screen resolution (useful for testing).</dd>
</dl> 