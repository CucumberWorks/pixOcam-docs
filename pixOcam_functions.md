# pixOcam Shader Feature Documentation

## Base Settings

*   **Enable Shader Effect (`_EnableRendering`)**: Toggles the main shader effects (first pass) on or off. When off, the object will be invisible (or transparent), but the Camera Hack overlay (second pass) may still function if enabled.
*   **Texture (`_MainTex`)**: The main input texture that the effects will be applied to.
*   **Resolution Width / Height (`_FixedResolutionWidth`, `_FixedResolutionHeight`)**: Sets the target low resolution. The input texture is effectively downscaled to these dimensions, creating the pixelated look.
*   **Is Fullscreen Effect (`_IsFullscreenEffect`)**: (Informational) Indicates if the shader is intended for use as a fullscreen camera effect (like a post-processing effect).
*   **Object Aspect Ratio (`_ObjectAspectRatio`)**: Adjusts the aspect ratio for non-square objects (like quads) when *not* using the fullscreen effect, helping to prevent stretching.
*   **Enable Color Depth Reduction (`_ColorDepthEnabled`)**: Turns the color reduction effect on or off.
*   **Color Depth (`_ColorDepth`)**: Reduces the number of available colors, simulating retro hardware limitations. Lower values mean fewer colors (more posterized look).
*   **Contrast (`_Contrast`)**: Adjusts the difference between light and dark areas.
*   **Brightness (`_Brightness`)**: Adjusts the overall lightness or darkness of the image.

## Effect Settings

*   **Enable Dithering (`_DitherEnabled`)**: Toggles the dithering effect.
*   **Dither Strength (`_DitherStrength`)**: Controls the intensity of the dithering pattern, which helps smooth out color banding caused by `Color Depth` reduction.
*   **Enable Grain (`_GrainEnabled`)**: Toggles the grain/noise effect.
*   **Grain Strength (`_GrainStrength`)**: Controls the visibility of the grain pattern.
*   **Grain Color Variance (`_GrainColorVariance`)**: Blends the grain between grayscale noise (0) and colored noise (1).

## Color Settings

*   **Use Color Palette (`_PaletteEnabled`)**: Toggles the color remapping effect.
*   **Color Palette 1-6 (`_GradientTex1` to `_GradientTex6`)**: Texture slots for gradient textures (LUTs). The shader uses the one selected by `Gradient Preset`.
*   **Palette Steps (`_PaletteSteps`)**: Reduces the number of distinct colors sampled from the gradient texture. Creates a more banded look.
*   **Palette Blend (`_PaletteBlend`)**: Blends between the original image colors (0) and the remapped palette colors (1).
*   **Gradient Preset (`_GradientPreset`)**: Selects which `Color Palette` gradient texture (1-6) to use for the effect.

## Edge Settings

*   **Enable Edge Detection (`_EdgeDetectEnabled`)**: Toggles the outline effect.
*   **Edge Thickness (`_EdgeThickness`)**: Controls the thickness of the detected outlines.
*   **Edge Color (`_EdgeColor`)**: Sets the color of the outlines.

## Bloom Settings

*   **Enable Bloom (`_BloomEnabled`)**: Toggles the bloom effect.
*   **Bloom Threshold (`_BloomThreshold`)**: Pixels brighter than this value will contribute to the bloom effect.
*   **Bloom Intensity (`_BloomIntensity`)**: Controls the overall brightness of the bloom effect.
*   **Bloom Radius (`_BloomRadius`)**: Controls how far the bloom effect spreads from bright areas.
*   **Bloom Softness (`_BloomSoftness`)**: Controls the softness or sharpness of the bloom falloff.

## CCD Smear Settings

*   **Enable CCD Smear (`_SmearEnabled`)**: Toggles the vertical light smearing effect (CCD sensor simulation).
*   **Smear Threshold (`_SmearThreshold`)**: Pixels brighter than this value will cause smearing.
*   **Smear Intensity (`_SmearIntensity`)**: Controls the brightness of the smear streaks.
*   **Smear Length (`_SmearLength`)**: Controls how long the vertical smear streaks are.
*   **Smear Falloff (`_SmearFalloff`)**: Controls how quickly the smear effect fades along its length.

## Vignette Settings

