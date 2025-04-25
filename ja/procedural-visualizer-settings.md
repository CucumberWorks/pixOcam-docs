---
title: プロシージャルビジュアライザー設定
layout: default
parent: pixOcam シェーダー機能 (JA)
nav_order: 13
permalink: /ja/procedural-visualizer-settings/
---

## プロシージャルビジュアライザー設定 (UIオーバーレイのみ)

*これらは、UIオーバーレイ内の主要なプロシージャルビジュアライザー（周回する円）の外観を制御します。*

<dl>
  <dt><strong>軌道速度</strong></dt>
  <dd><code>_OrbitalSpeed</code>: 主要な円がビジュアライザーボックス内でどれだけ速く周回するかを制御します。</dd>

  <dt><strong>軌道幅 / 高さ</strong></dt>
  <dd><code>_OrbitalWidth</code>, <code>_OrbitalHeight</code>: 楕円軌道パスの形状とサイズを定義します。</dd>

  <dt><strong>副円のサイズ</strong></dt>
  <dd><code>_SecondaryCircleSize</code>: 主要な円に対する2番目の反対側の円のサイズを制御します。</dd>

  <dt><strong>副円のブレンド</strong></dt>
  <dd><code>_SecondaryCircleBlend</code>: 2番目の円の不透明度/明るさを制御します。</dd>

  <dt><strong>主円の色 / 副円の色</strong></dt>
  <dd><code>_PrimaryCircleColor</code>, <code>_SecondaryCircleColor</code>: ビジュアライザー内の2つの周回する円の[HDR](https://docs.unity3d.com/ja/current/Manual/HDRColorPicker.html)カラーを設定します。</dd>
</dl> 