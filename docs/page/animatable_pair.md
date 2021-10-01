---
layout: page
---

### 説明

複数プロパティをアニメーション

### 使い方

    AnimatablePair<1つ目のアニメーション(VectorArithmetic), ２つ目のアニメーション(VectorArithmetic)>

### 例

#### 基本的な使い方

    var rows: Int
    var columns: Int
    public var animatableData: AnimatablePair<Double, Double>{
        get {
            AnimatablePair(Double(rows), Double(columns))
        }
        set {
            self.rows = Int(newValue.first)
            self.columns = Int(newValue.second)
        }
    }

### 宣言

    @frozen struct AnimatablePair<First, Second> where First : VectorArithmetic, Second : VectorArithmetic

### プロパティ

| 名前               | 型                                | 説明                             |
| ---------------- | -------------------------------- | ------------------------------ |
| zero             | AnimatablePair&lt;First, Second> | ゼロ                             |
| first            | First                            | 1つ目のアニメーション                    |
| second           | Second                           | 2つ目のアニメーション                    |
| magnitudeSquared | Double                           | アニメーションペアのドットプロダクトは自分自身との組み合わせ |

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

    animatableData
        .scale(by: 1.0)

### 参考サイト

<https://developer.apple.com/documentation/swiftui/animatablepair>
