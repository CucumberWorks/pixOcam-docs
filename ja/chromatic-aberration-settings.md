---
title: 色収差設定
layout: default
parent: pixOcam シェーダー機能 (JA)
nav_order: 8
permalink: /ja/chromatic-aberration-settings/
---

## 色収差設定

*   **色収差有効化 (`_ChromaticEnabled`)**:
    色収差（カラーフリンジ）エフェクトを切り替えます。
*   **色収差強度 (`_ChromaticStrength`)**:
    色分離の全体的な量を制御します。
*   **エッジぼかし量 (`_ChromaticBlur`)**:
    分離された色にぼかしを適用します。`リアルレンズモデル使用 / Use Radial Distortion`がオンの場合、中心からの距離に応じて増加します。
*   **リアルレンズモデル使用 (`_ChromaticRadialMode`)**:
    2つのモードを切り替えます:
    *   **オン (放射状):** リアルなレンズ歪みをシミュレートし、中心から放射状に色を分離します。
    *   **オフ (ベクトル):** 固定された`赤/緑/青チャンネルオフセット`ベクトルに基づいて色を分離します。
*   **赤/緑/青チャンネルオフセット (`_ChromaticRedOffset`, etc.)**:
    (`リアルレンズモデル使用 / Use Radial Distortion`がオフの場合に使用) 各カラーチャンネルがシフトされる方向と距離を定義します。 