---
layout: page
---

### 説明

直線的なグラデーション

### 使い方

    LinearGradient(gradient: グラデーション(Gradient), startPoint: 開始位置(UnitPoint), endPoint: 終了位置(UnitPoint))

### 引数の使い方

#### Gradient

| 名前                               | 説明                     |
| -------------------------------- | ---------------------- |
| Gradient(colors: [Color])        | 色の配列からグラデーションを作成       |
| Gradient(stops: [Gradient.Stop]) | カラーストップの配列からグラデーションを作成 |

#### UnitPoint

| 名前                                | 説明         |
| --------------------------------- | ---------- |
| bottom                            | 下          |
| bottomLeading                     | 左下         |
| bottomTrailing                    | 右下         |
| center                            | 真ん中        |
| leading                           | 左          |
| top                               | 上          |
| topLeading                        | 左上         |
| topTrailing                       | 右上         |
| trailing                          | 右          |
| zero                              | 0          |
| UnitPoint()                       | 作成         |
| UnitPoint(x: CGFloat, y: CGFloat) | xとyを指定して作成 |

### 例

#### 基本的な使い方

    LinearGradient(gradient: Gradient(colors: [.red]), startPoint: .top, endPoint: .bottom)

### 宣言

    @frozen struct LinearGradient

### 参考サイト

<https://developer.apple.com/documentation/swiftui/lineargradient>
