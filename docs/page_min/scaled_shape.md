---
layout: page
---

### 説明

スケールトランスフォームが適用された形状

### 使い方

    ScaledShape(shape: シェイプ(Content), scale: スケール(CGSize), anchor: 開始位置(UnitPoint) = .center)

### 引数の使い方

#### CGSizeの使い方

| 名前                                                   | 説明                         |
| ---------------------------------------------------- | -------------------------- |
| CGSize()                                             | 幅と高さがゼロのサイズを作成             |
| CGSize?(dictionaryRepresentation dict: CFDictionary) | 正規の辞書表現からサイズを作成            |
| CGSize(from decoder: Decoder)                        | Decoderを指定                 |
| CGSize(width: Double, height: Double)                | 浮動小数点値で指定された寸法を持つサイズを作成    |
| CGSize(width: CGFloat, height: CGFloat)              | CGFloatの値で指定された寸法を持つサイズを作成 |
| CGSize(width: Int, height: Int)                      | 整数値で指定された寸法を持つサイズを作成       |

#### UnitPointの使い方

| 名前                                | 説明         |
| --------------------------------- | ---------- |
| .bottom                           | 下          |
| .bottomLeading                    | 左下         |
| .bottomTrailing                   | 右下         |
| .center                           | 中央        |
| .leading                          | 左          |
| .top                              | 上          |
| .topLeading                       | 左上         |
| .topTrailing                      | 右上         |
| .trailing                         | 右          |
| .zero                             | 0          |
| UnitPoint()                       | 作成         |
| UnitPoint(x: CGFloat, y: CGFloat) | xとyを指定して作成 |

### 例

#### 基本的な使い方

    ScaledShape(shape: Circle(), scale: CGSize())

### 宣言

    @frozen struct ScaledShape<Content> where Content : Shape

### プロパティ

| 名前             | 型                                   | 説明              |
| -------------- | ----------------------------------- | --------------- |
| anchor         | UnitPoint                           | 開始位置            |
| animatableData | ScaledShape<Content>.AnimatableData | アニメーションするためのデータ |
| scale          | CGSize                              | スケール            |
| shape          | Content                             | 図形              |
