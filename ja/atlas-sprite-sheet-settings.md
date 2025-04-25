---
title: アトラス / スプライトシート設定
layout: default
parent: pixOcam シェーダー機能 (JA)
nav_order: 12
permalink: /ja/atlas-sprite-sheet-settings/
---

## アトラス / スプライトシート設定 (カスタムビジュアライザー用)

*これらの設定は、`カスタムテクスチャ`がスプライトシートの場合のアニメーションを制御します。*

<dl>
  <dt><strong>アニメーション有効化</strong></dt>
  <dd><code>_IsAnimatedTexture</code>: シェーダーに`カスタムテクスチャ`をアニメーション化されたスプライトシートとして扱うように指示します。</dd>

  <dt><strong>総フレーム数</strong></dt>
  <dd><code>_AnimFrameCount</code>: アニメーションシーケンス内の総フレーム数。</dd>

  <dt><strong>アニメーション速度</strong></dt>
  <dd><code>_AnimSpeed</code>: アニメーションの再生速度を制御します。</dd>

  <dt><strong>行あたりフレーム数 / 列あたりフレーム数</strong></dt>
  <dd><code>_AnimFramesPerRow</code>, <code>_AnimFramesPerColumn</code>: スプライトシートテクスチャ内のフレームのグリッドレイアウトを定義します。</dd>

  <dt><strong>フレームクロップ量</strong></dt>
  <dd><code>_FrameCropAmount</code>: 各フレームにズームインし、エッジからこのパーセンテージをクロップします（0から0.25）。</dd>
</dl>