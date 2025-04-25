---
title: カラーパレット
layout: default
parent: pixOcam シェーダー機能 (JA)
nav_order: 3
permalink: /ja/color-settings/
---

## カラーパレット

<dl>
  <dt><strong>カラーパレット有効化</strong></dt>
  <dd><code>_PaletteEnabled</code>: カラーリマッピングエフェクトを切り替えます。</dd>

  <dt><strong>グラデーションテクスチャ 1-6</strong></dt>
  <dd><code>_GradientTex1</code> ～ <code>_GradientTex6</code>: グラデーションテクスチャ（LUT）用のテクスチャスロットです。シェーダーは`グラデーションプリセット`で選択されたものを使用します。</dd>

  <dt><strong>パレット段階数</strong></dt>
  <dd><code>_PaletteSteps</code>: グラデーションテクスチャからサンプリングされる個別の色数を減らします。よりバンディングされた見た目を作成します。</dd>

  <dt><strong>パレット混合</strong></dt>
  <dd><code>_PaletteBlend</code>: 元の画像の色（0）とリマップされたパレットの色（1）の間でブレンドします。</dd>

  <dt><strong>グラデーションプリセット</strong></dt>
  <dd><code>_GradientPreset</code>: エフェクトに使用する`カラーパレット`グラデーションテクスチャ（1～6）を選択します。</dd>
</dl> 