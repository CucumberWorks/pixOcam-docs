---
title: Base Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 1
permalink: /en/base-settings/
---

## Base Settings

<dl>
  <dt><strong>Enable Shader Effect</strong></dt>
  <dd><code>_EnableRendering</code>: Toggles the main shader effects (first pass) on or off. When off, the object will be invisible (or transparent), but the Camera Hack overlay (second pass) may still function if enabled.</dd>

  <dt><strong>Texture</strong></dt>
  <dd><code>_MainTex</code>: The main input texture that the effects will be applied to.</dd>

  <dt><strong>Resolution Width / Height</strong></dt>
  <dd><code>_FixedResolutionWidth</code>, <code>_FixedResolutionHeight</code>: Sets the target low resolution. The input texture is effectively downscaled to these dimensions, creating the pixelated look.</dd>

  <dt><strong>Is Fullscreen Effect</strong></dt>
  <dd><code>_IsFullscreenEffect</code>: (Informational) Indicates if the shader is intended for use as a fullscreen camera effect (like a post-processing effect).</dd>

  <dt><strong>Object Aspect Ratio</strong></dt>
  <dd><code>_ObjectAspectRatio</code>: Adjusts the aspect ratio for non-square objects (like quads) when *not* using the fullscreen effect, helping to prevent stretching.</dd>

  <dt><strong>Enable Color Depth Reduction</strong></dt>
  <dd><code>_ColorDepthEnabled</code>: Turns the color reduction effect on or off.</dd>

  <dt><strong>Color Depth</strong></dt>
  <dd><code>_ColorDepth</code>: Reduces the number of available colors, simulating retro hardware limitations. Lower values mean fewer colors (more posterized look).</dd>

  <dt><strong>Contrast</strong></dt>
  <dd><code>_Contrast</code>: Adjusts the difference between light and dark areas.</dd>

  <dt><strong>Brightness</strong></dt>
  <dd><code>_Brightness</code>: Adjusts the overall lightness or darkness of the image.</dd>
</dl> 