---
layout: page
---

### 説明

並進オフセット変換が適用された形状

### 使い方

    OffsetShape(shape: シェイプ(Shape), offset: オフセット(CGSize))

### 引数の使い方

#### CGSize

| 名前                                                   | 説明                         |
| ---------------------------------------------------- | -------------------------- |
| CGSize()                                             | 幅と高さがゼロのサイズを作成             |
| CGSize?(dictionaryRepresentation dict: CFDictionary) | 正規の辞書表現からサイズを作成            |
| CGSize(from decoder: Decoder)                        | Decoderを指定                 |
| CGSize(width: Double, height: Double)                | 浮動小数点値で指定された寸法を持つサイズを作成    |
| CGSize(width: CGFloat, height: CGFloat)              | CGFloatの値で指定された寸法を持つサイズを作成 |
| CGSize(width: Int, height: Int)                      | 整数値で指定された寸法を持つサイズを作成       |

### 例

#### 基本的な使い方

    OffsetShape(shape: Circle(), offset: CGSize())

### 宣言

    @frozen struct OffsetShape<Content> where Content : Shape

### プロパティ

| 名前             | 型                                   | 説明              |
| -------------- | ----------------------------------- | --------------- |
| animatableData | ScaledShape<Content>.AnimatableData | アニメーションするためのデータ |
| offset         | CGSize                              | オフセット           |
| shape          | Content                             | 図形              |
