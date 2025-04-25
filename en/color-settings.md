---
title: Color Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 3
permalink: /en/color-settings/
---

## Color Settings

<dl>
  <dt><strong>Use Color Palette</strong></dt>
  <dd><code>_PaletteEnabled</code>: Toggles the color remapping effect.</dd>

  <dt><strong>Color Palette 1-6</strong></dt>
  <dd><code>_GradientTex1</code> to <code>_GradientTex6</code>: Texture slots for gradient textures (LUTs). The shader uses the one selected by `Gradient Preset`.</dd>

  <dt><strong>Palette Steps</strong></dt>
  <dd><code>_PaletteSteps</code>: Reduces the number of distinct colors sampled from the gradient texture. Creates a more banded look.</dd>

  <dt><strong>Palette Blend</strong></dt>
  <dd><code>_PaletteBlend</code>: Blends between the original image colors (0) and the remapped palette colors (1).</dd>

  <dt><strong>Gradient Preset</strong></dt>
  <dd><code>_GradientPreset</code>: Selects which `Color Palette` gradient texture (1-6) to use for the effect.</dd>
</dl> 