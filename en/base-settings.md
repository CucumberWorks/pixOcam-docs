---
title: Base Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 1
permalink: /en/base-settings/
---

## Base Settings

<dl>
  <dt><strong>Enable Shader Effect (`_EnableRendering`)</strong></dt>
  <dd>Toggles the main shader effects (first pass) on or off. When off, the object will be invisible (or transparent), but the Camera Hack overlay (second pass) may still function if enabled.</dd>

  <dt><strong>Texture (`_MainTex`)</strong></dt>
  <dd>The main input texture that the effects will be applied to.</dd>

  <dt><strong>Resolution Width / Height (`_FixedResolutionWidth`, `_FixedResolutionHeight`)</strong></dt>
  <dd>Sets the target low resolution. The input texture is effectively downscaled to these dimensions, creating the pixelated look.</dd>

  <dt><strong>Is Fullscreen Effect (`_IsFullscreenEffect`)</strong></dt>
  <dd>(Informational) Indicates if the shader is intended for use as a fullscreen camera effect (like a post-processing effect).</dd>

  <dt><strong>Object Aspect Ratio (`_ObjectAspectRatio`)</strong></dt>
  <dd>Adjusts the aspect ratio for non-square objects (like quads) when *not* using the fullscreen effect, helping to prevent stretching.</dd>

  <dt><strong>Enable Color Depth Reduction (`_ColorDepthEnabled`)</strong></dt>
  <dd>Turns the color reduction effect on or off.</dd>

  <dt><strong>Color Depth (`_ColorDepth`)</strong></dt>
  <dd>Reduces the number of available colors, simulating retro hardware limitations. Lower values mean fewer colors (more posterized look).</dd>

  <dt><strong>Contrast (`_Contrast`)</strong></dt>
  <dd>Adjusts the difference between light and dark areas.</dd>

  <dt><strong>Brightness (`_Brightness`)</strong></dt>
  <dd>Adjusts the overall lightness or darkness of the image.</dd>
</dl> 