*   **Enable Vignette (`_VignetteEnabled`)**: Toggles the vignette effect (darkening the corners).
*   **Vignette Size (`_VignetteSize`)**: Controls the size of the vignette area (higher values make the vignette smaller/tighter).
*   **Vignette Intensity (`_VignetteIntensity`)**: Controls the darkness of the vignette effect.
*   **Vignette Roundness (`_VignetteRoundness`)**: Blends the vignette shape between rectangular (0) and circular (1).
*   **Vignette Color (`_VignetteColor`)**: Sets the color used for the vignette darkening (usually black).

## Chromatic Aberration Settings

*   **Enable Chromatic Aberration (`_ChromaticEnabled`)**: Toggles the chromatic aberration (color fringing) effect.
*   **Chromatic Strength (`_ChromaticStrength`)**: Controls the overall amount of color separation.
*   **Chromatic Blur (`_ChromaticBlur`)**: Applies a blur to the separated colors, increasing with distance from the center when `Use Radial Distortion` is On.
*   **Use Radial Distortion (`_ChromaticRadialMode`)**: Switches between two modes:
    *   **On (Radial):** Simulates realistic lens distortion, separating colors radially from the center.
    *   **Off (Vector):** Separates colors based on fixed `Red/Green/Blue Channel Offset` vectors.
*   **Red/Green/Blue Channel Offset (`_ChromaticRedOffset`, etc.)**: (Used when `Use Radial Distortion` is Off) Defines the direction and distance each color channel is shifted.

## Camera Hack Settings

*This feature allows the shader effect (applied to an object like a quad) to display fullscreen under specific conditions (e.g., on a spectator camera view in VRChat), simulating a camera's viewfinder or screen.*

*   **Enable Camera Hack (`_CameraHackEnabled`)**: Toggles the Camera Hack mode. Requires specific screen resolutions or `Bypass Resolution Check (Debug)` to be enabled. Won't activate in VR headset views.
*   **Camera Hack Radius (`_CameraHackRadius`)**: The maximum distance (relative to object size) the camera can be from the object for the hack to activate.
*   **Border Size (`_BorderSize`)**: Sets the size of the black border around the 4:3 content area when the Camera Hack is active and the `Show Information Overlay` is on.
*   **Left Align Content (`_LeftAlign`)**: When enabled, aligns the 4:3 content area to the left within the screen borders, instead of centering it.
*   **Bypass Resolution Check (Debug) (`_DisableResolutionCheck`)**: Allows the Camera Hack to activate regardless of screen resolution (useful for testing).

## UI Overlay Settings

*These settings only apply when `Enable Camera Hack` and `Show Information Overlay` are both turned on.*

*   **Font Texture (16x16) (`_FontTex`)**: A 16x16 grid texture containing the characters used for the overlay text.
*   **Show Information Overlay (`_ShowOverlay`)**: Toggles the visibility of the overlay elements (text, visualizers, white border) within the Camera Hack's border area. If off, the content area stretches to fill the screen while maintaining aspect ratio.
*   **Overlay Text Color (`_OverlayColor`)**: Sets the color for the text displayed in the overlay.

## Custom Texture Visualizer Settings

*   **Custom Visualizer Texture (`_CustomVisualizerTex`)**: The texture to display in the secondary visualizer box in the UI Overlay (useful for seeing how your textures look with the effects).
*   **Show Custom Texture Visualizer (`_ShowCustomVisualizer`)**: Toggles the visibility of this specific visualizer in the UI Overlay.
*   **Visualizer Pixel Density (`_CustomVisualizerPixelDensity`)**: Controls the pixelation level applied *specifically* to the texture shown in the Custom Visualizer box.

## Atlas / Sprite Sheet Settings (For Custom Visualizer)

*These settings control animation if the `Custom Visualizer Texture` is a sprite sheet.*

*   **Enable Animation (`_IsAnimatedTexture`)**: Tells the shader to treat the `Custom Visualizer Texture` as an animated sprite sheet.
*   **Animation Frame Count (`_AnimFrameCount`)**: The total number of frames in the animation sequence.
*   **Animation Speed (`_AnimSpeed`)**: Controls the playback speed of the animation.
*   **Frames Per Row / Column (`_AnimFramesPerRow`, `_AnimFramesPerColumn`)**: Defines the grid layout of frames within the sprite sheet texture.
*   **Frame Crop Amount (`_FrameCropAmount`)**: Zooms into each frame by cropping this percentage from the edges (0 to 0.25).

