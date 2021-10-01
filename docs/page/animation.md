---
layout: page
---

### 説明

再利用可能なアクションを作成

### 宣言

    @frozen struct Animation

### プロパティ

| 名前                  | 型         | 説明                  |
| ------------------- | --------- | ------------------- |
| Animation.default   | Animation | デフォルト               |
| Animation.easeIn    | Animation | 徐々に加速               |
| Animation.easeInOut | Animation | 加速してから減速            |
| Animation.easeOut   | Animation | 徐々に減速               |
| Animation.linear    | Animation | 等速で変化               |
| customMirror        | Mirror    | インスタンスのカスタムミラー      |
| debugDescription    | String    | デバック用のインスタンスのテキスト表現 |
| description         | String    | インスタンスのテキスト表現       |

### メソッド

| 名前                            | 説明                    |
| ----------------------------- | --------------------- |
| Animation.easeIn              | 徐々に加速                 |
| Animation.easeInOut           | 加速してから減速              |
| Animation.easeOut             | 徐々に減速                 |
| Animation.interactiveSpring   | インタラクティブなスプリングアニメーション |
| Animation.interpolatingSpring | 補間スプリングアニメーション        |
| Animation.linear              | 等速で変化                 |
| Animation.spring              | スプリングアニメーション          |
| Animation.timingCurve         | タイミング曲線               |

### メソッド詳細

#### easeIn

##### 意味

徐々に加速

##### 使い方

    .easeIn(duration: 持続時間(Double))

##### 例

    Animation.easeIn(duration: 2)

#### easeInOut

##### 意味

加速してから減速

##### 使い方

    .easeInOut(duration: 持続時間(Double))

##### 例

    Animation.easeInOut(duration: 2)

#### easeOut

##### 意味

徐々に減速

##### 使い方

    .easeOut(duration: 持続時間(Double))

##### 例

    Animation.easeOut(duration: 2)

#### interactiveSpring

##### 意味

インタラクティブなスプリングアニメーション

##### 使い方

    .interactiveSpring(response: レスポンス(Double) = 0.15, dampingFraction: 減衰率(Double) = 0.86, blendDuration: ブレンド時間(Double) = 0.25)

##### 例

    Animation.interactiveSpring(response: Double = 0.15, dampingFraction: Double = 0.86, blendDuration: Double = 0.25)

#### interpolatingSpring

##### 意味

補間スプリングアニメーション

##### 使い方

    .interpolatingSpring(mass: 質量(Double) = 1.0, stiffness: 硬さ(Double), damping: ダンピング値(Double), initialVelocity: 範囲(Double) = 0.0)

##### 例

    Animation.interpolatingSpring(mass: 1.0, stiffness: 1.0, damping: 1.0, initialVelocity: 0.0)

#### linear

##### 意味

等速で変化

##### 使い方

    .linear(duration: 持続時間(Double))

##### 例

    Animation.linear(duration: 2.0)

#### .spring(response: Double = 0.55, dampingFraction: Double = 0.825, blendDuration: Double = 0)

##### 意味

スプリングアニメーション

##### 使い方

    .spring(response: 硬さ(Double) = 0.55, dampingFraction: ドラッグの量(Double) = 0.825, blendDuration: 応答値の変化を補間するための時間(Double) = 0)

##### 例

    .spring()

#### timingCurve

##### 意味

タイミング曲線

##### 使い方

    .timingCurve(X0(Double), Y0(Double), X1(Double), _ Y1(Double), duration: 持続時間(Double) = 0.35)

##### 例

    Animation.timingCurve(1.0, 1.0, 2.0, 2.0)

### 参考サイト

<https://developer.apple.com/documentation/swiftui/animation>
