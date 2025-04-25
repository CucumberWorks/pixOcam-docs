---
title: Camera Hack Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 9
permalink: /en/camera-hack-settings/
---

## Camera Hack Settings

*This feature allows the shader effect (applied to an object like a quad) to display fullscreen under specific conditions (e.g., on a spectator camera view in VRChat), simulating a camera's viewfinder or screen.*

*   **Enable Camera Hack (`_CameraHackEnabled`)**:
    Toggles the Camera Hack mode. Requires specific screen resolutions or `Bypass Resolution Check (Debug)` to be enabled. Won't activate in VR headset views.
*   **Camera Hack Radius (`_CameraHackRadius`)**:
    The maximum distance (relative to object size) the camera can be from the object for the hack to activate.
*   **Border Size (`_BorderSize`)**:
    Sets the size of the black border around the 4:3 content area when the Camera Hack is active and the `Show Information Overlay` is on.
*   **Left Align Content (`_LeftAlign`)**:
    When enabled, aligns the 4:3 content area to the left within the screen borders, instead of centering it.
*   **Bypass Resolution Check (Debug) (`_DisableResolutionCheck`)**:
    Allows the Camera Hack to activate regardless of screen resolution (useful for testing). 