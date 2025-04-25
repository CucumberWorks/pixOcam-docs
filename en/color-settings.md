---
title: Color Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 3
permalink: /en/color-settings/
---

## Color Settings

*   **Use Color Palette (`_PaletteEnabled`)**:
    Toggles the color remapping effect.
*   **Color Palette 1-6 (`_GradientTex1` to `_GradientTex6`)**:
    Texture slots for gradient textures (LUTs). The shader uses the one selected by `Gradient Preset`.
*   **Palette Steps (`_PaletteSteps`)**:
    Reduces the number of distinct colors sampled from the gradient texture. Creates a more banded look.
*   **Palette Blend (`_PaletteBlend`)**:
    Blends between the original image colors (0) and the remapped palette colors (1).
*   **Gradient Preset (`_GradientPreset`)**:
    Selects which `Color Palette` gradient texture (1-6) to use for the effect. 