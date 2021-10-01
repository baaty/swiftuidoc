---
layout: page
---

### 説明

プロジェクション変換

### 使い方

    ProjectionTransform()

    ProjectionTransform(アフィン変換行列(CGAffineTransform))

    ProjectionTransform(標準的な変換行列(CATransform3D))

### 引数の使い方

#### CGAffineTransform

| 名前                                                                                          | 説明                         |
| ------------------------------------------------------------------------------------------- | -------------------------- |
| CGAffineTransform(rotationAngle: CGFloat)                                                   | 指定された回転値から構築されたアフィン変換行列    |
| CGAffineTransform(scaleX: CGFloat, y: CGFloat)                                              | 指定したスケーリング値から構築されたアフィン変換行列 |
| CGAffineTransform(translationX: CGFloat, y: CGFloat)                                        | 与えられた翻訳値から構築されたアフィン変換行列    |
| CGAffineTransform()                                                                         | アフィン変換行列                   |
| CGAffineTransform(a: CGFloat, b: CGFloat, c: CGFloat, d: CGFloat, tx: CGFloat, ty: CGFloat) | アフィン変換行列                   |
| CGAffineTransform(from decoder: Decoder)                                                    | アフィン変換行列                   |

#### CATransform3D

| 説明                                                                                                                                                                                                                                            | 名前       |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| CATransform3D()                                                                                                                                                                                                                               | 標準的な変換行列 |
| CATransform3D(m11: CGFloat, m12: CGFloat, m13: CGFloat, m14: CGFloat, m21: CGFloat, m22: CGFloat, m23: CGFloat, m24: CGFloat, m31: CGFloat, m32: CGFloat, m33: CGFloat, m34: CGFloat, m41: CGFloat, m42: CGFloat, m43: CGFloat, m44: CGFloat) | 標準的な変換行列 |
| CATransform3D(float4x4)                                                                                                                                                                                                                       | 標準的な変換行列 |
| CATransform3D(double4x4)                                                                                                                                                                                                                      | 標準的な変換行列 |

### 例

#### 基本的な使い方

    ProjectionTransform()

### 宣言

    @frozen struct ProjectionTransform

### プロパティ

| 名前         | 型       | 説明                    |
| ---------- | ------- | --------------------- |
| isAffine   | Bool    | 変換行列か                 |
| isIdentity | Bool    | アフィン変換が同一の変換であるか      |
| m11        | CGFloat | マトリックスの1,1の位置にあるエントリー |
| m12        | CGFloat | マトリックスの1,2の位置にあるエントリー |
| m13        | CGFloat | マトリックスの1,3の位置にあるエントリー |
| m21        | CGFloat | マトリックスの2,1の位置にあるエントリー |
| m22        | CGFloat | マトリックスの2,2の位置にあるエントリー |
| m23        | CGFloat | マトリックスの2,3の位置にあるエントリー |
| m31        | CGFloat | マトリックスの3,1の位置にあるエントリー |
| m32        | CGFloat | マトリックスの3,2の位置にあるエントリー |
| m33        | CGFloat | マトリックスの3,3の位置にあるエントリー |

### メソッド

| 名前            | 説明        |
| ------------- | --------- |
| concatenating | コンカチネーション |
| invert        | 反転するか     |
| inverted      | 反転        |
