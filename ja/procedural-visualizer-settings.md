---
title: プロシージャルビジュアライザー設定
layout: default
parent: pixOcam シェーダー機能 (JA)
nav_order: 13
permalink: /ja/procedural-visualizer-settings/
---

## プロシージャルビジュアライザー設定 (UIオーバーレイのみ)

*これらは、UIオーバーレイ内の主要なプロシージャルビジュアライザー（周回する円）の外観を制御します。*

*   **軌道速度 (`_OrbitalSpeed`)**:
    主要な円がビジュアライザーボックス内でどれだけ速く周回するかを制御します。
*   **軌道幅 / 高さ (`_OrbitalWidth`, `_OrbitalHeight`)**:
    楕円軌道パスの形状とサイズを定義します。
*   **副円のサイズ (`_SecondaryCircleSize`)**:
    主要な円に対する2番目の反対側の円のサイズを制御します。
*   **副円のブレンド (`_SecondaryCircleBlend`)**:
    2番目の円の不透明度/明るさを制御します。
*   **主円の色 / 副円の色 (`_PrimaryCircleColor`, `_SecondaryCircleColor`)**:
    ビジュアライザー内の2つの周回する円の[HDR](https://docs.unity3d.com/ja/current/Manual/HDRColorPicker.html)カラーを設定します。 