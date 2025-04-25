---
title: Base Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 1
permalink: /en/base-settings/
---

## Base Settings

*   **Enable Shader Effect (`_EnableRendering`)**:

    Toggles the main shader effects (first pass) on or off. When off, the object will be invisible (or transparent), but the Camera Hack overlay (second pass) may still function if enabled.
*   **Texture (`_MainTex`)**:

    The main input texture that the effects will be applied to.
*   **Resolution Width / Height (`_FixedResolutionWidth`, `_FixedResolutionHeight`)**:

    Sets the target low resolution. The input texture is effectively downscaled to these dimensions, creating the pixelated look.
*   **Is Fullscreen Effect (`_IsFullscreenEffect`)**:

    (Informational) Indicates if the shader is intended for use as a fullscreen camera effect (like a post-processing effect).
*   **Object Aspect Ratio (`_ObjectAspectRatio`)**:

    Adjusts the aspect ratio for non-square objects (like quads) when *not* using the fullscreen effect, helping to prevent stretching.
*   **Enable Color Depth Reduction (`_ColorDepthEnabled`)**:

    Turns the color reduction effect on or off.
*   **Color Depth (`_ColorDepth`)**:

    Reduces the number of available colors, simulating retro hardware limitations. Lower values mean fewer colors (more posterized look).
*   **Contrast (`_Contrast`)**:

    Adjusts the difference between light and dark areas.
*   **Brightness (`_Brightness`)**:

    Adjusts the overall lightness or darkness of the image. 