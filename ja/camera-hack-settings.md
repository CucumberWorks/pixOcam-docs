---
title: カメラハック
layout: default
parent: pixOcam シェーダー機能 (JA)
nav_order: 9
permalink: /ja/camera-hack-settings/
---

## カメラハック

*この機能により、シェーダーエフェクト（クアッドなどのオブジェクトに適用）が特定の条件下（例：VRChatの観客カメラビューなど）でフルスクリーン表示され、カメラのビューファインダーやスクリーンをシミュレートできます。*

<dl>
  <dt><strong>カメラハック有効化</strong></dt>
  <dd><code>_CameraHackEnabled</code>: カメラハックモードを切り替えます。特定の画面解像度または`解像度チェック回避 (デバッグ) / Bypass Resolution Check (Debug)`の有効化が必要です。VRヘッドセットビューではアクティブになりません。</dd>

  <dt><strong>カメラハック半径</strong></dt>
  <dd><code>_CameraHackRadius</code>: ハックがアクティブになるために、カメラがオブジェクトから（オブジェクトサイズに対して）どれだけ離れられるかの最大距離。</dd>

  <dt><strong>境界サイズ</strong></dt>
  <dd><code>_BorderSize</code>: カメラハックがアクティブで`情報オーバーレイ表示`がオンのときに、4:3コンテンツ領域の周りに表示される黒い境界線のサイズを設定します。</dd>

  <dt><strong>コンテンツ左揃え</strong></dt>
  <dd><code>_LeftAlign</code>: 有効にすると、4:3コンテンツ領域を画面境界内で中央揃えする代わりに左揃えにします。</dd>

  <dt><strong>解像度チェック回避 (デバッグ)</strong></dt>
  <dd><code>_DisableResolutionCheck</code>: 画面解像度に関係なくカメラハックをアクティブにできます（テストに便利）。</dd>
</dl> 