## Procedural Visualizer Settings (UI Overlay Only)

*These control the appearance of the primary procedural visualizer (orbiting circles) in the UI Overlay.*

*   **Orbital Speed (`_OrbitalSpeed`)**: Controls how fast the primary circle orbits within the visualizer box.
*   **Orbital Width / Height (`_OrbitalWidth`, `_OrbitalHeight`)**: Define the shape and size of the elliptical orbit path.
*   **Secondary Circle Size (`_SecondaryCircleSize`)**: Controls the size of the second, opposing circle relative to the primary one.
*   **Secondary Circle Blend (`_SecondaryCircleBlend`)**: Controls the opacity/brightness of the secondary circle.
*   **Primary / Secondary Circle Color (`_PrimaryCircleColor`, `_SecondaryCircleColor`)**: Sets the [HDR](https://docs.unity3d.com/Manual/HDRColorPicker.html) colors for the two orbiting circles in the visualizer.

---

# pixOcam シェーダー機能ドキュメント

## 基本設定

*   **シェーダーエフェクト有効化 (`_EnableRendering`)**: 主要なシェーダーエフェクト（最初のパス）をオンまたはオフに切り替えます。オフの場合、オブジェクトは非表示（または透明）になりますが、カメラハックのオーバーレイ（2番目のパス）は有効であれば機能し続けます。
*   **メインテクスチャ (`_MainTex`)**: エフェクトが適用される主要な入力テクスチャです。
*   **解像度 幅 / 高さ (`_FixedResolutionWidth`, `_FixedResolutionHeight`)**: ターゲットとなる低解像度を設定します。入力テクスチャは実質的にこれらの寸法にダウンスケールされ、ピクセル化された外観を作成します。
*   **フルスクリーンエフェクト (`_IsFullscreenEffect`)**: (情報提供用) シェーダーがフルスクリーンのカメラエフェクト（ポストプロセスエフェクトのようなもの）として使用されることを意図しているかどうかを示します。
*   **オブジェクトアスペクト比 (`_ObjectAspectRatio`)**: フルスクリーンエフェクトを使用しない場合に、正方形でないオブジェクト（クアッドなど）のアスペクト比を調整し、引き伸ばしを防ぎます。
*   **色深度削減有効化 (`_ColorDepthEnabled`)**: 色削減エフェクトをオンまたはオフにします。
*   **色深度 (`_ColorDepth`)**: 利用可能な色数を減らし、レトロなハードウェアの制限をシミュレートします。値が低いほど色数が少なくなります（よりポスタライズされた見た目になります）。
*   **コントラスト (`_Contrast`)**: 明るい領域と暗い領域の差を調整します。
*   **明るさ (`_Brightness`)**: 画像全体の明るさまたは暗さを調整します。

## エフェクト設定

*   **ディザリング有効化 (`_DitherEnabled`)**: ディザリングエフェクトを切り替えます。
*   **ディザ強度 (`_DitherStrength`)**: ディザリングパターンの強度を制御します。これは`色深度 / Color Depth`削減によって引き起こされるカラーバンディングを滑らかにするのに役立ちます。
*   **グレイン有効化 (`_GrainEnabled`)**: グレイン/ノイズエフェクトを切り替えます。
*   **グレイン強度 (`_GrainStrength`)**: グレインパターンの可視性を制御します。
*   **グレイン色分散 (`_GrainColorVariance`)**: グレインをグレースケールノイズ（0）とカラーノイズ（1）の間でブレンドします。

## カラーパレット

*   **カラーパレット有効化 (`_PaletteEnabled`)**: カラーリマッピングエフェクトを切り替えます。
*   **グラデーションテクスチャ 1-6 (`_GradientTex1` ～ `_GradientTex6`)**: グラデーションテクスチャ（LUT）用のテクスチャスロットです。シェーダーは`グラデーションプリセット`で選択されたものを使用します。
*   **パレット段階数 (`_PaletteSteps`)**: グラデーションテクスチャからサンプリングされる個別の色数を減らします。よりバンディングされた見た目を作成します。
*   **パレット混合 (`_PaletteBlend`)**: 元の画像の色（0）とリマップされたパレットの色（1）の間でブレンドします。
*   **グラデーションプリセット (`_GradientPreset`)**: エフェクトに使用する`カラーパレット`グラデーションテクスチャ（1～6）を選択します。

## エッジ検出

*   **エッジ検出有効化 (`_EdgeDetectEnabled`)**: アウトラインエフェクトを切り替えます。
*   **エッジ太さ (`_EdgeThickness`)**: 検出されたアウトラインの太さを制御します。
*   **エッジ色 (`_EdgeColor`)**: アウトラインの色を設定します。

## ブルーム

*   **ブルーム有効化 (`_BloomEnabled`)**: ブルームエフェクトを切り替えます。
*   **ブルームしきい値 (`_BloomThreshold`)**: この値より明るいピクセルがブルームエフェクトに寄与します。
*   **ブルーム強度 (`_BloomIntensity`)**: ブルームエフェクト全体の明るさを制御します。
*   **ブルーム半径 (`_BloomRadius`)**: ブルームエフェクトが明るい領域からどれだけ広がるかを制御します。
*   **ブルーム柔らかさ (`_BloomSoftness`)**: ブルームの減衰の柔らかさまたはシャープさを制御します。

## CCDスミア

*   **CCDスミア有効化 (`_SmearEnabled`)**: 垂直方向の光のにじみエフェクト（CCDセンサーシミュレーション）を切り替えます。
*   **スミアしきい値 (`_SmearThreshold`)**: この値より明るいピクセルがスミアリングを引き起こします。
*   **スミア強度 (`_SmearIntensity`)**: スミアストリークの明るさを制御します。
*   **スミア長さ (`_SmearLength`)**: 垂直方向のスミアストリークの長さを制御します。
*   **スミア減衰 (`_SmearFalloff`)**: スミアエフェクトがその長さに沿ってどれだけ速くフェードするかを制御します。

## ビネット設定

*   **ビネット有効化 (`_VignetteEnabled`)**: ビネットエフェクト（角を暗くする効果）を切り替えます。
*   **ビネットサイズ (`_VignetteSize`)**: ビネット領域のサイズを制御します（値が高いほどビネットが小さく/タイトになります）。
*   **ビネット強度 (`_VignetteIntensity`)**: ビネットエフェクトの暗さを制御します。
*   **ビネット丸み (`_VignetteRoundness`)**: ビネットの形状を長方形（0）と円形（1）の間でブレンドします。
*   **ビネット色 (`_VignetteColor`)**: ビネットの暗色化に使用される色を設定します（通常は黒）。

## 色収差設定

*   **色収差有効化 (`_ChromaticEnabled`)**: 色収差（カラーフリンジ）エフェクトを切り替えます。
*   **色収差強度 (`_ChromaticStrength`)**: 色分離の全体的な量を制御します。
*   **エッジぼかし量 (`_ChromaticBlur`)**: 分離された色にぼかしを適用します。`リアルレンズモデル使用 / Use Radial Distortion`がオンの場合、中心からの距離に応じて増加します。
*   **リアルレンズモデル使用 (`_ChromaticRadialMode`)**: 2つのモードを切り替えます:
    *   **オン (放射状):** リアルなレンズ歪みをシミュレートし、中心から放射状に色を分離します。
    *   **オフ (ベクトル):** 固定された`赤/緑/青チャンネルオフセット`ベクトルに基づいて色を分離します。
*   **赤/緑/青チャンネルオフセット (`_ChromaticRedOffset`, etc.)**: (`リアルレンズモデル使用 / Use Radial Distortion`がオフの場合に使用) 各カラーチャンネルがシフトされる方向と距離を定義します。

## カメラハック

*この機能により、シェーダーエフェクト（クアッドなどのオブジェクトに適用）が特定の条件下（例：VRChatの観客カメラビューなど）でフルスクリーン表示され、カメラのビューファインダーやスクリーンをシミュレートできます。*

*   **カメラハック有効化 (`_CameraHackEnabled`)**: カメラハックモードを切り替えます。特定の画面解像度または`解像度チェック回避 (デバッグ) / Bypass Resolution Check (Debug)`の有効化が必要です。VRヘッドセットビューではアクティブになりません。
*   **カメラハック半径 (`_CameraHackRadius`)**: ハックがアクティブになるために、カメラがオブジェクトから（オブジェクトサイズに対して）どれだけ離れられるかの最大距離。
*   **境界サイズ (`_BorderSize`)**: カメラハックがアクティブで`情報オーバーレイ表示`がオンのときに、4:3コンテンツ領域の周りに表示される黒い境界線のサイズを設定します。
*   **コンテンツ左揃え (`_LeftAlign`)**: 有効にすると、4:3コンテンツ領域を画面境界内で中央揃えする代わりに左揃えにします。
*   **解像度チェック回避 (デバッグ) (`_DisableResolutionCheck`)**: 画面解像度に関係なくカメラハックをアクティブにできます（テストに便利）。

## 情報オーバーレイ

*これらの設定は、`カメラハック有効化`と`情報オーバーレイ表示`の両方がオンの場合にのみ適用されます。*

*   **フォントテクスチャ (16x16グリッド) (`_FontTex`)**: オーバーレイテキストに使用される文字を含む16x16グリッドテクスチャ。
*   **情報オーバーレイ表示 (`_ShowOverlay`)**: カメラハックの境界領域内のオーバーレイ要素（テキスト、ビジュアライザー、白い境界線）の可視性を切り替えます。オフの場合、コンテンツ領域はアスペクト比を維持しながら画面いっぱいに引き伸ばされます。
*   **オーバーレイ文字色 (`_OverlayColor`)**: オーバーレイに表示されるテキストの色を設定します。

## カスタムテクスチャビジュアライザー

*   **カスタムテクスチャ (`_CustomVisualizerTex`)**: UIオーバーレイのセカンダリビジュアライザーボックスに表示するテクスチャ（自分のテクスチャがエフェクト適用後どのように見えるか確認するのに便利です）。
*   **カスタムテクスチャビジュアライザー表示 (`_ShowCustomVisualizer`)**: UIオーバーレイでこの特定のビジュアライザーの可視性を切り替えます。
*   **ビジュアライザーピクセル密度 (`_CustomVisualizerPixelDensity`)**: カスタムビジュアライザーボックスに表示されるテクスチャに*特別に*適用されるピクセル化レベルを制御します。

## アトラス / スプライトシート設定 (カスタムビジュアライザー用)

*これらの設定は、`カスタムテクスチャ`がスプライトシートの場合のアニメーションを制御します。*

*   **アニメーション有効化 (`_IsAnimatedTexture`)**: シェーダーに`カスタムテクスチャ`をアニメーション化されたスプライトシートとして扱うように指示します。
*   **総フレーム数 (`_AnimFrameCount`)**: アニメーションシーケンス内の総フレーム数。
*   **アニメーション速度 (`_AnimSpeed`)**: アニメーションの再生速度を制御します。
*   **行あたりフレーム数 / 列あたりフレーム数 (`_AnimFramesPerRow`, `_AnimFramesPerColumn`)**: スプライトシートテクスチャ内のフレームのグリッドレイアウトを定義します。
*   **フレームクロップ量 (`_FrameCropAmount`)**: 各フレームにズームインし、エッジからこのパーセンテージをクロップします（0から0.25）。

## プロシージャルビジュアライザー設定 (UIオーバーレイのみ)

*これらは、UIオーバーレイ内の主要なプロシージャルビジュアライザー（周回する円）の外観を制御します。*

*   **軌道速度 (`_OrbitalSpeed`)**: 主要な円がビジュアライザーボックス内でどれだけ速く周回するかを制御します。
*   **軌道幅 / 高さ (`_OrbitalWidth`, `_OrbitalHeight`)**: 楕円軌道パスの形状とサイズを定義します。
*   **副円のサイズ (`_SecondaryCircleSize`)**: 主要な円に対する2番目の反対側の円のサイズを制御します。
*   **副円のブレンド (`_SecondaryCircleBlend`)**: 2番目の円の不透明度/明るさを制御します。
*   **主円の色 / 副円の色 (`_PrimaryCircleColor`, `_SecondaryCircleColor`)**: ビジュアライザー内の2つの周回する円の[HDR](https://docs.unity3d.com/ja/current/Manual/HDRColorPicker.html)カラーを設定します。 