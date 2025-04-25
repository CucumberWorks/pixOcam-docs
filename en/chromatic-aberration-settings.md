---
title: Chromatic Aberration Settings
layout: default
parent: pixOcam Shader Features (EN)
nav_order: 8
permalink: /en/chromatic-aberration-settings/
---

## Chromatic Aberration Settings

<dl>
  <dt><strong>Enable Chromatic Aberration</strong></dt>
  <dd><code>_ChromaticEnabled</code>: Toggles the chromatic aberration (color fringing) effect.</dd>

  <dt><strong>Chromatic Strength</strong></dt>
  <dd><code>_ChromaticStrength</code>: Controls the overall amount of color separation.</dd>

  <dt><strong>Chromatic Blur</strong></dt>
  <dd><code>_ChromaticBlur</code>: Applies a blur to the separated colors, increasing with distance from the center when `Use Radial Distortion` is On.</dd>

  <dt><strong>Use Radial Distortion</strong></dt>
  <dd><code>_ChromaticRadialMode</code>: Switches between two modes:
    <ul>
      <li><strong>On (Radial):</strong> Simulates realistic lens distortion, separating colors radially from the center.</li>
      <li><strong>Off (Vector):</strong> Separates colors based on fixed `Red/Green/Blue Channel Offset` vectors.</li>
    </ul>
  </dd>

  <dt><strong>Red/Green/Blue Channel Offset</strong></dt>
  <dd><code>_ChromaticRedOffset</code>, etc.: (Used when `Use Radial Distortion` is Off) Defines the direction and distance each color channel is shifted.</dd>
</dl> 