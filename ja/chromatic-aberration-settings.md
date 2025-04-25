---
title: 色収差設定
layout: default
parent: pixOcam シェーダー機能 (JA)
nav_order: 8
permalink: /ja/chromatic-aberration-settings/
---

## 色収差設定

<dl>
  <dt><strong>色収差有効化</strong></dt>
  <dd><code>_ChromaticEnabled</code>: 色収差（カラーフリンジ）エフェクトを切り替えます。</dd>

  <dt><strong>色収差強度</strong></dt>
  <dd><code>_ChromaticStrength</code>: 色分離の全体的な量を制御します。</dd>

  <dt><strong>エッジぼかし量</strong></dt>
  <dd><code>_ChromaticBlur</code>: 分離された色にぼかしを適用します。`リアルレンズモデル使用 / Use Radial Distortion`がオンの場合、中心からの距離に応じて増加します。</dd>

  <dt><strong>リアルレンズモデル使用</strong></dt>
  <dd><code>_ChromaticRadialMode</code>: 2つのモードを切り替えます:
    <ul>
      <li><strong>オン (放射状):</strong> リアルなレンズ歪みをシミュレートし、中心から放射状に色を分離します。</li>
      <li><strong>オフ (ベクトル):</strong> 固定された`赤/緑/青チャンネルオフセット`ベクトルに基づいて色を分離します。</li>
    </ul>
  </dd>

  <dt><strong>赤/緑/青チャンネルオフセット</strong></dt>
  <dd><code>_ChromaticRedOffset</code>, etc.: (`リアルレンズモデル使用 / Use Radial Distortion`がオフの場合に使用) 各カラーチャンネルがシフトされる方向と距離を定義します。</dd>
</dl> 