---
title: Chromatic Aberration Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 8
permalink: /en/chromatic-aberration-settings/
---

## Chromatic Aberration Settings

*   **Enable Chromatic Aberration (`_ChromaticEnabled`)**: Toggles the chromatic aberration (color fringing) effect.
*   **Chromatic Strength (`_ChromaticStrength`)**: Controls the overall amount of color separation.
*   **Chromatic Blur (`_ChromaticBlur`)**: Applies a blur to the separated colors, increasing with distance from the center when `Use Radial Distortion` is On.
*   **Use Radial Distortion (`_ChromaticRadialMode`)**: Switches between two modes:
    *   **On (Radial):** Simulates realistic lens distortion, separating colors radially from the center.
    *   **Off (Vector):** Separates colors based on fixed `Red/Green/Blue Channel Offset` vectors.
*   **Red/Green/Blue Channel Offset (`_ChromaticRedOffset`, etc.)**: (Used when `Use Radial Distortion` is Off) Defines the direction and distance each color channel is shifted. 