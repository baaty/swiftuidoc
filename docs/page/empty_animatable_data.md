---
layout: page
---

### 説明

アニメーション可能なデータのための空の型

### 使い方

    EmptyAnimatableData()

### 例

#### 基本的な使い方

    EmptyAnimatableData()

### 宣言

    @frozen struct EmptyAnimatableData

### プロパティ

| 名前               | 型                   | 説明                    |
| ---------------- | ------------------- | --------------------- |
| zero             | EmptyAnimatableData | ゼロ                    |
| magnitudeSquared | Double              | インスタンスと自分自身とのドットプロダクト |

### メソッド

| 名前    | 説明  |
| ----- | --- |
| scale | 乗算  |

### メソッド詳細

#### scale

##### 意味

乗算

##### 使い方

    .scale(by: 乗算(Double))

##### 例

    EmptyAnimatableData()
        .scale(by: 1.0)

### 参考サイト

<https://developer.apple.com/documentation/swiftui/emptyanimatabledata>
