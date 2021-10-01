---
layout: page
---

### 説明

プロジェクション変換

### 使い方

    ProjectionTransform()
        .メソッド

    ProjectionTransform(アフィン変換行列(CGAffineTransform))
        .メソッド

    ProjectionTransform(標準的な変換行列(CATransform3D))
        .メソッド

### 引数の使い方

#### CGAffineTransform

| 名前                                                                                          | 説明  |
| ------------------------------------------------------------------------------------------- | --- |
| CGAffineTransform(rotationAngle: CGFloat)                                             |     |
| CGAffineTransform(scaleX: CGFloat, y: CGFloat)                                        |     |
| CGAffineTransform(translationX: CGFloat, y: CGFloat)                                  |     |
| CGAffineTransform()                                                                         |     |
| CGAffineTransform(a: CGFloat, b: CGFloat, c: CGFloat, d: CGFloat, tx: CGFloat, ty: CGFloat) |     |
| CGAffineTransform(from decoder: Decoder)                                                    |     |

#### CATransform3D

| 説明                                                                                                                                                                                                                                            | 名前  |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| CATransform3D()                                                                                                                                                                                                                               |     |
| CATransform3D(m11: CGFloat, m12: CGFloat, m13: CGFloat, m14: CGFloat, m21: CGFloat, m22: CGFloat, m23: CGFloat, m24: CGFloat, m31: CGFloat, m32: CGFloat, m33: CGFloat, m34: CGFloat, m41: CGFloat, m42: CGFloat, m43: CGFloat, m44: CGFloat) |     |
| CATransform3D(float4x4)                                                                                                                                                                                                                       |     |
| CATransform3D(double4x4)                                                                                                                                                                                                                      |     |

### 例

#### 基本的な使い方

    ProjectionTransform()

### 宣言

    @frozen struct ProjectionTransform

### プロパティ

| 名前         | 型       | 説明  |
| ---------- | ------- | --- |
| isAffine   | Bool    |     |
| isIdentity | Bool    |     |
| m11        | CGFloat |     |
| m12        | CGFloat |     |
| m13        | CGFloat |     |
| m21        | CGFloat |     |
| m22        | CGFloat |     |
| m23        | CGFloat |     |
| m31        | CGFloat |     |
| m32        | CGFloat |     |
| m33        | CGFloat |     |

### メソッド

| 名前            | 説明        |
| ------------- | --------- |
| concatenating | コンカチネーション |
| invert        | 反転するか     |
| inverted      | 反転        |

### メソッド詳細

#### concatenating

##### 意味

コンカチネーション

##### 使い方

    .concatenating(トランスフォーム(ProjectionTransform))

##### 例

    var x = ProjectionTransform()
    ProjectionTransform()
        .concatenating(x)

#### invert

##### 意味

反転するか

##### 使い方

    .invert()

##### 例

    var projectionTransform = ProjectionTransform()
    projectionTransform.invert()

#### inverted

##### 意味

反転

##### 使い方

    .inverted()

##### 例

    var projectionTransform = ProjectionTransform()
    projectionTransform.inverted()

### 参考サイト

<https://developer.apple.com/documentation/swiftui/projectiontransform>
