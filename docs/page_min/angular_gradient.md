---
layout: page
---

### 説明

円形グラデーション

### 使い方

#### 全回転角度グラデーションの作成

    AngularGradient(gradient: グラデーション構造体(Gradient), center: 中心位置(UnitPoint), angle: 角度(Angle) = .zero)

    AngularGradient(colors: カラーの配列([Color]), center: 中心位置(UnitPoint), angle: 角度(Angle) = .zero)

    AngularGradient(stops: 1色グラデーションの配列([Gradient.Stop]), center: 中心位置(UnitPoint), angle: 角度(Angle) = .zero)

#### 部分回転角型グラデーションの作成

    AngularGradient(gradient: グラデーション構造体(Gradient), center: 中心位置(UnitPoint), startAngle: 開始角度(Angle) = .zero, endAngle: 終了角度(Angle) = .zero)

    AngularGradient(colors: カラーの配列([Color]), center: 中心位置(UnitPoint), startAngle: 開始角度(Angle), endAngle: 終了角度(Angle))

    AngularGradient(stops: 1色グラデーションの配列([Gradient.Stop]), center: 中心位置(UnitPoint), startAngle: 開始角度(Angle), endAngle: 終了角度(Angle))

### 引数の使い方

#### Gradient

| 名前                               | 説明                     |
| -------------------------------- | ---------------------- |
| Gradient(colors: [Color])        | 色の配列からグラデーションを作成       |
| Gradient(stops: [Gradient.Stop]) | カラーストップの配列からグラデーションを作成 |

#### Gradient.Stop

| 名前                                    | 説明                  |
| ------------------------------------- | ------------------- |
| init(color: Color, location: CGFloat) | 色と場所を指定してカラーストップを作成 |

#### UnitPoint

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

##### Angle

| 名前               | 説明      |
| ---------------- | ------- |
| .degrees(Double) | 度を指定    |
| .radians(Double) | ラジアンを指定 |
| .zero            | ゼロ      |

### 例

#### 基本的な使い方

    AngularGradient(gradient: Gradient(colors: [.pink, .purple, .pink]), center: .center, angle: .degrees(0))

#### 部分回転角型グラデーションの作成

    AngularGradient(gradient: Gradient(colors: [.pink, .purple, .pink]), center: .center, startAngle: .degrees(45), endAngle: .degrees(180))

### 宣言

    @frozen struct AngularGradient
