---
title: 基本設定
layout: default
parent: pixOcam シェーダー機能 (JA)
nav_order: 1
permalink: /ja/base-settings/
---

## 基本設定

<dl>
  <dt><strong>シェーダーエフェクト有効化</strong></dt>
  <dd><code>_EnableRendering</code>: 主要なシェーダーエフェクト（最初のパス）をオンまたはオフに切り替えます。オフの場合、オブジェクトは非表示（または透明）になりますが、カメラハックのオーバーレイ（2番目のパス）は有効であれば機能し続けます。</dd>

  <dt><strong>メインテクスチャ</strong></dt>
  <dd><code>_MainTex</code>: エフェクトが適用される主要な入力テクスチャです。</dd>

  <dt><strong>解像度 幅 / 高さ</strong></dt>
  <dd><code>_FixedResolutionWidth</code>, <code>_FixedResolutionHeight</code>: ターゲットとなる低解像度を設定します。入力テクスチャは実質的にこれらの寸法にダウンスケールされ、ピクセル化された外観を作成します。</dd>

  <dt><strong>フルスクリーンエフェクト</strong></dt>
  <dd><code>_IsFullscreenEffect</code>: (情報提供用) シェーダーがフルスクリーンのカメラエフェクト（ポストプロセスエフェクトのようなもの）として使用されることを意図しているかどうかを示します。</dd>

  <dt><strong>オブジェクトアスペクト比</strong></dt>
  <dd><code>_ObjectAspectRatio</code>: フルスクリーンエフェクトを使用しない場合に、正方形でないオブジェクト（クアッドなど）のアスペクト比を調整し、引き伸ばしを防ぎます。</dd>

  <dt><strong>色深度削減有効化</strong></dt>
  <dd><code>_ColorDepthEnabled</code>: 色削減エフェクトをオンまたはオフにします。</dd>

  <dt><strong>色深度</strong></dt>
  <dd><code>_ColorDepth</code>: 利用可能な色数を減らし、レトロなハードウェアの制限をシミュレートします。値が低いほど色数が少なくなります（よりポスタライズされた見た目になります）。</dd>

  <dt><strong>コントラスト</strong></dt>
  <dd><code>_Contrast</code>: 明るい領域と暗い領域の差を調整します。</dd>

  <dt><strong>明るさ</strong></dt>
  <dd><code>_Brightness</code>: 画像全体の明るさまたは暗さを調整します。</dd>
</dl> 